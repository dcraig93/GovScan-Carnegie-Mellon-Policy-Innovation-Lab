from llama_index import StorageContext, load_index_from_storage
from llama_index import VectorStoreIndex
from llama_index.vector_stores import PineconeVectorStore
from llama_index.query_engine import CitationQueryEngine
from llama_index.vector_stores.types import ExactMatchFilter, MetadataFilters
import pinecone
import os
import streamlit as st

#Query Engine and Streamlit App
#run this file by entering the following in your command line (ensure you are within this files directory): streamlit run query_engine.py

st.set_page_config(layout="wide")

os.environ['OPENAI_API_KEY'] = 'INSERT YOUR API KEY HERE'
os.environ['PINECONE_API_KEY'] = 'INSERT YOUR API KEY HERE' #can create free pod (first is free) here https://www.pinecone.io/
os.environ['PINECONE_ENVIRONMENT'] = 'gcp-starter' #update with the environment for your Pinecone Vector DB

# initialize connection to pinecone
pinecone.init(
    api_key=os.environ['PINECONE_API_KEY'],
    environment=os.environ['PINECONE_ENVIRONMENT']
)

index_name = 'INSERT INDEX NAME'
pinecone_index = pinecone.Index(index_name)
vector_store = PineconeVectorStore(pinecone_index=pinecone_index)

# rebuild storage context
storage_context_1 = StorageContext.from_defaults(persist_dir="INSERT YOUR FIRST LOCAL DIRECTORY HERE")
# load your index from stored vectors
index_1 = VectorStoreIndex.from_vector_store(
    vector_store, storage_context=1
)
query_engine_1 = CitationQueryEngine.from_args(
    index_1,
    similarity_top_k=3,
    citation_chunk_size=500,
    filters=MetadataFilters(
        filters=[
            ExactMatchFilter(key="filename", value="INSERT ORIGINAL FILE NAME FOR PDF"), #filter your index so that this engine only returns results from your first PDF
        ]
    ),
)

# rebuild storage context
storage_context_2 = StorageContext.from_defaults(persist_dir="INSERT YOUR SECOND LOCAL DIRECTORY HERE")
# load your index from stored vectors
index_2 = VectorStoreIndex.from_vector_store(
    vector_store, storage_context=storage_context_2
)
query_engine_2 = CitationQueryEngine.from_args(
    index_2,
    similarity_top_k=3,
    citation_chunk_size=500,
    filters=MetadataFilters(
        filters=[
            ExactMatchFilter(key="filename", value="INSERT ORIGINAL FILE NAME FOR PDF"), #filter your index so that this engine only returns results from your second PDF
        ]
    ),
)

def main():
    st.title("GovScan")

    with st.form(key='query_form'):
        # Text input within the form, using a local variable
        query_input = st.text_input("Type your questions like you're chatting with a human:")

        # Submit button for the form
        submit_button = st.form_submit_button(label="Run Scan")

    if submit_button:
        # Use a local variable instead of session state for the query
        query = query_input

        # Debug print
        #print(f"Running query: {query}")

        # Run queries (without threads for debugging)
        response_1 = run_query(query_engine_1, query)
        response_2 = run_query(query_engine_2, query)

        # Create two columns for Pennsylvania and Ohio results
        col1, col2 = st.columns(2)

        # Display Pennsylvania results in the first column
        with col1:
            st.subheader("Results from Index 1:")
            st.write(response_1.response)
            with st.expander("Index 1 Sources"):
                for i, node in enumerate(response_1.source_nodes[:3]):
                    pages_metadata = node.node.metadata.get('pages', [])
                    page_info = f"Page: {pages_metadata[0]}" if pages_metadata else "Page info not available"
                    st.subheader(f"Source #{i+1}, {page_info}")
                    st.write(node.node.get_text())

        # Display Ohio results in the second column
        with col2:
            st.subheader("Results from Index 2:")
            st.write(response_2.response)
            with st.expander("Index 2 Sources"):
                for i, node in enumerate(response_2.source_nodes[:3]):
                    pages_metadata = node.node.metadata.get('pages', [])
                    page_info = f"Page: {pages_metadata[0]}" if pages_metadata else "Page info not available"
                    st.subheader(f"Source #{i+1}, {page_info}")
                    st.write(node.node.get_text())


def run_query(engine, query):
    return engine.query(query)

if __name__ == "__main__":
    main()
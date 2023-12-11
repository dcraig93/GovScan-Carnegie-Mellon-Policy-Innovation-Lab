# User Research Documentation

## Initial Prompt Received from USDS
"Can we take state plans for programs that are federally funded and state run (for example: Medicaid and child care subsidies) and make them digestible, easily searchable and actually useful to understand how 50 different states are implementing programs?

For example, states have to submit state plans to HHS (the Administration for Children and Families) to explain how they plan to implement their child care subsidy programs under ACF's regulations. These end up being PDFs of 300-400 pages that most likely contain a lot of interesting and useful information about how states are tackling different child care challenges - yet these resources are incredibly difficult to use as a policymaker because you can't easily compare across states or parse the information within. 

How might we use AI / ML tools to quickly parse these documents and create an easy-to-reference matrix that provides a snapshot of what's happening in these programs across the country?

Example from ACF based on the child care use case: https://www.acf.hhs.gov/occ/form/approved-ccdf-plans-fy-2022-2024Links to an external site. 

There is a wealth of information trapped inside these PDFs.  ACF also has a digital services team that might be willing to provide additional insight and thoughts on these are related challenges. 
Seed questions
How might we improve the usability of PDF reports for federally funded / state run programs?
How might we provide better transparency into the effectiveness of these programs?
How might we leverage technologies to build better products for decision-makers?
How might we create tools that could be easily repurposed for other, similar use cases?"


## Overview
The user research for GovScan followed HCD (Human Centered Design) principles and best practices and methods for qualitative user research. We conducted some light desktop research to understand the problem space of use cases of PDF program reports within the government. We conducted 12 interviews over the span of 2 weeks with professionals from a variety of job categories within the US State and Federal Governments, and NGOs as well as non-profit advocacy groups. As a culmination of our primary and secondary research (desktop and interviews), we came up with a user research synthesis report consisting of key findings, user personas, key insights, and most importantly - product opportunity gaps and guiding design principles. It is noteworthy to mention that before we started our user research process, we conducted some light problem area scoping to optimize our design sprints and break down the problem into a digestible focus area. We primarily focused on understanding CCDF program reports and built our initial prototype catering to those.

## User Research Protocol
We will be interviewing the stakeholders which are directly/indirectly impacted by the usability of policy reports. We are focusing on  Policy Analysts, Policy Advisors, Policy Professors, Program Specialists, Policy Lawyers. 
We will measure our research success based on the reduction of these unknowns -
1) What is the structure of the reports?
2) Who uses these reports and how frequently these reports are used/modified?
3) What tools /techniques do people currently use to extract data from these reports?
4) How much time are people currently spending on studying these reports?
5) What are the latent pain points of the different user groups?
6) What is the job that our target users are trying to get done by hiring/using these reports? (JTBD)

Tasks
* Raw data collection
* Affinity clustering of interview data to find patterns
* Synthesizing research findings to create actionable insights
* Creating visualizations of user’s mental models / concept frameworks
* Identifying early product opportunity gaps

## Interview Participant Recruitment Criteria
* Participant should have experience working within the government/public sectors, especially dealing with program reports
* Participant should be a current working professional and have a deep understanding of the domain subject
* Participant may be from a secondary stakeholder group which can help us understand technical constraints of the potential MVP
* Participant  should have a fair understanding of the cross functional channels between state and federal bodies
* Participant must be a US Citizen

## Interview Protocol
Interviewee Introduction:
“Hello! As we begin, we’d like to get to know you a little better.”
Can you please tell us a little bit about the work you do in your role?
How frequently do you have to engage with government program reports?
How long have you been working on such reports?

Body of the Interview (Deeper Level Questions):
According to you, what are the core skills one requires to understand these reports?
Have you come across any tools and techniques in recent years to analyze these reports? Do you use any of these?
How long have you been working on such reports?
What type of reports do you usually deal with on a daily basis?

General Usability:
What types of government reports do you typically encounter or use?
Can you describe your experience with using government reports?
Are there any particular reports that you find more or less usable than others? Why?

Access and Discoverability:
How do you typically find and access government reports? (e.g., websites, email subscriptions, search engines)
Have you ever encountered challenges in locating specific reports? Can you describe those challenges?

Navigation and Structure:
What do you think of the organization and structure of government reports?
Do you have any methods in place to speed up your comprehension of these vast reports?
Are there specific sections or features within reports that you find helpful or confusing?

Content and Clarity:
How would you rate the clarity of language and content in government reports on a scale of  1 to 5?
Are there any jargon or technical terms that are difficult to understand?
Do you often encounter information that is irrelevant to your needs within reports?
What are your thoughts on the formatting of government reports?

Interactivity and Accessibility:
Are government reports provided in formats that are accessible to you (e.g., PDF, web pages, plain text)?
Do you prefer any specific formats for ease of use?
Are there any interactive elements (e.g., hyperlinks, interactive tables) that you find helpful or distracting?

Suggestions for Improvement:
If you could change or improve one thing about government reports, what would it be?
Do you have any suggestions for how government reports could better meet your needs or the needs of others in your role?

Preferred Channels and Feedback:
If you have any questions/ doubts about the content of the report you’re dealing with, what steps do you take to resolve them?

Interview Closure (Wrapping Up):

Is there anything else you'd like to add or share about your experiences with government reports?

“Thanks for taking the time to speak with us today.  We really appreciate it.  Do you have any other questions for me or for any members of our team? I’d also like to ask my other team members if they have any questions they’d like to ask. Our next steps will be analyzing our notes on your feedback and thinking about how this will inform our overall approach.  We’d be happy to keep you informed of our project’s progress as we go if you would be interested.  I’m also curious if there is anyone else you would recommend we talk to. If you have any other questions, thoughts or comments later you can always reach out to me.  Thanks again for your time!”

## Refined How-Might-Wes
* How might we reduce the cognitive load on policy analysts while analyzing the reports?
* How might we aid policy analysts, advisors, researchers make decisions quickly?How might we help policy makers make better and well informed decisions?
* How might we increase transparency and connectivity between the network of stakeholders within program structures?
* How might we reduce the time it takes to find critical information from government reports?
* How might we increase the working efficiency of federal stakeholders in evaluating programs’ performances?
* How might we eliminate the need for PDF reports?
* How might we allow government report users to easily compare variations in specific parts of reports across many States?
* How might we rate the quality of different sections within a government report? 
* How might we extract specific data from government reports?
* How might we create a tool that is simple and intuitive for anyone to use? 
* How might we enable quick comparison across different reports to review good and bad reports effectively on state and federal level?
* How might we improve the feedback system between states and the federal government?
* How might we reduce workload for black and white information so that users can focus on gray areas? 
* How might we add a table of contents to reports that don’t already have one?
* How might we reduce administrative workload for government report users?
* How might we communicate the primary issues we discovered through user research? 
* How might we provide safety / potential harms / risks of any solution we develop?
 
How might we help federal policy analysts quickly find information within state CCDF plans? (Focusing on CCDF state plans for now, but will expand to other types of reports after prototyping.)

## Key Insights
* (From a Job To Be Done context) Users ‘hire’ program reports to make decisions.
* Users tend to look for specific data points while reading reports.
* There is a mismatch in the existing mental models of two user groups - ones who create reports and ones who consume them.
* At times the reports are generated at different points in time which makes recency of the report relative and hard to compare.
* Federal government is now focusing on data rather than reports.
* Users don’t always know what they’re looking for in a report.
* There is a wall of opacity between report generators and consumers which the consumers try to overcome by leveraging personal networks.


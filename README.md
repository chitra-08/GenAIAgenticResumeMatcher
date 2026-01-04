# GenAIAgenticResumeMatcher

This is an Agentic Resume Matcher which ingests the jobs available in the market and store them as embeddings in Vector database.
User uploads his resume and the call goes to find the jobs which in turn calls the agent which has a search job tool agent which will use the embeddings.
The agent is instructed to call the search tool multiple times in order to refine the job search result which suits the resume uploaded by the user.
At the end, user is not only provided with the link but a structured response which provides details about the closely related job url, the score, strength and weakness.


# Steps to run the project
1. Run the ingestion.py file first to scrape the job search URL and store the embeddings in the vector db. (Need to run only once if the search URL is not getting changed) 
2. Run the main.py which will call find jobs method responsible to read the file sent via upload file from UI, loads the agent and construct Multimodal Message to be passed as content.
3. Run the streamlit_app.py to run the UI and upload the resume.

<img width="2354" height="1213" alt="image" src="https://github.com/user-attachments/assets/928ec8ad-ec72-4bb2-b48e-2da34443e537" />
<img width="2354" height="1213" alt="image" src="https://github.com/user-attachments/assets/1ccee91f-36f8-4ba8-942a-a190a8b46ac4" />

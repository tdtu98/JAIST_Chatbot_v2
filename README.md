# JAIST_Chatbot_v2
<p align="center"> 
  <img src="https://github.com/tdtu98/JAIST_Chatbot_v2/blob/main/images/demo.gif" alt="drawing" style="width:80%;"/>
</p>
This the the next version of my chatbot following RAG method. Our features includes:

- Signup and login.
- RAG system with Langchain and ChatGPT-3.5 API.
- User data and chat histories storage with Mongodb.
- Chat streaming with Fastapi and chain method astream_event.
- Containerization with Docker.

## RAG
<p align="center"> 
  <img src="https://github.com/tdtu98/JAIST_Chatbot_v2/blob/main/images/RAG.png" alt="drawing" style="width:90%;"/>
</p>
The basic idea of our RAG system is using a chat memory to re-generate the input question. For example in our demo, since the previous question is about JAIST, the new generated question is likely to be "What does JAIST stand for?". The rest of our RAG basically follows the standard stucture containing different components: embeddings, LLM, vectorstore, prompts.

## Usage
Please pull this respository and using the docker command:
```
docker-compose -f docker-compose.yml up
```
You also need to create an .env file to store your openai api key and the mongodb username=admin together with password=secret.
To access the website, please connect to localhost:80. If you want to check the database, please connect to localhost:8081

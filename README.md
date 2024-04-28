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

The basic idea of our RAG system is using a chat memory to re-generate the input question. For example in our demo, since the previous question is ```Where is JAIST?``` and the next input question is ```What does its name stand for?```, the new generated question is likely to be ```What does JAIST stand for?```. The rest of our RAG basically follows the standard stucture containing different components: embeddings, LLM, vectorstore, prompts.

## Usage
After pulling this respository, create a ```.env``` file following my [```.env.local file``` ](https://github.com/tdtu98/JAIST_Chatbot_v2/blob/main/app/.env.local) to store your environment variables such as ```OPENAI_API_KEY```.
Compose the docker image using this commnad:
```
docker-compose -f docker-compose.yml up
```
After successfully creating the docker containers ```mongo```, ```mongo-express```, and ```jaist_chatbot```, you can use the web browser to connect to our app locally at ```localhost:80``` or visually view the database at ```localhost:8081```

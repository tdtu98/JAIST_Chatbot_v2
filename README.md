# JAIST_Chatbot_v2
This the the next version of my chatbot following RAG method. Instead of using streamlit, I implemented the backend with fastapi. The new features like login and signup with username and password are also implemented. The chat history and user's information are stored in mongodb. We can monitor the mongodb using mongo express. I also containerized all components for future deployment or testing.
<p align="center"> 
  <img src="https://github.com/tdtu98/JAIST_Chatbot_v2/blob/main/images/login.png" alt="drawing" style="width:80%;"/>
  <img src="https://github.com/tdtu98/JAIST_Chatbot_v2/blob/main/images/chat.png" alt="drawing" style="width:80%;"/>
</p>

## Usage
Please pull this respository and using the docker command:
```
docker-compose -f docker-compose.yml up
```
You also need to create an .env file to store your openai api key and the mongodb username=admin together with password=secret.
To access the website, please connect to localhost:80. If you want to check the database, please connect to localhost:8081

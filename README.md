# Video Chatter

This app summarizes YouTube videos and makes them conversational.

### The Architecture

![Video Chat Architecture](video-chat-arch.png)

1. A user enters a YouTube video URL to summarize.
2. The Streamlit app takes the URL, parses it to get the video ID, and calls the YouTube API to get the video transcript.
3. The app builds a prompt from the transcript and passes it to Bedrock for summarization using a predefined model.
4. Bedrock summarizes the transcript based on the generated prompt and returns the summary to the user.
5. If users have follow-up questions, the app builds a conversation memory using Langchain and answers follow-up questions based on content from the original transcript.

### Installation

1. **Clone the repo**
   ```sh
   git clone https://github.com/ekhiyami/video-chat.git

2. **Move to root directory**
   ```sh
   cd video-chat

3. **Install requirements**
   ```sh
   pip install -r requirements.txt

>The code as is works on Streamlit. If you like to change it to work on your local environment, follow steps 4, 5, and 6. Otherwise, jump directly to step 7.

 4. **Create .aws folder in the roots**

 5.**Move to .aws directory**  
      ```sh
      cd .aws
 6. **Create credentials.ini file and add AWS credentials in the file**
      ```sh
      ACCESS_KEY=<Your AWS access key>
      SECRET_KEY=<Your AWS secret access key>

 7. **Change lines 23 and 24 in bedrock.py to read the secrets from your local environment**
      ```sh
      ACCESS_KEY = os.getenv("ACCESS_KEY")
      SECRET_KEY = os.getenv("SECRET_KEY")

 8. d**From root folder, run the following command to run the application in the browser**
      ```sh
      streamlit run app.py





1. **Change lines 23 and 24 in bedrock.py to read the secrets from your local environment** 
   ```sh
   ACCESS_KEY=<Your AWS access key>
SECRET_KEY=<Your AWS secret access key>

1. **From root folder, run the following command to run the application in the browser**
   ```sh


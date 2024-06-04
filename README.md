# Video Chatter

## Name

Video Chatter

## Description

I summarize Youtube videos and make them conversational 

## Installation

Steps to install the application

1. Clone the repo
   ```sh
   git clone git@gitlab.com:subinvs/chatbot.git
   ```
2. Move to root directory
   ```sh
   cd chatbot
   ```
3. Install packages
   ```sh
   pip install -r reuirements.txt
   ```
4. Create .aws folder in the root
5. Move to .aws directory
   ```sh
   cd .aws
   ```
6. Create credentials.ini file and add AWS credentials in the file
   ```sh
   [default]
   aws_access_key_id=<Access key>
   aws_secret_access_key=<Secret access key>
   ```
7. From root folder run the following command to run the application in browser
   ```sh
   streamlit run app.py
   ```

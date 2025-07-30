# Chatbot

 Voice-Enabled Mental Health Chatbot using Streamlit & Google Gemini

 Project Overview

Mental health is an increasingly important topic in today’s fast-paced world. Many individuals seek a safe and judgment-free space to express their emotions, even if only to a non-human listener. This project, Voice Mental Health Chatbot, aims to bridge that need through technology — providing a kind, always-available chatbot that listens to users either through voice or text and responds empathetically.

This chatbot is not a substitute for professional mental health services, but it offers a supportive environment to help users feel heard and acknowledged.


 Objectives

The primary goals of this project include:

* Enabling a low-barrier entry to emotional expression via voice or text.

* Using Google Gemini’s advanced generative AI (Gemini 1.5 Flash) to craft empathetic, natural responses.

* Delivering an interactive web app using Streamlit that is easy to deploy, run, and use.

* Highlighting how AI can augment mental wellness support tools without replacing human professionals.

Technology Stack

Python: Core programming language for backend logic.

* Streamlit: Lightweight Python library for building web apps, used to design the user interface.

* Google Generative AI (Gemini 1.5 Flash): API used for generating contextual, human-like chatbot responses.

* SpeechRecognition + PyAudio: For converting user voice input into text that can be processed by the chatbot.

 Project Structure

voice-mental-health-chatbot/
├── app.py              
└── requirements.txt 

How It Works

User Interface:
1. Streamlit provides a simple UI with a text input field and a button to speak through the microphone.

2. Voice Input Handling:
When the user clicks the " Speak Now" button, the app activates the microphone and listens for speech using speech_recognition. It converts the spoken input into text and displays it to the user.

3. AI Response Generation:
Both spoken and typed user inputs are sent to Google’s Gemini API with a custom prompt instructing it to be supportive, kind, and understanding. The AI responds accordingly.

4. Chat Display:
The conversation is stored in a session state and rendered in a chat-like format, alternating between user and bot responses.

5. Disclaimer:
At the bottom, the app reminds users that it is a support tool only — not a licensed mental health service.

 Installation and Setup Guide

 1. Clone the Repository:
    git clone .git
   cd voice-mental-health-chatbot

 2. Install Dependencies
     pip install -r requirements.txt

   On Windows, if PyAudio fails:

    pip install pipwin
    pipwin install pyaudio

 3. Add Your Gemini API Key
      Edit app.py:
     genai.configure(api_key="YOUR_API_KEY_HERE")

 4.  Run the Application

     streamlit run app.py

   Then go to http://localhost:8501/ in your browser.     

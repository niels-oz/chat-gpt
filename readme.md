# Langchain Ask PDF (Tutorial)

>You may find the step-by-step video tutorial to build this application [on Youtube](https://youtu.be/wUAUdEw5oxM).

This is a Python application that allows you to load a PDF and ask questions about it using natural language. The application uses a LLM to generate a response about your PDF. The LLM will not answer questions unrelated to the document.

## How it works

The application reads the PDF and splits the text into smaller chunks that can be then fed into a LLM. It uses OpenAI embeddings to create vector representations of the chunks. The application then finds the chunks that are semantically similar to the question that the user asked and feeds those chunks to the LLM to generate a response.

The application uses Streamlit to create the GUI and Langchain to deal with the LLM.


## Installation

To install the repository, please clone this repository, create a virtual environment and install the requirements:

```
git clone https://github.com/niels-oz/chat-gpt.git
mkdir -p venv
cd chat-gpt
python3 -m venv ../venv/chat-gpt
source ../venv/chat-gpt/bin/activate
pip install -r requirements.txt
```

To create an openAI API key goto https://platform.openai.com/account/api-keys. 
Create a `.env` file. And add your OpenAI API key to it.

## Usage

To use the application, run the `app.py` file with the streamlit CLI (after having installed streamlit): 

```
streamlit run app.py
```




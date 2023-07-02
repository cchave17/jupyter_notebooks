# README

## Overview

This repository contains a Jupyter notebook that showcases how to use the OpenAI's GPT-4, a large language model, for different tasks such as text generation and creating a chatbot. It uses the LangChain library for interaction with the OpenAI API and the Pinecone service for vector indexing.

## Installation

Before running the notebook, make sure you have Python 3.8+ installed. To install the necessary dependencies, run:

```bash
pip install -r requirements.txt
```

This command will install the following packages as per the provided requirements.txt:

- python-dotenv==1.0.0
- langchain==0.0.220
- pinecone-client==2.2.1
- openai

## Setup
You need to create a `.env` file in the root directory of this project and add the following variables:

```bash
OPENAI_API_KEY=""
PINECONE_ENV=""
PINECONE_API_KEY=""
```
Replace the empty quotes `""` with your own API keys and environment details. This `.env` file will be used to securely load the environment variables necessary for the notebook to interact with the OpenAI and Pinecone APIs.

**Note:** Do not expose these keys publicly and ensure that the `.env` file is listed in your `.gitignore` file to prevent it from being committed to version control.

## Usage

Once the setup is done, start your Jupyter notebook server by running:

```bash
jupyter notebook
```

Then open the notebook and run the cells in order. Here's a brief explanation of what each cell does:

- **Cell 1**: Imports the necessary function from `dotenv` and loads the environment variables from the `.env` file.
- **Cell 2**: Initializes an instance of `OpenAI` from the `langchain.llms` module and uses it to generate text.
- **Cell 3**: Imports the required classes from `langchain.schema` and `langchain.chat_models`.
- **Cell 4**: Initializes a `ChatOpenAI` instance with specific parameters and generates a chat response based on a sequence of messages.
- **Cell 5**: Prints the content of the chat response.


# obama_agent
# Obama Tweet Agent

# Description
This AI agent analyzes news articles from The New York Times and generates opinions based on the tweets of President Barack Obama between 2009-2017. It utilizes natural language processing techniques to find relevant tweets and then leverages a large language model (GPT-4o-Mini) to craft opinions in Obama's style.

# How it Works
# Data Acquisition:

Fetches the latest news articles from The New York Times' World News RSS feed.
Loads a dataset of Barack Obama's tweets from a CSV file (tweets.csv).
Tweet Embedding and Indexing:

Uses OpenAI's Embeddings API to generate vector representations (embeddings) of Obama's tweets.
Stores these embeddings in a ChromaDB vector database for efficient similarity search.
News Analysis and Opinion Generation:

For each news article:
Extracts the title and summary.
Searches the tweet database for relevant tweets based on similarity to the news title.
Constructs a prompt for GPT-4o-Mini, including the news article and the relevant tweets.
Generates an opinion using GPT-4o-Mini, mimicking Barack Obama's style.
User Interface:

Presents the generated opinions through a user-friendly interface built with Gradio.

# Requirements
Python 3.7 or higher
Required Libraries:
!pip install openai feedparser tiktoken langchain-community pandas chromadb langchain openai gradio 

OpenAI API Key: You'll need an OpenAI API key for accessing the Embeddings API and GPT-4o-Mini. Store your API key in Google Colab's Secrets as 'quiqueapi'.

# Usage
Prepare the Data:
Place the tweets.csv file containing Obama's tweets in the /content directory of your Google Colab environment.
Run the Code:
Execute the Python code in a Jupyter notebook or Google Colab environment.
Interact with the Interface:
A Gradio interface will launch in a new browser tab. Click the "Run" button to generate opinions on recent news articles.

# Disclaimer
This project is for educational and entertainment purposes only.
The generated opinions are based on AI interpretations of Barack Obama's tweets and may not accurately reflect his views.
The accuracy and reliability of the generated content depend on the quality of the input data and the capabilities of the AI models.

# Data Source
Barack Obama's tweets: https://www.obamalibrary.gov/digital-research-room/archived-white-house-websites-and-social-media#socialmedia
New York Times World News RSS feed: [[redacted link]
](https://rss.nytimes.com/services/xml/rss/nyt/World.xml)

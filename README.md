#Reddit Post Retrieval Automation

Overview

This repository contains an n8n workflow designed to automate the retrieval of Reddit user metadata and generate targeted sales pitches for Myntra products. The workflow processes user input to identify topics, extracts relevant keywords, fetches related subreddits and posts using SerpAPI and Reddit tools, and creates a customized sales pitch based on post content.

Workflow Structure

The workflow consists of multiple nodes, including:





AI Agents: Powered by Groq language models (LLaMA-3.1-8B, Gemma2-9B, and OpenAI GPT-OSS-20B) for processing and extracting information.



SerpAPI Tool: Used to search for relevant subreddits and Myntra products.



Reddit Tools: Fetch subreddit names and posts, filtered by category (e.g., "new").



Information Extractors: Parse subreddit names and other relevant data from AI outputs.



Memory Buffers: Maintain context across interactions with a defined context window.



Chat Trigger: Initiates the workflow upon receiving a chat message.

Functionality





Input Processing: Accepts a user-defined topic and generates keywords for Reddit searches.



Subreddit Discovery: Uses SerpAPI and Reddit tools to identify two relevant, non-redundant subreddits.



Post Retrieval: Fetches posts from identified subreddits, focusing on recent content.



Sales Pitch Generation: Analyzes post content (e.g., user requirements in selftext) and uses SerpAPI to find matching Myntra products, crafting a tailored sales pitch.



Error Handling: Configured to ignore tool execution errors and proceed with available data.

Dependencies





n8n: Workflow automation platform.



Groq API: For AI language model processing.



SerpAPI: For search functionality.



Reddit OAuth2 API: For accessing Reddit data.

Setup






License

This project is licensed under the MIT License.

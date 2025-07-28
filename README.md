Customer Support Chatbot 
This notebook demonstrates building a customer support chatbot using LangGraph and Google's Gemini model. The chatbot is designed to assist users with travel-related queries, specifically focusing on flight information, hotel bookings, car rentals, and trip recommendations.

Features
Flight Information: Users can inquire about their existing flight details.
Flight Updates and Cancellations: The chatbot can delegate tasks to a specialized assistant to handle flight changes and cancellations (requires user approval for sensitive operations).
Hotel Booking: Users can search for and book hotels through a dedicated assistant.
Car Rental: Users can search for and book car rentals through a dedicated assistant.
Trip Recommendations: The chatbot can provide trip recommendations and book excursions.
Policy Lookup: The chatbot can consult company policies to answer user questions.
Modular Design: The application is built with LangGraph, allowing for a clear definition of different assistant roles and transitions between them.
Tool Usage: The chatbot leverages various tools (functions) to interact with a simulated travel database and external services (like Tavily search).
Technologies Used
LangGraph: For building stateful, multi-actor applications with LLMs.
LangChain: Provides abstractions for working with language models and tools.
Google Gemini: The large language model used for generating responses and understanding user intent.
SQLite: A simple database used to store travel information (flights, hotels, car rentals, trip recommendations).
Tavily Search: Used for searching external information (example: weather).
Sentence Transformers: For generating embeddings for policy lookup.
Setup
Clone the repository:
Install dependencies:

It's recommended to create a virtual environment before installing dependencies.

pip install -r requirements.txt

Set up environment variables:

You will need API keys for Google Gemini and Tavily. Store these securely and make them available as environment variables. In Google Colab, you can use the Secrets Manager.

GOOGLE_API_KEY
TAVILY_API_KEY
HUGGINGFACEHUB_API_TOKEN (if using Hugging Face embeddings, though this notebook uses sentence_transformers)
LANGCHAIN_API_KEY (for LangSmith tracing)
Project Structure
The notebook is structured as follows:

Setup and Dependencies: Installs necessary libraries and sets up environment variables.
Database Setup: Downloads and prepares a SQLite database for travel information.
Tool Definitions: Defines various tools (Python functions) that the chatbot can use to interact with the database and external services (e.g., searching flights, booking hotels, looking up policies).
Assistant Definitions: Defines different assistant roles (primary assistant and specialized assistants for flights, hotels, car rentals, and excursions) and their prompts.
LangGraph Setup: Builds the state graph using LangGraph, defining the states, nodes, and edges that represent the conversation flow and transitions between assistants and tools.
Running the Chatbot: Demonstrates how to run the chatbot with a sample conversation and how to handle user interactions and sensitive operations.
How to Use
Follow the setup steps to install dependencies and set up environment variables.
Run the cells in the notebook sequentially.
Interact with the chatbot by providing user queries in the designated input cells.
Approve or deny sensitive operations when prompted.
Extending the Chatbot
Add more tools: Create new Python functions that interact with other services or data sources to expand the chatbot's capabilities.
Add more specialized assistants: Define new assistant roles and prompts to handle specific types of user queries.
Improve routing: Enhance the logic for routing between assistants based on user intent.
Integrate with other LLMs: Experiment with different language models.

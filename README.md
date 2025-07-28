🚀 Just Built a Modular Customer Support Chatbot for Travel Industry
Leveraging LangGraph, Google Gemini & Multi-Agent Design

Project Overview
Developed a stateful chatbot that handles complex travel queries through specialized AI agents:
✈️ Flight info, updates & cancellations
🏨 Hotel bookings & recommendations
🚗 Car rental reservations
🗺️ Trip planning & excursion booking
📑 Policy lookup via semantic search

Key Technical Features
✅ Multi-Agent Orchestration with LangGraph
✅ Secure Sensitive Operations (user approval workflow)
✅ Hybrid Data Retrieval: SQL + Vector Search (Sentence Transformers)
✅ External API Integration (Tavily for real-time data)
✅ Modular Tool Design for easy extensibility

Tech Stack
• LLM: Google Gemini
• Framework: LangChain + LangGraph
• Database: SQLite
• Search: Tavily + Sentence Transformers
• Infra: Python, FastAPI (implied)

Setup in 3 Steps

git clone [repo_url]

pip install -r requirements.txt

Set env vars:
GOOGLE_API_KEY, TAVILY_API_KEY

Extendable Design Opportunities
• Add payment processing agents 💳
• Integrate voice interface (ASR/TTS) 🎤
• Implement real-flight API connections 🌐
• Add multi-language support 🌍

See it in action?
Sample conversation:

User: "Help! My LAX-SFO flight got canceled"
Bot:

Retrieves booking details

Suggests alternatives via flight agent

Requests approval for rebooking

Confirms new itinerary


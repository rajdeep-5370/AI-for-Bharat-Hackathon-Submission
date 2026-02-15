# JanSahayak AI: The Intelligent Scheme Information Hub 🇮🇳
### Bridging the gap between Government Policy and Citizen Reality

![Architecture Diagram](Architecture.jpeg)

## 🚨 The Problem
While the government releases thousands of beneficial schemes, the intended beneficiaries (Farmers, Students, Rural Citizens) often miss out due to:
* [cite_start]**Information Overload:** Too many irrelevant schemes to sift through[cite: 28].
* [cite_start]**Complexity Barrier:** Official documents use bureaucratic economic terms (e.g., "fiscal allocation") that are hard to understand[cite: 39].
* [cite_start]**Lack of Context:** A generic search doesn't tell a farmer *how* a specific subsidy impacts their daily income[cite: 35].

## 💡 The Solution
**JanSahayak AI** is not just a chatbot; it is a **Context-Aware Information Router**. [cite_start]It filters the massive universe of government data based on who the user is (Identity-Aware) and translates complex policies into simple, relatable analogies (Complexity Reduction)[cite: 41, 46, 48].

## ✨ Key Features
* [cite_start]**🎭 Persona-Based Filtering:** Automatically detects if the user is a **Student** or **Farmer** and filters noise, showing only relevant schemes[cite: 63, 46].
* [cite_start]**🧠 RAG-Powered Explanations:** Uses Retrieval-Augmented Generation to fetch official guidelines and explain them in "plain English" or local languages[cite: 20, 73].
* [cite_start]**🗣️ Multilingual Support:** Accepts queries in Hindi/Regional languages and breaks down barriers[cite: 19].
* [cite_start]**🔔 Proactive Notifications:** Alerts users about deadlines and new relevant updates before they even ask[cite: 93].
* [cite_start]**👶 "Explain Like I'm 5":** A unique toggle to switch between detailed official text and simplified analogies[cite: 88].

## 🛠️ Tech Stack
* [cite_start]**Frontend:** Next.js (React) [cite: 103]
* [cite_start]**Backend & Database:** Supabase (Auth & PostgreSQL) [cite: 104]
* [cite_start]**AI Engine:** OpenAI / Claude API (LLM) + Supabase Vector Store (pgvector) [cite: 105]

## 📸 System Architecture & Flow
The system uses a **Context-Aware Router** to verify user identity before querying the vector database, ensuring high relevance and low hallucination.

**User Journey:**
![User Flow Diagram](Flowdiagram.png)

## 🚀 Future Roadmap
* [cite_start]Expansion to new personas: Women Entrepreneurs, Senior Citizens, and MSMEs[cite: 123].
* [cite_start]Voice-first interface for complete accessibility in rural areas[cite: 51].
* Integration with direct application portals (API-based form filling).

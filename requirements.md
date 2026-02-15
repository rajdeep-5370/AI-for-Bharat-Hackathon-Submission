# Project Name: JanSahayak AI (Local Government Scheme Helpline)

## 1. Problem Statement
While the internet is filled with information about government schemes, it suffers from an "accessibility vs. comprehensibility" gap.
* **Information Overload:** Rural citizens cannot filter through hundreds of irrelevant schemes.
* **Literacy & Context Barrier:** Official documents use bureaucratic economic terms (e.g., "fiscal allocation," "subsidy amortization") that are unintelligible to the target beneficiaries.
* **Fragmentation:** Data is scattered across various portals without a unified interface for specific user needs.

## 2. Proposed Solution
**JanSahayak AI** is a "Scheme Information Hub" that acts as an intelligent intermediary between government data and citizens. It does not just retrieve information; it translates context.
* **Identity-Aware Filtering:** Automatically filters the information universe based on the user's role (e.g., Student vs. Farmer).
* **Complexity Reduction:** Uses GenAI (RAG) to translate official guidelines into simple, relatable analogies (e.g., explaining MSP in terms of crop prices, or scholarships in terms of semester fees).
* **Multilingual Support:** Accepts queries in Hindi/Regional languages and provides understandable answers.

## 3. Target User Personas (MVP)
### Persona A: The Student
* **Needs:** Scholarship updates, research grants, internship opportunities, exam-related government news.
* **Pain Point:** Confused by eligibility criteria and complex application procedures.
* **Goal:** "How can I fund my final year engineering project?"

### Persona B: The Farmer
* **Needs:** Agricultural subsidies, fertilizer rates, MSP updates, loan waivers, crop insurance.
* **Pain Point:** Cannot read complex PDFs; needs voice interaction or simple local language text.
* **Goal:** "What is the new government rate for my wheat crop?"

## 4. Functional Requirements
### Core Modules
1.  **User Onboarding & Persona Detection:**
    * System must collect basic info (Age, Location, Occupation) to classify the user.
    * System must route queries through a "Context-Aware Router" (as per architecture).
2.  **Scheme Matching Engine:**
    * Database of 10-15 active schemes (split between Education & Agriculture).
    * Semantic search to match user profile to eligible schemes.
3.  **RAG-Based Explanation Layer:**
    * **Input:** Official Government PDFs/Circulars.
    * **Process:** Retrieve relevant chunks -> LLM Simplification.
    * **Output:** "Explain Like I'm 5" summaries and detailed breakdowns.
4.  **Interactive Query Interface:**
    * Web-based Chatbot (Text/Voice support).
    * Quick Action buttons (e.g., "Show Eligible Schemes," "Explain Simply").
5.  **Proactive Notification System:**
    * Alert users about deadlines or new relevant schemes based on their profile.

## 5. Non-Functional Requirements
* **Accuracy:** Responses must be grounded in official documents (Zero hallucination policy).
* **Latency:** Explanations generated within <3 seconds.
* **Accessibility:** Interface must be simple enough for low-digital-literacy users.
* **Scalability:** Architecture must support adding new personas (e.g., Women Entrepreneurs, Senior Citizens) without code changes.

# System Design: JanSahayak AI

## 1. High-Level Architecture
The system follows a Retrieval-Augmented Generation (RAG) pipeline to ensure accuracy and context.

### A. Input Layer
* **Web Portal:** A Next.js frontend interface supporting both text and voice input.
* **User Query:** Captures natural language questions in Hindi/English.

### B. Processing Layer (The Gatekeeper)
* **Authentication:** OTP/ID based login via Supabase Auth.
* **Identity Detection:** Classifies user into `Student` or `Farmer` roles.
* **Context-Aware Router:** Directs the query to the specific knowledge base relevant to the user's persona (filtering out noise).

### C. RAG Engine (The Brain)
* **Document Sources:** Ingests Circulars, Government PDFs, Scheme Guidelines, and Application Forms.
* **Vector Database:** Supabase (pgvector) stores embeddings of these documents.
* **Semantic Search:** Performs cosine similarity search to find the exact paragraph in a government PDF that answers the user's specific question.

### D. Response Layer (The Translator)
* **LLM (Generative AI):** Uses OpenAI/Claude API.
* **Prompt Engineering:**
    * *System Prompt:* "You are a helpful assistant. Explain this government scheme to a [Farmer] using analogies related to crops/village economy."
* **Output:**
    * **Language Simplification:** Converts bureaucratic text to simple language.
    * **Voice Output:** (Optional) Text-to-Speech for accessibility.

## 2. User Flow (UX Strategy)
1.  **Onboarding:** User enters basic details -> System assigns "Persona Tag".
2.  **Discovery:** User sees a dashboard of "Schemes for You" (Proactive) OR asks a question (Reactive).
3.  **Processing:**
    * *If Eligible:* Show scheme details + "Apply Link".
    * *If Confused:* User clicks "Explain Simply" -> AI generates analogy.
4.  **Engagement:** User opts-in for deadline reminders via WhatsApp/SMS.

## 3. Technology Stack
* **Frontend:** Next.js (React) - For a responsive, fast web interface.
* **Backend & Database:** Supabase - Handles Auth, PostgreSQL database, and Vector storage for RAG.
* **AI/LLM:** OpenAI API (GPT-4o or similar) or Anthropic Claude - For summarization and translation.
* **Search:** Semantic Search (Embeddings) to retrieve relevant scheme info.
* **Integration:** Twilio API (for WhatsApp integration demo).

## 4. Data Schema (MVP)
* `Users`: id, role (student/farmer), location, language_pref.
* `Schemes`: id, title, category, eligibility_criteria, official_pdf_link.
* `Scheme_Embeddings`: vector_data (for AI search).
* `Updates`: id, scheme_id, news_text, date.

## 5. Security & Privacy
* User data is encrypted.
* AI is restricted to "Read Only" access of government data to prevent misinformation.

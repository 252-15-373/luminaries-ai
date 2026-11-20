# ✦ Luminaries — AI Study Operating System (LearnSphere AI)

> **Built for the International AI Builders Congress 2026**  
> **Team:** Team Luminaries | **Domain:** University Education (LearnSphere AI)

**Luminaries** is a unified, privacy-first AI Study Operating System designed for university students. It combines a Socratic AI Tutor, a client-side RAG (Retrieval-Augmented Generation) Knowledge Base synced directly with course materials, academic writing and research labs, and 8 specialized study utility tools in a single zero-friction web application.

---

## 🔗 Live Deployment & Quick Judge Access

- **Live Web App:** [https://252-15-373.github.io/luminaries-ai/](https://252-15-373.github.io/luminaries-ai/)
- **Login / Guest Entry:** [https://252-15-373.github.io/luminaries-ai/login.html](https://252-15-373.github.io/luminaries-ai/login.html)
- **Instant Access:** Click **"Continue as Guest →"** on the entry screen to explore the full workspace immediately with pre-loaded university study materials—no account creation or API key required.

---

## 🎯 Problem Statement
University students rely on scattered, generic chatbots that often hallucinate academic citations, dump raw homework answers without teaching underlying concepts, struggle with bilingual (English/Bengali/Banglish) technical queries, and have no connection to a student's actual course syllabus or lecture notes.

---

## 🚀 Key Features

### 1. Core AI Workspaces
- **Chat (Socratic AI Tutor):** Explains concepts step-by-step, supports English, Bengali, and Banglish (preserving technical terminology in English), and includes a live **`📚 RAG: ON/OFF`** toggle.
- **Create Studio:** Structured generator for lab reports, project proposals, study notes, and professional academic emails.
- **Research Lab:** Deep topic analysis, concept comparisons, and exam prep with a strict **Zero-Hallucination Citation Policy**.

### 2. Automated GitHub-to-Browser RAG Engine & Library
- Automatically syncs `.pdf`, `.txt`, `.md`, `.json`, and `.csv` study files from the repository's `/study-materials` folder into the browser's Knowledge Base.
- Supports in-browser **PDF.js** text extraction for uploaded lecture slides.
- Retrieves relevant study chunks before querying the LLM and displays a transparent **`📚 Grounded in Knowledge Base`** source badge on grounded answers.

### 3. Tools Hub (8 Specialized Study Utilities)
1. **PDF Summarizer** (Real in-browser PDF.js extraction + AI summary)
2. **Writing Assistant** (AI rewrite + Instant Local Grammar Engine)
3. **Code Debugger** (Multi-language root-cause analysis + complexity review)
4. **Translator** (Preserves English technical terms in Bengali translations)
5. **Text Summarizer** (Exam revision sheets & bullet takeaways)
6. **Quiz & Flashcard Maker** (Active-recall MCQs & Q&A flashcards)
7. **JSON Converter** (Deterministic local JSON/Markdown formatter + AI structuring)
8. **Math Helper** (Instant local arithmetic/quadratic solver + AI step-by-step proofs)

---

## 🛡️ Ethical AI & Security Safeguards
- **Academic Integrity (Socratic Guardrails):** System prompts instruct the tutor to teach intuition and step-by-step reasoning first, ending with an active-recall check instead of enabling blind copy-paste cheating.
- **Anti-Hallucination Policy:** Research Lab explicitly refuses to fabricate paper titles, authors, or fake URLs, suggesting verifiable Google Scholar / IEEE Xplore search terms instead.
- **Zero-Key Client Security:** No private API keys are ever stored in `localStorage` or exposed in frontend source code. The Model Config panel supports connecting a secure FastAPI backend proxy (`.env`-managed keys) while maintaining a live keyless public AI fallback for zero-friction evaluation.
- **Privacy-First Local Storage:** Student chats, notes, and uploaded files remain locally in the user's browser.

---

## 🏗️ Technical Architecture
- **Frontend:** Vanilla HTML5, CSS3 (Adaptive Dark/Light Theme, Collapsible Dual-Panel Flexbox Shell), and Modular ES6 JavaScript—zero build-step overhead, instant edge delivery on GitHub Pages.
- **Document Parsing:** Mozilla `PDF.js` with a native binary PDF stream fallback parser.
- **Retrieval Layer:** Client-side keyword-weighted scoring engine (`retrieveLibraryContext`) indexing both user-uploaded documents and `/study-materials` repository files.
- **Backend Proxy Ready:** Configurable FastAPI `/api/chat` and `/api/health` integration inside **Settings → Model Config** for seamless transition to enterprise OpenAI/Gemini endpoints.

---

## 💼 Business Model & Global Readiness
- **B2C Freemium (Students):** Free core study OS, local tools, and personal notes; low-cost student Pro tier for cloud sync, unlimited PDF OCR, and premium reasoning models.
- **B2B Institutional Licensing (Universities & Departments):** Department-hosted Knowledge Bases where faculty upload verified syllabi and lab manuals so students get 24/7 course-grounded tutoring.
- **Cross-Border Adaptability:** Designed in Bangladesh with native bilingual technical support, easily adaptable to any university curriculum or language globally.

---

## 📈 Scalability Roadmap
1. **Phase 1 (Current — Live):** Edge-hosted static Study OS on GitHub Pages with in-browser RAG and zero infrastructure cost.
2. **Phase 2 (Campus Pilot):** Connect the built-in FastAPI proxy endpoint to a managed Vector Database (PostgreSQL + `pgvector`) for multi-course semantic search and student authentication.
3. **Phase 3 (Global Scale):** LMS integrations (Moodle, Google Classroom, Canvas) with faculty analytics dashboards and institutional SSO.

---

## 📂 Repository Structure
```text
luminaries-ai/
├── index.html           # Main AI Study OS (Workspaces, 8 Tools, RAG Engine, Settings)
├── login.html           # Entry interface with Quick Guest Access & Email Login/Signup
├── study-materials/     # Course notes & PDFs auto-indexed by the in-browser RAG engine
└── README.md            # Project documentation

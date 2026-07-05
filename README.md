# AtomMail — AI Email Assistant with RAG, OCR, and Personalized Reply Generation

**Hackfest project | 2nd Prize**

AtomMail is an AI-powered email assistant that helps users understand, search, and respond to email faster. It combines retrieval-augmented generation, OCR over attachments/screenshots, user-history retrieval, and LLM-based response drafting.

## Problem

Email replies are slow because useful context is scattered across:

- old emails
- attachments
- screenshots
- previous user tone/style
- long email threads
- task-specific details

AtomMail turns that scattered context into a personalized response assistant.

## What I built

- RAG pipeline for retrieving relevant past email context.
- OCR ingestion for extracting text from images and scanned documents.
- LLM response generation for context-aware email drafts.
- User-history adaptation so replies match the user's past communication style.
- Flask/Python backend for inference and orchestration.
- MongoDB-backed storage for user context and retrieval.
- Frontend flow for interacting with email content and generated replies.

## Impact

- Reduced time taken to reply to emails by approximately **80%** in the hackathon workflow.
- Won **2nd Prize** at Hackfest for the AtomMail project.

## Tech stack

| Layer | Tools |
|---|---|
| Backend | Python, Flask |
| AI / LLM | LangChain, HuggingFace, Gemini APIs |
| Retrieval | RAG pipeline, vector-style context retrieval |
| OCR | Tesseract OCR |
| Database | MongoDB |
| Frontend | JavaScript, HTML, CSS |
| Use case | Gmail/email productivity assistant |

## Architecture

```text
Email / thread / attachment
        ↓
Preprocessing
        ↓
OCR extraction for image/PDF-like inputs
        ↓
Context chunking and storage
        ↓
User-history retrieval
        ↓
RAG context assembly
        ↓
LLM draft generation
        ↓
Personalized email response
```

## Core features

### 1. Context-aware reply generation

AtomMail uses the current email plus retrieved historical context to produce replies that are specific to the conversation instead of generic.

### 2. OCR-based context extraction

Attachments, screenshots, or scanned text can be processed using OCR so that useful hidden context is available to the model.

### 3. Personalized tone adaptation

The system uses user history to adapt response style, tone, and wording patterns.

### 4. Retrieval-augmented generation

Relevant past context is retrieved before generating a reply, reducing hallucination and improving usefulness.

## Suggested local setup

Update this section after verifying exact commands in the repo.

```bash
git clone https://github.com/Arush777/my-hackfest-atom-mail.git
cd my-hackfest-atom-mail
```

### Backend

```bash
cd gmail
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

### Frontend

```bash
npm install
npm run dev
```

## Environment variables

Create a `.env` file and add the required keys:

```bash
GEMINI_API_KEY=
MONGO_URI=
GMAIL_CLIENT_ID=
GMAIL_CLIENT_SECRET=
```

Do not commit real credentials.

## Demo checklist

Add these artifacts to make the repo much stronger:

- hackathon certificate link
- 60-second demo video
- UI screenshots
- sample email → generated reply example
- architecture diagram
- setup screenshots
- limitations section

## Repository cleanup checklist

- Add `.env.example`
- Add `requirements.txt`
- Add setup instructions tested from a clean clone
- Add screenshots under `assets/`
- Add a `docs/architecture.md`
- Add a short demo GIF to the top of this README

## Status

Hackathon prototype. Built to validate fast, personalized AI email drafting using RAG + OCR + LLMs.

## Author

Arush Sharma

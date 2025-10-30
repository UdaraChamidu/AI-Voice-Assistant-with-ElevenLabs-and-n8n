# 🎙️ Voice RAG System

> Ask questions to your documents using voice. Upload PDFs, speak your question, get spoken answers.

## What It Does

- Upload PDF documents through a web interface
- Ask questions using your voice (via ElevenLabs)
- Get accurate answers based on your documents
- Answers are spoken back to you

## Tech Stack

- **n8n** - Automation workflows
- **Pinecone** - Vector database
- **OpenAI** - AI language model
- **ElevenLabs** - Voice AI

## Quick Setup

### 1. Pinecone
- Create account at [pinecone.io](https://pinecone.io)
- Create index: name `sample`, dimensions `512`, metric `cosine`

### 2. n8n Workflows
- Import `Data_to_Pinecone.json` (for document uploads)
- Import `Voice-RAG-Agent.json` (for voice queries)
- Add your OpenAI and Pinecone API keys

### 3. ElevenLabs Agent
- Create agent at [elevenlabs.io](https://elevenlabs.io)
- Add webhook tool pointing to your n8n workflow
- Use the provided system prompt

### 4. Web Interface
- Open `upload.html` in browser
- Update webhook URL to your n8n instance
- Start uploading documents

## Usage

1. **Upload**: Drag and drop PDF files to the web interface
2. **Ask**: Speak your question to the ElevenLabs agent
3. **Listen**: Get accurate answers from your documents

## How It Works

```
PDF Upload → Text Extraction → Vector Embeddings → Pinecone Storage
↓
Voice Question → Vector Search → AI Response → Voice Answer
```

## Requirements

- n8n instance (cloud or self-hosted)
- OpenAI API key
- ElevenLabs API key
- Pinecone account

## Future Plans

- [ ] Text-based chat interface
- [ ] Document management

---

**Built with ❤️ using n8n, OpenAI, ElevenLabs, and Pinecone**


## How It Works


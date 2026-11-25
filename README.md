# agentic-ai-workflows
These 16 agentic AI workflows are created using n8n, largely.
# Autonomous Agentic AI Workflows & Multi-Agent Orchestration Portfolio

**Author:** Vikash Madduri  
**Platform:** n8n (Event-Driven, Webhook, Scheduled & Multimodal Orchestration)  
**Program:** MSc in Computer Science (Artificial Intelligence & Machine Learning) — Woolf University & Scaler Neovarsity (2026–2027)

## Overview
This repository documents **16 autonomous, production-tested Agentic AI workflows** built in **n8n**, spanning multimodal conversational interfaces (WhatsApp, Telegram, Voice Telephony), Retrieval-Augmented Generation (RAG) pipelines (including multilingual Indic-language retrieval with Sarvam AI and Supabase `pgvector`), Human-in-the-Loop (HITL) financial governance, academic opportunity scraping via MCP/Claude Code, and multi-channel social publishing engines[cite: 332].

> **Note on Confidentiality & Reproducibility:** All workflow blueprints (`workflow.json`), system prompts (`system_prompt.md`), and execution traces (`sample_io.md`) in this repository are sanitized with placeholder credentials and synthetic test payloads to ensure safe public sharing and reproducibility.

---

## Core Architectural Patterns Implemented
* **Multimodal & Omnichannel Ingestion:** Processing text, voice notes (Speech-to-Text / Text-to-Speech), images (Vision APIs), PDFs, webhooks, and outbound telephony calls (Retell AI / Twilio)[cite: 332].
* **Grounded Retrieval-Augmented Generation (RAG):** Semantic document chunking, OpenAI vector embeddings, `Simple Vector Store` and **Supabase (`pgvector`)** similarity search, and **Sarvam AI** Indic-to-English query translation with strict hallucination guardrails[cite: 332].
* **Human-in-the-Loop (HITL) & Governance Guardrails:** Threshold-based approval routing (`sendAndWait` Gmail pauses), status-gated publishing switches, regex input validation, and JSON Schema enforcement via `Structured Output Parser`[cite: 332].
* **Parallel Scraping & Deduplication Pipelines:** Concurrent Serper Dev & ScrapingBee ingestion, custom JavaScript timestamp normalization, URL deduplication, and rate-limited Google Sheets/CRM synchronization[cite: 332].

---

## Master Catalog of 16 Agentic AI Workflows

### 1. Conversational, Voice & Multimodal Assistants
| Agent | Workflow Name | Orchestration & Key Capabilities | Tech Stack |
| :--- | :--- | :--- | :--- |
| **Agent-01** | **[AI-Powered Medical Appointment Booking Assistant](./01-medical-appointment-assistant/)** | Multi-turn slot-filling (`Agent Vikash`), real-time regex phone/email validation, age/future-date checks, and confirmation loops before logging[cite: 332]. | `n8n`, `OpenAI API`, `Simple Memory`, `Google Sheets`, `Apify`[cite: 332] |
| **Agent-06** | **[Autonomous Telegram AI Bot for Commercial Product Image Generation](./06-telegram-product-image-bot/)** | Branches text and binary photo uploads (`/start` reset handling) to transform raw product cutouts into studio-lit commercial advertisements[cite: 332]. | `n8n`, `OpenAI GPT-5 Mini`, `OpenAI Image Edit`, `Telegram Bot API`[cite: 332] |
| **Agent-13** | **[Autonomous Conversational AI Voice Agent for Clinic Scheduling](./13-voice-clinic-scheduling-agent/)** | Triggers instant outbound telephony calls via Retell AI ("Anamika") upon form submission, parses spoken preferences, and books Google Calendar events[cite: 332]. | `n8n`, `Retell AI`, `Twilio SIP`, `OpenAI API`, `Google Calendar`, `Google Sheets`[cite: 332] |
| **Agent-14** | **[Multimodal WhatsApp AI Assistant (Text, Voice & Vision)](./14-multimodal-whatsapp-assistant/)** | Triages WhatsApp text, voice notes (Whisper STT + TTS with MP3 MIME normalization), and images (GPT-4.1 Mini Vision) with symmetric modality replies[cite: 332]. | `n8n`, `WhatsApp Cloud API`, `GPT-5 Mini`, `GPT-4.1 Mini Vision`, `Whisper / TTS`[cite: 332] |

### 2. Knowledge Retrieval (RAG) & Multilingual Document Intelligence
| Agent | Workflow Name | Orchestration & Key Capabilities | Tech Stack |
| :--- | :--- | :--- | :--- |
| **Agent-02** | **[RAG Knowledge Base & Conversational AI Agent](./02-rag-knowledge-base-agent/)** | Dual-flow ingestion (PDF/DOCX parsing + OpenAI embeddings) and chat retrieval tool with strict context-only grounding and out-of-scope fallbacks[cite: 332]. | `n8n`, `OpenAI Embeddings`, `OpenAI Chat Model`, `Simple Vector Store`[cite: 332] |
| **Agent-16** | **[Multilingual RAG Agent for Indian Language Documents](./16-multilingual-indic-rag-agent/)** | Translates Indic queries via **Sarvam AI (`mayura:v1`)**, queries **Supabase `pgvector`** (`match_documents`), and summarizes Hindi government EOIs in English[cite: 332]. | `n8n`, `Sarvam AI API`, `Supabase (pgvector)`, `Postgres Memory`, `GPT-4o Mini`[cite: 332] |

### 3. Enterprise Operations, Financial Governance & Inbox Automation
| Agent | Workflow Name | Orchestration & Key Capabilities | Tech Stack |
| :--- | :--- | :--- | :--- |
| **Agent-05** | **[Autonomous Gmail Triage, Classification & Auto-Reply Agent](./05-gmail-intent-classifier/)** | Batch-processes incoming emails, classifies 4 intents (`course`, `payment`, `consultation`, `common_query`) with JSON confidence scores, applies labels, and auto-replies[cite: 332]. | `n8n`, `OpenAI Chat Model`, `Structured Output Parser`, `Gmail API`[cite: 332] |
| **Agent-09** | **[Automated Multi-Department Invoice Classification & Routing Pipeline](./09-invoice-classification-routing/)** | Parses inbound webhook PDFs, extracts structured invoice fields via custom JavaScript regex, and routes to HR, Procurement, Finance, or Misc queues[cite: 332]. | `n8n`, `JavaScript (Node.js)`, `PDF Text Extractor`, `Google Sheets`, `Webhooks`[cite: 332] |
| **Agent-10** | **[Human-in-the-Loop Invoice Approval & Financial Governance Engine](./10-hitl-invoice-approval-engine/)** | Auto-approves compliant invoices $\le 2,000\text{ INR}$ and pauses execution via Gmail `sendAndWait` for mandatory management sign-off above threshold[cite: 332]. | `n8n`, `JavaScript (Node.js)`, `Gmail API (sendAndWait)`, `Google Sheets`, `Webhooks`[cite: 332] |

### 4. Academic Research & B2B / Hiring Intelligence Pipelines
| Agent | Workflow Name | Orchestration & Key Capabilities | Tech Stack |
| :--- | :--- | :--- | :--- |
| **Agent-11** | **[Autonomous B2B Lead Enrichment & Cold Outreach Pipeline](./11-b2b-lead-enrichment-outreach/)** | Discovers LinkedIn executive profiles via Serper Dev, isolates C-Suite/Founder roles via LLM guardrails, drafts tailored pitches, and sends HTML outreach emails[cite: 332]. | `n8n`, `Serper Dev API`, `OpenAI GPT-5 Mini`, `Gmail API`, `Google Sheets`[cite: 332] |
| **Agent-12** | **[Autonomous AI PhD Opportunity Research & Scraping Agent](./12-phd-opportunity-scraper/)** | Scheduled agent (built with MCP & Claude Code) scraping EURAXESS/FindAPhD portals, validating eligibility/deadlines, deduplicating, and logging to Sheets[cite: 332]. | `n8n`, `ScrapingBee`, `OpenAI API`, `JavaScript`, `Google Sheets`, `Claude MCP`[cite: 332] |
| **Agent-15** | **[Automated Multi-Channel Freelance & Hiring Lead Scraping Engine](./15-linkedin-hiring-lead-scraper/)** | Executes 9 parallel Serper Dev queries across AI/automation niches, normalizes relative timestamps within a 14-day window, deduplicates URLs, and logs with 5s pacing[cite: 332]. | `n8n`, `Serper Dev API`, `JavaScript (Node.js)`, `Google Sheets`[cite: 332] |

### 5. Multi-Platform Content & Automated Social Publishing Engines
| Agent | Workflow Name | Orchestration & Key Capabilities | Tech Stack |
| :--- | :--- | :--- | :--- |
| **Agent-03** | **[Automated Social Media Content & Image Generation Pipeline](./03-social-media-content-generator/)** | Reads campaign briefs from Sheets, generates platform-tailored copy (LinkedIn, Facebook, Instagram) with JSON schema validation, creates visuals, and archives to Drive[cite: 332]. | `n8n`, `OpenAI Chat Model`, `DALL·E`, `Google Sheets`, `Google Drive`[cite: 332] |
| **Agent-04** | **[Automated AI Content & LinkedIn Publishing Engine](./04-linkedin-publishing-engine/)** | Status-gated multi-branch pipeline generating ad copy/visuals, enforcing human review checkpoints, and publishing directly via LinkedIn OAuth HTTP API[cite: 332]. | `n8n`, `OpenAI API`, `DALL·E`, `LinkedIn API`, `Google Drive`, `Google Sheets`[cite: 332] |
| **Agent-07** | **[Multi-Platform AI Content & Social Publishing Engine (LinkedIn & Facebook)](./07-linkedin-facebook-publishing-engine/)** | Extends status-routed creative generation with dual-channel automated publishing to both LinkedIn and Facebook Pages via Graph API tokens[cite: 332]. | `n8n`, `OpenAI API`, `DALL·E`, `LinkedIn API`, `Facebook Graph API`, `Google Drive`[cite: 332] |
| **Agent-08** | **[Automated Instagram Content Generation & Publishing Engine](./08-instagram-publishing-engine/)** | Manages the asynchronous Meta Graph API v23.0 media container lifecycle (`Wait` + `status_code == FINISHED` polling) to publish feed posts autonomously[cite: 332]. | `n8n`, `GPT-5 Mini`, `OpenAI Image Gen`, `Instagram Graph API`, `Google Drive`[cite: 332] |

---

## Repository Structure
Each agent folder (`01-...` through `16-...`) contains:
```text
├── README.md          # Architecture breakdown, node flow, validation rules & live outcomes
├── workflow.json      # Exported n8n workflow blueprint (API keys and credentials scrubbed)
├── system_prompt.md   # Agent system instructions, JSON output schemas & guardrails
└── sample_io.md       # Sanitized input payload and verified execution output

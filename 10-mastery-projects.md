# Mastery Projects — 10 Built Apps

> **After A9.** Build production-grade AI applications from scratch. No tutorials, no hand-holding.
> 10 projects. Blind builds. Reference reveal. Gap analysis.

---

## How Mastery Projects Work

### Format (mirrors Backend Mastery Phase)

Each project follows this protocol:

1. **Read the brief.** One paragraph + capabilities checklist.
2. **Design and build it blind.** No hints during the build.
3. **Submit your build.** When done, tell the AI instructor.
4. **Reference reveal.** The AI reveals a reference solution + design doc.
5. **Gap analysis.** Compare your build against the reference.

### Reuse the provider abstraction

Every project starts from your A1 `provider-abstraction`. You never rebuild it.

### Free-tier discipline

Every project must run on free-tier or local infrastructure. No paid APIs required.

### Production-grade means

Every project must be:

- **Fully documented** (README with architecture diagram, trade-offs, limitations)
- **Fully tested** (unit + integration where applicable)
- **Observable** (traces, cost tracking, latency metrics)
- **Evaluable** (fixed test set + regression pipeline)
- **Deployable** (Docker + run script)

A project is not "done" until it ships.

---

## The 10 Projects

### 1. Multi-Provider Chatbot

**Brief**: A chat application that talks to any of Gemini, Groq, OpenRouter, or Ollama through a unified interface, streams responses, tracks cost, and falls back automatically.

**Capabilities**:

- Provider abstraction (from A1)
- Streaming responses (SSE)
- Cost tracking per request
- Fallback chain
- Conversation memory (session-scoped)
- Web UI (minimal)

**Proves**: A1, A2, A4 core skills.

**Deliverables**: `projects/01-multi-provider-chatbot/`

---

### 2. PDF Q&A with Citations

**Brief**: A service that ingests PDFs, answers questions about them with citations back to source pages, evaluates on a fixed test set, and handles incremental document updates.

**Capabilities**:

- PDF ingestion pipeline
- Chunking (semantic + parent-child)
- Free/local embeddings
- pgvector storage
- Hybrid search (BM25 + vector)
- Cross-encoder reranking
- Citation generation
- Eval on a fixed set
- Incremental updates + deletes

**Proves**: A5 (retrieval) end-to-end.

**Deliverables**: `projects/02-pdf-qa/`

---

### 3. Codebase Q&A Assistant

**Brief**: A service that indexes a codebase, answers questions about its structure and behavior, and provides code references. Uses code graph + semantic search.

**Capabilities**:

- Code parsing (Tree-sitter via ast-grep or similar)
- Code graph (files, symbols, dependencies)
- Semantic code search
- Query answering with code references
- Incremental indexing
- Repository updates

**Proves**: A5 + A8 (code comprehension tools).

**Deliverables**: `projects/03-codebase-qa/`

---

### 4. Customer Support Agent

**Brief**: A support agent that uses tools to look up orders, check status, escalate to humans, and cite policies.

**Capabilities**:

- Tool calling (order lookup, policy search, escalation)
- Memory (customer context across sessions)
- Retrieval (policy docs)
- Escalation to human (approval gate)
- Cost tracking per conversation
- Success metrics (resolution rate, cost per ticket)
- Guardrails (no off-topic responses)

**Proves**: A3, A4, A5, A6 primitives together.

**Deliverables**: `projects/04-customer-support/`

---

### 5. Email Triage Assistant

**Brief**: A service that reads incoming emails, classifies them, drafts replies, and escalates priority items. Human-in-the-loop for sending.

**Capabilities**:

- Email ingestion
- Classification (urgent / normal / spam)
- Draft replies (with tone matching)
- Priority escalation
- Approval gate before sending
- Cost tracking
- Metrics (accuracy, response time)

**Proves**: A2, A3, A4, A6 (approval workflows).

**Deliverables**: `projects/05-email-triage/`

---

### 6. Research Assistant (Multi-Agent)

**Brief**: A multi-agent system that researches a question using web search, retrieval, and reasoning, and produces a cited report.

**Capabilities**:

- Planner agent (decomposes question)
- Researcher agents (retrieval + web search tools)
- Writer agent (synthesizes)
- Reviewer agent (critiques, requests revisions)
- Shared memory
- Human-in-the-loop for final publishing
- Cost tracking per task
- Evaluation on fixed research questions

**Proves**: A6 (multi-agent) end-to-end.

**Deliverables**: `projects/06-research-assistant/`

---

### 7. Personal Knowledge Base

**Brief**: A service that ingests your notes, articles, and links; answers questions about them; and maintains a long-term memory of your preferences and interests.

**Capabilities**:

- Multi-source ingestion (markdown, URLs, PDFs)
- Semantic search across all content
- Long-term memory (user profile, interests)
- Memory consolidation (summarize old content)
- Memory decay (recency weighting)
- GDPR export/delete
- Cost tracking

**Proves**: A4 (memory) + A5 (retrieval).

**Deliverables**: `projects/07-personal-kb/`

---

### 8. Coding Assistant with MCP

**Brief**: A coding assistant that runs as an MCP server, exposes tools (read file, write file, run tests, search codebase), and integrates with Antigravity, Codex, and Cursor.

**Capabilities**:

- Custom MCP server (tools + resources)
- Tool sandboxing (Docker)
- File permissions (restricted paths)
- Command allowlist
- Per-tool rate limits
- Logging (tool calls, durations)
- Works across multiple agents

**Proves**: A3 (tools) + A6 (MCP) + A7 (skills integration).

**Deliverables**: `projects/08-coding-assistant-mcp/`

---

### 9. Voice Assistant

**Brief**: A voice-based assistant that transcribes speech, processes it with an LLM, and responds with synthesized speech.

**Capabilities**:

- Speech-to-text (Whisper local or free tier)
- LLM processing
- Text-to-speech (local or free tier)
- Conversation memory
- Interruption handling
- Latency optimization (streaming STT → LLM → TTS)
- Cost tracking (per second of audio)

**Proves**: A3 (tools), A4 (memory), multimodal awareness.

**Deliverables**: `projects/09-voice-assistant/`

---

### 10. Production AI Platform

**Brief**: A production-grade AI service with full observability, evaluation, cost controls, and safety — a reference for how AI applications should be operated.

**Capabilities**:

- Complete observability (traces, metrics, dashboards)
- Evaluation pipeline (regression + LLM-as-judge + A/B testing)
- Cost controls (prompt caching, semantic caching, routing, budgets)
- Safety (injection defense, PII redaction, output filtering)
- Multi-tenancy (isolation, quotas, GDPR)
- Deployment (canary, feature flags, rollback)
- Runbook + postmortem template
- Local fallback (Ollama)

**Proves**: A9 (production) end-to-end.

**Deliverables**: `projects/10-production-ai-platform/`

---

## Recommended Order

1. Multi-Provider Chatbot (warm-up)
2. PDF Q&A with Citations (RAG)
3. Codebase Q&A Assistant (code comprehension)
4. Customer Support Agent (tools + memory)
5. Email Triage Assistant (classification + approval)
6. Research Assistant (multi-agent)
7. Personal Knowledge Base (long-term memory)
8. Coding Assistant with MCP (MCP + sandboxing)
9. Voice Assistant (multimodal)
10. Production AI Platform (capstone)

---

## What "Done" Looks Like

You've completed Mastery Phase when:

- All 10 apps are built, tested, documented, and deployed
- Each has a README with architecture, trade-offs, and cost estimate
- Each runs on free-tier or local infrastructure
- You can start a new AI app from the A1 provider abstraction and ship a real feature within a day
- You can look at any AI problem and know which primitives to reach for

---

## Reference Solutions

For each project, a reference solution exists (revealed after your build). The reference includes:

- Full source code
- Architecture diagram (Mermaid)
- Design doc (trade-offs, alternatives)
- Cost benchmarks (per request, per user)
- A "what I'd do differently at 10x scale" section

The reference is **one** correct answer. Not **the** correct answer. Gap analysis, not grading.

# Design Capstones — 10 Systems

> Design 10 real AI systems at scale. Produce 10 design docs + 10 defense transcripts.
> Uses the same 7-part format and Mock Defense Protocol as System Design T5.

---

## Purpose

By the end of the design capstones, you can:

- Design an AI system end-to-end from requirements to failure modes
- Defend the design under Staff-Engineer-level grilling
- Revise designs based on gap analysis
- Build a portfolio of 10 design docs + 10 defense transcripts

---

## Anchored Artifact

**10 design docs + 10 defense transcripts.**

Each capstone produces:

- `design-docs/[capstone-slug].md` — the 7-part design doc (written by you)
- `defense-transcripts/[capstone-slug].md` — the mock defense transcript (written by AI)

**Deliverables**: 20 documents total.

---

## The Mock Defense Protocol

Same as System Design T5:

1. **Sketch** — you design on paper/Excalidraw, untimed. AI does not help.
2. **Write** — you produce the 7-part design doc. AI does not help.
3. **Defend** — AI acts as FAANG Staff Engineer. Grills on SPOFs, 10x/100x spikes, edge cases, AI-specific failure modes (provider outages, prompt injection, cost explosion). One question at a time.
4. **Reveal** — AI presents a reference solution + gap analysis.
5. **Revise** — you revise your design doc based on the gap analysis.

---

## The 7-Part Design Doc Format

```
# [System Name] — Design Doc

## 1. Requirements & Scope
Functional requirements, non-functional requirements (p99 latency, availability, consistency), out of scope.

## 2. Capacity Estimation
QPS, tokens per request, cost per request, storage per year, cache sizing. Back-of-the-envelope math shown.

## 3. High-Level Design
End-to-end architecture diagram (Mermaid). Component responsibilities. Data flow.

## 4. Low-Level Design
Database schemas, indexes. API contracts. Prompt/model choices. Caching strategy. Fallback chain.

## 5. Trade-offs & Alternatives
Why this design over alternatives. What you're giving up.

## 6. Failure Modes & Mitigations
What breaks under 10x traffic. What breaks under provider outage. What breaks under prompt injection. Cost spike scenarios.

## 7. Defense Transcript
AI grill questions + your answers. Gap analysis (your design vs reference).
```

---

## The 10 Capstones

### 1. ChatGPT-Style Conversational Assistant

**Design**: A general-purpose conversational assistant at 10M DAU.

**Focus areas for defense**:

- Multi-provider abstraction (avoid vendor lock-in)
- Conversation state at scale (Redis + Postgres)
- Streaming responses with backpressure
- Cost model per conversation
- Prompt injection defense
- Model routing (fast vs reasoning based on query)
- Fallback chain when providers are down

**Deliverables**: `design-docs/01-chatgpt-assistant.md` + `defense-transcripts/01-chatgpt-assistant.md`

---

### 2. GitHub Copilot-Style Coding Assistant

**Design**: A coding assistant that understands the codebase and suggests completions + multi-file edits.

**Focus areas for defense**:

- Codebase indexing (graph + semantic)
- Context selection (what to include in the prompt)
- Latency budget (<200ms for completion)
- Streaming partial completions
- Prompt caching for repeated prefixes
- Multi-file edit orchestration
- Cost per active developer

**Deliverables**: `design-docs/02-coding-assistant.md` + `defense-transcripts/02-coding-assistant.md`

---

### 3. Perplexity-Style Search + Retrieval Engine

**Design**: A search engine that answers queries with cited sources at scale.

**Focus areas for defense**:

- Retrieval pipeline (BM25 + vector + reranking)
- Source diversity + freshness
- Citation accuracy
- Query understanding + reformulation
- Latency budget (<2s end-to-end)
- Cost per query
- Handling breaking news (fresh content)

**Deliverables**: `design-docs/03-search-retrieval.md` + `defense-transcripts/03-search-retrieval.md`

---

### 4. Cursor-Style Autonomous Coding Agent

**Design**: An autonomous coding agent that plans multi-step changes, edits files, runs tests, iterates.

**Focus areas for defense**:

- Agent loop (plan → act → observe → repeat)
- Tool sandboxing (filesystem, shell, network)
- Stopping criteria (when is the task done?)
- Cost per task (unbounded without caps)
- Context management (large repos)
- Approval gates for risky actions
- Fallback when stuck

**Deliverables**: `design-docs/04-coding-agent.md` + `defense-transcripts/04-coding-agent.md`

---

### 5. Notion AI-Style Document Q&A + Extraction

**Design**: A workspace AI that answers questions over documents, extracts structured data, and generates summaries at scale.

**Focus areas for defense**:

- Multi-tenant document isolation
- Retrieval quality across heterogeneous docs
- Structured extraction (schemas, validation)
- Incremental indexing
- Permissions model (which users see which docs)
- Cost per workspace
- Latency for interactive queries

**Deliverables**: `design-docs/05-document-qa.md` + `defense-transcripts/05-document-qa.md`

---

### 6. Customer Support Agent at Scale

**Design**: A support agent handling 10M tickets/day across multiple languages and channels.

**Focus areas for defense**:

- Multi-channel ingestion (email, chat, phone)
- Tool integration (order lookup, refunds, escalation)
- Human-in-the-loop for high-stakes actions
- Multi-language support
- Cost per ticket
- Success metrics (resolution rate)
- Escalation paths and SLAs
- Audit trail for compliance

**Deliverables**: `design-docs/06-customer-support.md` + `defense-transcripts/06-customer-support.md`

---

### 7. Multi-Agent Research System

**Design**: A research platform where multiple agents collaborate to produce comprehensive reports.

**Focus areas for defense**:

- Agent coordination (supervisor, pipeline, or hybrid)
- Shared state and communication
- Cost per research task
- Quality measurement (report accuracy)
- Failure modes (agents deadlock, disagree, loop)
- Human-in-the-loop for critical findings
- Scaling concurrent research tasks

**Deliverables**: `design-docs/07-research-system.md` + `defense-transcripts/07-research-system.md`

---

### 8. MCP-Based Tool Ecosystem

**Design**: A platform of MCP servers exposing internal tools to AI agents, with auth, permissions, and observability.

**Focus areas for defense**:

- MCP server architecture (tools, resources, prompts)
- Authentication (OAuth for user-triggered tools)
- Permission scoping (per-tool, per-user)
- Audit logging
- Tool poisoning defense
- Rate limiting per MCP server
- Deployment (local vs remote MCP)
- How agents discover + use MCP servers

**Deliverables**: `design-docs/08-mcp-ecosystem.md` + `defense-transcripts/08-mcp-ecosystem.md`

---

### 9. Voice Agent at Scale

**Design**: A voice assistant handling 1M concurrent calls.

**Focus areas for defense**:

- STT → LLM → TTS pipeline latency budget (<500ms perceived)
- Barge-in (interruption handling)
- Real-time streaming protocol
- Cost per minute of audio
- Multi-language support
- Fallback when STT/TTS providers fail
- Concurrent call handling
- Session state across interruptions

**Deliverables**: `design-docs/09-voice-agent.md` + `defense-transcripts/09-voice-agent.md`

---

### 10. Production AI Platform (Design + Capacity Math)

**Design**: A comprehensive AI platform that provides LLM access, RAG, agents, and observability as internal infrastructure for 100 teams.

**Focus areas for defense**:

- Multi-tenant platform design (isolation, quotas, billing)
- Provider abstraction + routing at scale
- Shared RAG infrastructure
- Agent orchestration service
- Evaluation as a service
- Observability for 100 teams
- Cost allocation and chargeback
- Compliance (GDPR, SOC2, data residency)
- SLA for platform availability

**Deliverables**: `design-docs/10-production-platform.md` + `defense-transcripts/10-production-platform.md`

---

## Recommended Order

1. ChatGPT-style assistant (warm-up)
2. Coding assistant (code comprehension)
3. Perplexity-style search (retrieval at scale)
4. Cursor-style agent (autonomous)
5. Document Q&A (multi-tenant)
6. Customer support (tool-heavy)
7. Multi-agent research (coordination)
8. MCP ecosystem (platform)
9. Voice agent (real-time)
10. Production platform (capstone)

---

## What "Done" Looks Like

- 10 design docs (7 parts each)
- 10 defense transcripts
- Each design defended, revised, and improved
- The portfolio is what you show to senior AI engineering interviewers

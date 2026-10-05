# Case Studies Vault

> 35 real AI products and platforms. Read on demand — the AI never proactively suggests them.
> Each case study reinforces specific tiers. Say "go deeper on [name]" for a full analysis.

---

## How to Use This Vault

Case studies are read **on demand**. Not part of the linear tier progression. Read when you want to see how a real system solved a problem you're working on.

**On-demand deep dives**: say _"go deeper on [case study name]"_ → generates `case-study-deep-dives/[slug].md` with a 5-part structure.

**Length**: Short entries below are ~200 words each. Deep dives are ~600 lines.

---

## Case Study Table

| #   | System                        | Primary Tier | Why It Matters                                      |
| --- | ----------------------------- | ------------ | --------------------------------------------------- |
| 1   | Claude Code                   | A6, A7, A8   | Terminal agent architecture; skills + MCP ecosystem |
| 2   | Cursor                        | A5, A8       | Codebase indexing + Composer multi-file editing     |
| 3   | GitHub Copilot                | A1, A8       | IDE-to-suggestion pipeline; latency constraints     |
| 4   | Perplexity                    | A5, A9       | Retrieval + reranking pipeline at scale             |
| 5   | v0 (Vercel)                   | A2, A8       | Component generation from prompts                   |
| 6   | Notion AI                     | A4, A5       | Document understanding + workspace memory           |
| 7   | Devin (Cognition)             | A6           | Autonomous coding agent                             |
| 8   | ChatGPT Memory                | A4           | Long-term memory storage + retrieval                |
| 9   | Character.AI                  | A4, A9       | Conversation at scale                               |
| 10  | Segment + OpenAI              | A9           | Production AI integration patterns                  |
| 11  | Claude Projects & Artifacts   | A4, A6       | Workspace + rendering architecture                  |
| 12  | Gemini Code Assist            | A5, A8       | Google's IDE integration                            |
| 13  | Replit Agent                  | A6, A8       | Browser-based full-stack agent                      |
| 14  | Windsurf / Codeium            | A5, A8       | Codebase indexing and reasoning                     |
| 15  | Lovable                       | A6, A8       | Non-developer app builder                           |
| 16  | Bolt.new                      | A6, A8       | In-browser full-stack generation                    |
| 17  | Perplexity Labs               | A5, A6       | Research + report generation                        |
| 18  | Midjourney                    | A1, A9       | Diffusion pipeline at scale                         |
| 19  | Suno                          | A1, A9       | Music generation infrastructure                     |
| 20  | Runway                        | A1, A9       | Video generation architecture                       |
| 21  | OpenRouter                    | A1, A8       | Multi-provider routing                              |
| 22  | LangSmith / LangFuse          | A9           | LLM observability platforms                         |
| 23  | Vercel AI SDK                 | A1, A3       | Abstraction layer design                            |
| 24  | Pinecone                      | A5, A9       | Managed vector DB                                   |
| 25  | Ollama                        | A1, A8       | Local model serving                                 |
| 26  | Anthropic's Constitutional AI | A9           | Safety architecture                                 |
| 27  | OpenAI's Moderation API       | A9           | Content moderation at scale                         |
| 28  | Stripe's AI integration       | A9           | Payments + AI                                       |
| 29  | Shopify Sidekick              | A6, A9       | Commerce AI assistant                               |
| 30  | Salesforce Einstein           | A6, A9       | Enterprise AI assistant                             |
| 31  | GitHub Copilot Chat           | A3, A6       | Tool-augmented chat in IDE                          |
| 32  | Sourcegraph Cody              | A5, A8       | Enterprise code AI                                  |
| 33  | Netflix's ML platform         | A9           | Production ML/AI at scale                           |
| 34  | Spotify's AI DJ               | A4, A6       | Personalization + generation                        |
| 35  | Hugging Face Spaces           | A8, A9       | AI app hosting + sharing                            |

---

## Sample Case Study Entries

### 1. Claude Code

**Tier**: A6, A7, A8

**Why it matters**: Claude Code is Anthropic's terminal-first coding agent. It demonstrates the modern agent architecture: tool calling (bash, file operations, web fetch), context management across a repo, skills loaded on demand, MCP servers for extensibility.

**Key lessons**:

- Terminal-first UX forces explicit context (unlike IDE agents)
- Tool selection happens via description matching
- Skills progressively disclosed (name + description at startup, content on demand)
- MCP servers exposed as tools within the agent loop
- Cost model: per-token + per-cache-write
- Where it fits: interactive coding, complex multi-file changes

---

### 2. Cursor

**Tier**: A5, A8

**Why it matters**: Cursor is a VS Code fork with AI-native editing. Its architecture shows how codebase indexing (embeddings + tree structure), context selection (which files to include), and multi-file editing (Composer) work together.

**Key lessons**:

- Codebase indexed with vector embeddings + AST structure
- Context selection based on cursor position + semantic similarity
- Composer orchestrates multi-file edits
- Latency budget: <200ms for completion; <5s for multi-file
- Cost model: subscription (fixed) + token limits
- Where it fits: IDE-integrated coding, refactoring

---

### 4. Perplexity

**Tier**: A5, A9

**Why it matters**: Perplexity is a search engine that answers with citations. Its architecture covers retrieval (web + index), reranking, source selection, and citation generation at scale.

**Key lessons**:

- Multi-stage retrieval (BM25 + embeddings + reranking)
- Source diversity enforced (avoid single-source answers)
- Freshness signals in ranking
- Citation accuracy as a first-class metric
- Latency budget: <2s end-to-end
- Cost model: per-query with caching
- Where it fits: research, fact-checking

---

### 7. Devin (Cognition)

**Tier**: A6

**Why it matters**: Devin is an autonomous coding agent with planning, tool use (shell, browser, code editor), and self-correction. First "AI software engineer" product.

**Key lessons**:

- Agent loop with explicit planning phase
- Sandboxed environment (browser + terminal + file system)
- Long-horizon tasks (hours, not minutes)
- Cost per task: unbounded without caps
- Where it fits: autonomous coding on well-defined tasks

---

### 21. OpenRouter

**Tier**: A1, A8

**Why it matters**: OpenRouter provides a unified API across many model providers. Its architecture shows how provider abstraction works at production scale.

**Key lessons**:

- Single API for dozens of providers
- Routing based on cost, latency, availability
- Free-tier models flagged + rate-limited
- Fallback chains handled at platform level
- Cost: pass-through + small markup
- Where it fits: multi-provider applications

---

### 30. Salesforce Einstein

**Tier**: A6, A9

**Why it matters**: Enterprise AI assistant embedded in a CRM. Multi-tenant, permission-aware, audit-logged. Shows how AI integrates into existing enterprise software.

**Key lessons**:

- Per-tenant data isolation enforced
- Permissions enforced before retrieval
- Audit logging for every AI action
- Human-in-the-loop for high-stakes actions
- Cost allocation per tenant
- Where it fits: enterprise AI

---

## Case Studies by Tier (Full Mapping)

**A1** (Foundations): #3, #18, #19, #20, #21, #23, #25
**A2** (Prompting): #5
**A3** (Tools): #23, #31
**A4** (Memory): #6, #8, #9, #11, #34
**A5** (Retrieval): #2, #4, #12, #14, #17, #24, #32
**A6** (Agents): #1, #7, #11, #13, #15, #16, #17, #29, #30, #31, #34
**A7** (Skills): #1
**A8** (Ecosystem): #1, #2, #3, #5, #12, #13, #14, #15, #16, #21, #23, #25, #32, #35
**A9** (Production): #4, #9, #10, #18, #19, #20, #22, #24, #26, #27, #28, #29, #30, #33, #35

---

## On-Demand Deep Dives

Say _"go deeper on [name]"_ → generates `case-study-deep-dives/[slug].md`:

1. 💡 Context & Why It Matters
2. 🔬 Technical Deep Dive
3. 📐 Diagrams / Schemas / Architecture
4. ⚠️ Trade-offs, Failure Modes & What Went Wrong
5. 🎯 What You Can Apply

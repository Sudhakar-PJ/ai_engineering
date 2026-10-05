# Problems → Patterns Index

> A grep-able lookup table. When you think "which pattern solves this?", come here first.

---

## Foundations (A1)

| Problem                    | Pattern                                   | Tier       |
| -------------------------- | ----------------------------------------- | ---------- |
| "Locked into one provider" | Provider abstraction layer                | A1.3       |
| "Free tier exhausted"      | Fallback chain to another provider        | A1.4       |
| "Surprise costs"           | Token tracking from day one               | A1.4       |
| "Slow perceived response"  | Streaming (SSE)                           | A1.5       |
| "Rate limit hit mid-task"  | Exponential backoff + provider fallback   | A1.4       |
| "Provider outage"          | Multi-provider fallback + circuit breaker | A1.4, A9.4 |

## Prompting (A2)

| Problem                      | Pattern                                | Tier |
| ---------------------------- | -------------------------------------- | ---- |
| "Inconsistent outputs"       | Structured output + Zod validation     | A2.3 |
| "Model ignores instructions" | Chain-of-thought + delimiters + role   | A2.2 |
| "Can't measure quality"      | Eval sets + LLM-as-judge               | A2.4 |
| "Prompt injection"           | Input sanitization + output validation | A2.5 |
| "No prompt versioning"       | Git-tracked prompts + eval CI          | A2.4 |

## Tools (A3)

| Problem                           | Pattern                                | Tier |
| --------------------------------- | -------------------------------------- | ---- |
| "Model can't reach external data" | Tool calling + function schemas        | A3.2 |
| "Tool errors kill the loop"       | Feed errors back to model for recovery | A3.4 |
| "Arbitrary code execution"        | Docker sandbox + allowlist             | A3.5 |
| "No standard tool integration"    | MCP servers                            | A3.6 |
| "Secrets leaked in prompts"       | Secret management + tool-only access   | A3.5 |

## Memory (A4)

| Problem                         | Pattern                              | Tier       |
| ------------------------------- | ------------------------------------ | ---------- |
| "Model forgets between calls"   | Session state + long-term memory     | A4.2, A4.3 |
| "Context window exceeded"       | Token budget + compression           | A4.4       |
| "Irrelevant memories retrieved" | Hybrid ranking (recency + relevance) | A4.5       |
| "Memory grows forever"          | Consolidation + decay                | A4.5       |
| "Cross-user leaks"              | Per-user isolation + quotas          | A4.6       |

## Retrieval (A5)

| Problem                            | Pattern                             | Tier |
| ---------------------------------- | ----------------------------------- | ---- |
| "Hallucinations despite documents" | Grounded RAG with citations         | A5.1 |
| "Poor retrieval quality"           | Hybrid search (BM25 + vector) + RRF | A5.5 |
| "Irrelevant top-K"                 | Cross-encoder reranking             | A5.5 |
| "Expensive embeddings"             | Local embeddings (BGE, Nomic)       | A5.3 |
| "Full re-index on updates"         | Incremental indexing with caching   | A5.6 |
| "Silent quality regression"        | RAGAS + regression testing          | A5.8 |

## Agents (A6)

| Problem                               | Pattern                                | Tier |
| ------------------------------------- | -------------------------------------- | ---- |
| "Infinite loops"                      | Max iterations + stopping criteria     | A6.2 |
| "Runaway costs"                       | Per-task budget + cost tracking        | A6.7 |
| "Single agent hits complexity limits" | Multi-agent (supervisor, pipeline)     | A6.5 |
| "Agents lose each other's state"      | Shared memory + communication protocol | A6.5 |
| "Agents do harmful actions"           | Approval gates + sandboxing            | A6.7 |
| "No agent evaluation"                 | Task success + iteration metrics       | A6.7 |

## Skills (A7)

| Problem                              | Pattern                                  | Tier |
| ------------------------------------ | ---------------------------------------- | ---- |
| "Context bloat from too many skills" | Layered stack (one per layer)            | A7.7 |
| "Skills never load"                  | Precise descriptions                     | A7.2 |
| "Malicious skill install"            | openclaw-skill-vetter-mcp before install | A7.4 |
| "Agent-specific skills"              | Portable SKILL.md core                   | A7.5 |
| "No skill for my need"               | Build with skill-creator                 | A7.6 |

## Ecosystem (A8)

| Problem                        | Pattern                                  | Tier |
| ------------------------------ | ---------------------------------------- | ---- |
| "Wrong agent for the task"     | Agent routing cheatsheet                 | A8.3 |
| "Burn through quotas fast"     | Free-tier optimization + local fallback  | A8.3 |
| "Adopt tools on hype"          | 5-minute evaluation framework            | A8.6 |
| "Forget rejected tools"        | tool-evaluations.md with revisit cadence | A8.6 |
| "Outdated landscape awareness" | Update AI Landscape file                 | A8.7 |

## Production (A9)

| Problem                            | Pattern                                     | Tier |
| ---------------------------------- | ------------------------------------------- | ---- |
| "Can't diagnose failures"          | Distributed tracing + dashboards            | A9.1 |
| "Silent quality regression"        | Eval pipeline + regression testing          | A9.2 |
| "Runaway costs"                    | Prompt caching + semantic caching + budgets | A9.3 |
| "Provider outage = service outage" | Fallback chain + circuit breakers           | A9.4 |
| "Prompt injection in production"   | Multi-layer defense                         | A9.5 |
| "PII leaks"                        | PII detection + redaction                   | A9.5 |
| "Multi-tenant leaks"               | Tenant isolation + quotas                   | A9.6 |
| "Regressions to all users"         | Canary deployments                          | A9.7 |
| "No incident response"             | Runbook + postmortems                       | A9.8 |

---

## Cross-References to Backend + System Design

| AI pattern                 | Backend coverage    | System Design coverage |
| -------------------------- | ------------------- | ---------------------- |
| Rate limiting AI providers | Backend T3c.5, T4.6 | System Design T3.5.2   |
| Caching (semantic, prompt) | Backend T3c.6, T5.5 | System Design T3.5.1   |
| Vector DBs (pgvector)      | Backend T3a         | —                      |
| Multi-tenancy              | Backend T7.7        | System Design T3.5.5   |
| Observability              | Backend T6.6        | System Design T3.5.9   |
| Idempotency                | Backend T4.7, T5.1  | System Design T3.2     |
| Streaming (SSE, WS)        | Backend T7.5        | —                      |
| Job queues                 | Backend T5.2        | System Design T3.5.3   |
| Secrets management         | Backend T4.7        | System Design T3.5.10  |
| Deployments (canary)       | Backend T6.5        | —                      |

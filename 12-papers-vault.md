# Papers Vault

> 25 seminal papers for AI Application Engineering. Read inline as the tier where they matter arrives.
> Each paper has a digest → read → analysis treatment. Deep-dive analyses generated on demand.

---

## How to Use This Vault

Papers are read **during the tier where their concept is taught**. When you reach A5 (Retrieval), you read the RAG paper. When you reach A6 (Agents), you read ReAct.

**Reading depth**:

- **Architecture-level** — understand the shape, no math
- **Deep read** — read the paper itself, with guided commentary
- **Analysis** — write a 1-page paper analysis (only for papers marked "Deep Read")

**On-demand deep dives**: say _"go deeper on [paper name]"_ → generates `paper-deep-dives/[slug].md`.

---

## Paper Table

| #   | Paper                                     | Year | Tier  | Depth        | Time   |
| --- | ----------------------------------------- | ---- | ----- | ------------ | ------ |
| 1   | Attention Is All You Need                 | 2017 | A1    | Architecture | 45 min |
| 2   | GPT-3: Few-Shot Learners                  | 2020 | A1    | Architecture | 60 min |
| 3   | Chain-of-Thought Prompting                | 2022 | A2    | Deep Read    | 40 min |
| 4   | Self-Consistency                          | 2022 | A2    | Architecture | 30 min |
| 5   | Toolformer                                | 2023 | A3    | Deep Read    | 45 min |
| 6   | MRKL Systems                              | 2022 | A3    | Architecture | 30 min |
| 7   | Gorilla: LLMs Connected with Massive APIs | 2023 | A3    | Architecture | 40 min |
| 8   | MemGPT                                    | 2023 | A4    | Deep Read    | 50 min |
| 9   | Generative Agents                         | 2023 | A4    | Deep Read    | 60 min |
| 10  | RAG: Retrieval-Augmented Generation       | 2020 | A5    | Deep Read    | 50 min |
| 11  | DPR: Dense Passage Retrieval              | 2020 | A5    | Architecture | 40 min |
| 12  | ColBERT: Late Interaction                 | 2020 | A5    | Architecture | 45 min |
| 13  | Self-RAG                                  | 2023 | A5    | Deep Read    | 50 min |
| 14  | HyDE: Hypothetical Documents              | 2022 | A5    | Architecture | 35 min |
| 15  | ReAct: Reasoning + Acting                 | 2022 | A6    | Deep Read    | 45 min |
| 16  | Reflexion                                 | 2023 | A6    | Deep Read    | 40 min |
| 17  | Tree of Thoughts                          | 2023 | A6    | Architecture | 40 min |
| 18  | Plan-and-Solve Prompting                  | 2023 | A6    | Architecture | 30 min |
| 19  | Constitutional AI                         | 2022 | A9    | Deep Read    | 55 min |
| 20  | MCP Specification                         | 2024 | A3/A6 | Deep Read    | 60 min |
| 21  | Mixture of Experts                        | 2022 | A1    | Architecture | 45 min |
| 22  | Llama 2                                   | 2023 | A1    | Architecture | 50 min |
| 23  | Direct Preference Optimization (DPO)      | 2023 | A9    | Architecture | 45 min |
| 24  | LoRA                                      | 2021 | A9    | Architecture | 35 min |
| 25  | Scaling Laws for Neural LMs               | 2020 | A1    | Architecture | 40 min |

**Total reading**: ~24 hours across the curriculum.

---

## Paper Entries

### 1. Attention Is All You Need (Vaswani et al., 2017)

**Tier**: A1. **Depth**: Architecture. **Time**: 45 min.
The transformer architecture. Introduces self-attention, multi-head attention, positional encoding, encoder-decoder structure. Foundation of every modern LLM. You don't need the math — you need to understand the _shape_: how attention lets each token look at every other token.
**Key concepts**: self-attention, multi-head attention, positional encoding, parallel training.

### 2. GPT-3: Language Models are Few-Shot Learners (Brown et al., 2020)

**Tier**: A1. **Depth**: Architecture. **Time**: 60 min.
Introduces in-context learning: models can perform tasks given only examples in the prompt, no fine-tuning. Explains few-shot, one-shot, zero-shot behavior. Explains why prompting works at all.
**Key concepts**: in-context learning, few-shot prompting, prompt sensitivity, model scaling.

### 3. Chain-of-Thought Prompting (Wei et al., 2022)

**Tier**: A2. **Depth**: Deep Read. **Time**: 40 min.
Shows that asking the model to "think step by step" dramatically improves reasoning accuracy. Birth of modern CoT prompting.
**Key concepts**: step-by-step reasoning, CoT accuracy gains, when CoT helps.

### 4. Self-Consistency (Wang et al., 2022)

**Tier**: A2. **Depth**: Architecture. **Time**: 30 min.
Sample multiple CoT answers, vote for the majority. Improves accuracy without any training.
**Key concepts**: sampling multiple answers, majority voting, reliability from diversity.

### 5. Toolformer (Schick et al., 2023)

**Tier**: A3. **Depth**: Deep Read. **Time**: 45 min.
Models learn to decide _when_ to call APIs (search, calculator, etc.). Foundation for modern tool calling.
**Key concepts**: tool selection, API calling, when to use tools.

### 6. MRKL Systems (Karpas et al., 2022)

**Tier**: A3. **Depth**: Architecture. **Time**: 30 min.
Modular Reasoning, Knowledge, and Language. Framework for combining LLMs with specialized modules (tools).
**Key concepts**: modular architecture, LLM as router, specialized tools.

### 7. Gorilla (Patil et al., 2023)

**Tier**: A3. **Depth**: Architecture. **Time**: 40 min.
LLMs that use massive API collections (1000+ tools). Shows how models navigate large tool sets.
**Key concepts**: large tool sets, API retrieval, tool selection at scale.

### 8. MemGPT (Packer et al., 2023)

**Tier**: A4. **Depth**: Deep Read. **Time**: 50 min.
LLM memory inspired by OS virtual memory. Treats the context window as "RAM" and external storage as "disk," with paging between them.
**Key concepts**: paging memory, function-based recall, infinite context via external storage.

### 9. Generative Agents (Park et al., 2023)

**Tier**: A4. **Depth**: Deep Read. **Time**: 60 min.
Simulated humans with memory, reflection, and planning. Foundational for agent memory architecture.
**Key concepts**: memory stream, reflection, retrieval by relevance, planning.

### 10. RAG: Retrieval-Augmented Generation (Lewis et al., 2020)

**Tier**: A5. **Depth**: Deep Read. **Time**: 50 min.
The original RAG paper. Combines a retriever and generator, trained jointly. Foundation of all modern RAG.
**Key concepts**: retrieval + generation, end-to-end training, grounding.

### 11. DPR: Dense Passage Retrieval (Karpukhin et al., 2020)

**Tier**: A5. **Depth**: Architecture. **Time**: 40 min.
Dense embeddings for passage retrieval. Superior to BM25 in many domains. Foundation for modern vector search.
**Key concepts**: dense embeddings, dual encoders, in-batch negatives.

### 12. ColBERT: Late Interaction (Khattab & Zaharia, 2020)

**Tier**: A5. **Depth**: Architecture. **Time**: 45 min.
Efficient retrieval with late interaction between queries and documents. Balance between fast retrieval and quality.
**Key concepts**: late interaction, max-sim operator, efficient reranking.

### 13. Self-RAG (Asai et al., 2023)

**Tier**: A5. **Depth**: Deep Read. **Time**: 50 min.
Models learn to decide _when_ to retrieve and _whether_ retrieved content is useful. Critical for production RAG.
**Key concepts**: retrieve-on-demand, self-critique, reflection tokens.

### 14. HyDE (Gao et al., 2022)

**Tier**: A5. **Depth**: Architecture. **Time**: 35 min.
Generate a hypothetical answer, embed that, retrieve against it. Improves retrieval for query-document mismatch.
**Key concepts**: hypothetical documents, embed generation, query expansion.

### 15. ReAct: Synergizing Reasoning and Acting (Yao et al., 2022)

**Tier**: A6. **Depth**: Deep Read. **Time**: 45 min.
The agent loop pattern. Interleave reasoning ("thinking") with actions ("tool calls"). Foundation for all modern agents.
**Key concepts**: thought-action-observation loop, tool use, agent reasoning.

### 16. Reflexion (Shinn et al., 2023)

**Tier**: A6. **Depth**: Deep Read. **Time**: 40 min.
Agents reflect on failures and improve without gradient updates. Verbal self-feedback loop.
**Key concepts**: self-reflection, failure learning, memory of mistakes.

### 17. Tree of Thoughts (Yao et al., 2023)

**Tier**: A6. **Depth**: Architecture. **Time**: 40 min.
Explore multiple reasoning paths, prune, backtrack. Extends CoT to search over thoughts.
**Key concepts**: tree search over reasoning, thought evaluation, backtracking.

### 18. Plan-and-Solve Prompting (Wang et al., 2023)

**Tier**: A6. **Depth**: Architecture. **Time**: 30 min.
Plan the approach before executing. Improves multi-step tasks vs CoT alone.
**Key concepts**: plan-then-solve, explicit planning, decomposition.

### 19. Constitutional AI (Bai et al., 2022)

**Tier**: A9. **Depth**: Deep Read. **Time**: 55 min.
Anthropic's approach to alignment: model critiques and revises itself using a constitution of principles. Foundation for safe AI systems.
**Key concepts**: self-critique, constitutional principles, RLAIF.

### 20. MCP Specification (Anthropic, 2024)

**Tier**: A3/A6. **Depth**: Deep Read. **Time**: 60 min.
The Model Context Protocol. Open standard for connecting agents to tools, resources, prompts. Read the spec directly.
**Key concepts**: hosts, clients, servers, tools, resources, prompts, transports.

### 21. Mixture of Experts (Fedus et al., 2022)

**Tier**: A1. **Depth**: Architecture. **Time**: 45 min.
Sparse models where only some parameters activate per token. Foundation for efficient frontier models.
**Key concepts**: sparse activation, routing, efficiency at scale.

### 22. Llama 2 (Touvron et al., 2023)

**Tier**: A1. **Depth**: Architecture. **Time**: 50 min.
Meta's open-weights LLM. Foundation for local model work (Ollama).
**Key concepts**: open weights, RLHF, chat-tuning, local deployment.

### 23. Direct Preference Optimization (Rafailov et al., 2023)

**Tier**: A9. **Depth**: Architecture. **Time**: 45 min.
Simpler alternative to RLHF. Aligns models using preference data without reward modeling.
**Key concepts**: preference optimization, simplified alignment, no RL.

### 24. LoRA: Low-Rank Adaptation (Hu et al., 2021)

**Tier**: A9. **Depth**: Architecture. **Time**: 35 min.
Efficient fine-tuning by training small adapter matrices. Foundation for practical fine-tuning.
**Key concepts**: low-rank adapters, parameter efficiency, fine-tuning on modest hardware.

### 25. Scaling Laws for Neural Language Models (Kaplan et al., 2020)

**Tier**: A1. **Depth**: Architecture. **Time**: 40 min.
Empirical laws relating model size, data, compute to performance. Explains why big models work.
**Key concepts**: scaling laws, compute-optimal training, emergent capabilities.

---

## Papers by Tier

**A1** (Foundations): 1, 2, 21, 22, 25
**A2** (Prompting): 3, 4
**A3** (Tools): 5, 6, 7, 20
**A4** (Memory): 8, 9
**A5** (Retrieval): 10, 11, 12, 13, 14
**A6** (Agents): 15, 16, 17, 18, 20
**A9** (Production): 19, 23, 24

---

## On-Demand Deep Dives

Say _"go deeper on [paper name]"_ → generates `paper-deep-dives/[slug].md` with:

1. 💡 Context & Why It Matters
2. 🔬 Technical Deep Dive
3. 📐 Diagrams / Schemas / Architecture
4. ⚠️ Trade-offs, Failure Modes & What Went Wrong
5. 🎯 What You Can Apply

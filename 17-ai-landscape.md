# AI Landscape

> Living document. Updated when a significant new tool, protocol, or model family arrives.
> Not speculative. Only concrete additions.
> **Last Updated**: `YYYY-MM-DD`

---

## How This File Works

Read it periodically (every 2–3 weeks). Update when you encounter something new during a session.

**Update workflow**:

1. Add the item to the appropriate section.
2. One-line description + why it matters.
3. Update the Last Updated date.

---

## Terminal / CLI Agents

| Tool            | Free Tier            | Notes                                    |
| --------------- | -------------------- | ---------------------------------------- |
| **Antigravity** | Free via Jio         | Primary agent                            |
| **Codex CLI**   | Free tier            | Secondary agent; sandboxed               |
| **Gemini CLI**  | 60 req/min, 1000/day | Open source; generous                    |
| **Claude Code** | Paid                 | Industry leader; awareness-level         |
| **WrenCode**    | Free                 | Minimal; single Python file; educational |
| **Amp**         | Pay-as-you-go        | Threads, subagents, multi-model          |

---

## IDE-Integrated AI

| Tool               | Free Tier           | Notes                            |
| ------------------ | ------------------- | -------------------------------- |
| **Cursor**         | 50 req/mo           | Most popular AI IDE              |
| **GitHub Copilot** | 2000 completions/mo | Most stable                      |
| **Windsurf**       | 25 credits/mo       | Formerly Codeium                 |
| **Zed**            | Free (BYOK)         | Rust-native; ACP for agents      |
| **Kilo Code**      | Free (BYOK)         | 500+ models; VS Code + JetBrains |
| **Cline**          | Free (BYOK)         | Open source; local model support |

---

## Code Review Tools

| Tool              | Free Tier         | Notes                                 |
| ----------------- | ----------------- | ------------------------------------- |
| **CodeRabbit**    | Free public repos | Most popular; best DX                 |
| **Greptile**      | Free Starter      | Repo-wide context                     |
| **Qodo**          | 14-day trial      | Multi-agent review + test generation  |
| **Cursor BugBot** | Requires Cursor   | Deep Cursor integration               |
| **Macroscope**    | $100 credit       | Codebase-aware; auto-approve safe PRs |
| **Snyk**          | Free tier         | Security scanning                     |
| **Semgrep**       | Open source       | Deterministic SAST                    |

---

## Research & Knowledge Tools

| Tool           | Free Tier | Notes                                 |
| -------------- | --------- | ------------------------------------- |
| **Perplexity** | Free      | AI search with citations              |
| **DeepWiki**   | Free      | AI-generated docs for GitHub repos    |
| **ChatGPT**    | Free      | General assistant                     |
| **Claude**     | Free      | Long-document analysis                |
| **Gemini**     | Free      | Google Workspace integration          |
| **Context7**   | Free      | Version-specific library docs via MCP |

---

## MCP Servers (Essential)

| Server                  | Notes                                   |
| ----------------------- | --------------------------------------- |
| **Context7**            | Live library docs; 52k+ stars           |
| **Playwright CLI**      | Browser automation; token-efficient     |
| **Chrome DevTools MCP** | Console, network, performance profiling |
| **GitHub MCP**          | PRs, issues, code search                |
| **Figma MCP**           | Design-to-code pipelines                |
| **Blender MCP**         | 3D control via Python API               |
| **Sequential Thinking** | Structured reasoning scratchpad         |
| **GitMCP**              | Turn any GitHub repo into MCP docs      |

---

## Skill Categories & Top Skills

### Frontend / UI / UX

- **UI/UX Pro Max** — 240+ styles, 99 UX guidelines
- **Taste Skill** — tunable variance/motion/density
- **design-skills (Cuellar)** — WCAG 2.2 audit methodology
- **design-auditor** — 17-point deterministic audit
- **frontend-design-pro** — 11 named aesthetics with demos

### Backend / API

- **api-and-interface-design (Addy Osmani)** — Hyrum's Law, deprecation strategy
- **improve-codebase-architecture (Matt Pocock)** — architectural deepening
- **schema-guard (Jeffallan)** — Zod/Prisma schema parity
- **rfc-architect** — CAP tradeoffs, QPS capacity planning

### Security

- **sast-skills (utkusen)** — 68 skills, 64 vuln classes
- **llm-sast-scanner (cujanovic)** — 106 vuln classes, adversarial judge
- **Trail of Bits Skills** — 28+ skills from a respected firm
- **openclaw-skill-vetter-mcp** — vets skills before install (mandatory)

### Code Comprehension

- **graphify** — knowledge graph from any input
- **codebase-memory-mcp (DeusData)** — 160+ languages, 10x fewer tokens
- **Code Graph RAG** — 11 languages, 26 MCP methods
- **ast-grep** — structural AST search
- **RepoMap** — token-efficient repo mapping

### 3D / Game Dev

- **cc-blender-skill (RobLe3)** — full 3D pipeline
- **Three.js Claude Skill Package** — 24 skills
- **Godot Skill (Shihab Shahrier)** — Godot 4.3+ enforcement
- **unity-game-skills (tea-x-random)** — Unity 6 workflow
- **Game Developer Skill (Jeffallan)** — Unity/Unreal/Godot

### Documentation

- **documentation-and-adrs (Addy)** — engineering-doc skill
- **ADR Skill (Joel Parker Henderson)** — 11 ADR formats
- **mermaid-diagrams (Magnus)** — technical diagrams

### Testing / Review

- **anthroos code-review** — 280+ checks; CodeRabbit alternative
- **Matt Pocock code-review** — two-axis review (spec + standards)
- **agentic-pr-evaluator (dudum-lab)** — 3 subagents + confidence >8/10
- **pypict-test-designer** — combinatorial testing

### Workflow / Planning

- **Superpowers (obra)** — brainstorm → spec → TDD → review
- **Matt Pocock Skills** — grilling → domain model → spec → issues
- **Addy Osmani Agent Skills** — Define → Plan → Build → Verify → Review → Ship
- **BMAD Method** — heavyweight multi-role planning

---

## Skill Discovery Sources

| Source                                  | Notes                                |
| --------------------------------------- | ------------------------------------ |
| **VoltAgent/awesome-agent-skills**      | 35k stars; cross-agent; 1000+ skills |
| **BehiSecc/awesome-claude-skills**      | 10k stars; Claude-focused            |
| **ComposioHQ/awesome-claude-skills**    | Curated; verified                    |
| **skills.sh**                           | Install telemetry leaderboard        |
| **mcp.directory**                       | 3000+ MCP servers + 9291 skills      |
| **Claude Code Frontend Design Toolkit** | 70+ frontend skills                  |
| **jeffallan/claude-skills**             | 65+ full-stack skills                |

---

## Free-Tier AI Providers

| Provider                       | Free Tier      | Notes                         |
| ------------------------------ | -------------- | ----------------------------- |
| **Google AI Studio (Gemini)**  | Generous       | Gemini 2.5 Flash + Pro        |
| **Groq**                       | Rate-limited   | Fastest inference             |
| **OpenRouter**                 | `:free` models | Multi-provider routing        |
| **Cerebras**                   | Rate-limited   | Hosted open models            |
| **Hugging Face Inference API** | Rate-limited   | Open models                   |
| **Ollama**                     | Local          | Zero cost; hardware-dependent |
| **llama.cpp**                  | Local          | Minimal hardware              |

---

## Model Families

| Family       | Notable Models          | Free Tier        | Notes                 |
| ------------ | ----------------------- | ---------------- | --------------------- |
| **GPT**      | GPT-4, GPT-5            | No               | OpenAI                |
| **Claude**   | Claude 4.5 Sonnet, Opus | No               | Anthropic             |
| **Gemini**   | 2.0, 2.5 Flash, Pro     | Yes (AI Studio)  | Google                |
| **Llama**    | Llama 3, 3.1            | Via Groq, Ollama | Meta; open weights    |
| **Qwen**     | Qwen 2.5, 3             | Via Groq, Ollama | Alibaba; open weights |
| **Mistral**  | Mistral, Mixtral        | Via Groq, Ollama | French; open weights  |
| **DeepSeek** | V3, R1                  | Via Groq, Ollama | Chinese; open weights |

---

## Protocol Standards

| Protocol                          | Status            | Notes                            |
| --------------------------------- | ----------------- | -------------------------------- |
| **MCP**                           | Active standard   | Anthropic; agents ↔ tools        |
| **A2A (Agent-to-Agent)**          | Emerging          | Google; agents ↔ agents          |
| **Agent Skills (agentskills.io)** | Emerging standard | Portable SKILL.md                |
| **OpenAI Function Calling**       | Legacy            | Superseded by structured outputs |
| **JSON Schema**                   | Universal         | Tool schemas                     |

---

## Recent Additions

> Add new items here as you encounter them. Format: `YYYY-MM-DD — [item] — [one-line why]`.

- `(empty)`

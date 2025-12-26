# GenAI Systems in Production

**Production-oriented designs and implementations of GenAI systems**, focused on
LLM inference, Retrieval-Augmented Generation (RAG), and agent-based architectures.

This repository documents **design decisions, trade-offs, and failure modes** encountered while
building real-world GenAI systems.


---

## System Areas Covered

### 1. LLM Inference Systems
**Goal:** Understand and control inference behavior in real deployments.

Topics include:
- Local LLM inference using Ollama
- Model selection and quantization trade-offs
- Latency vs throughput analysis
- When local inference fails to scale
- Cost and reliability considerations

Focus is on *when to use* local inference — and when **not** to.

---

### 2. Retrieval-Augmented Generation (RAG)
**Goal:** Build RAG systems that degrade gracefully instead of hallucinating confidently.

Implementations explore:
- Basic semantic RAG pipelines
- Hybrid retrieval (keyword + semantic)
- Reranking strategies
- Chunking trade-offs and context limits
- Retrieval evaluation beyond anecdotal testing

Includes analysis of common RAG failure modes:
- Context poisoning
- Retrieval sparsity
- Over-retrieval and distraction
- False confidence from partial context

---

### 3. Agent Architectures
**Goal:** Move beyond single-shot prompts toward goal-driven systems.

Patterns covered:
- Tool-using agents
- Multi-step reasoning loops
- Multi-agent coordination
- Agent failure handling and guardrails

Emphasis is placed on:
- Agent observability
- Error propagation
- Why agents fail silently in production

---

### 4. MCP-Based Integrations
**Goal:** Enable structured interaction between LLMs and external systems.

Examples include:
- SQL-based agents
- API-calling agents
- Controlled tool invocation via MCP patterns

Focus is on **system safety and determinism**, not agent autonomy for its own sake.

---

### 5. Real-World Case Studies
**Goal:** Bridge the gap between prototypes and business usage.

Contains:
- Client-style problem breakdowns
- System constraints and assumptions
- Design choices made under real deadlines
- What worked, what failed, and why

Sensitive details are abstracted, but **engineering decisions are preserved**.

---

## Design Philosophy

- **Systems > Models**  
  Models change. System behavior matters.

- **Evaluation > Demos**  
  If it cannot be measured, it cannot be trusted.

- **Failure-aware design**  
  The most dangerous GenAI systems are the ones that fail confidently.

- **Explicit trade-offs**  
  Every design decision documents what was sacrificed.

---

## Intended Audience

This repository is written for:
- Senior / Staff engineers working with GenAI
- Architects designing LLM-powered platforms
- Engineers transitioning from ML to GenAI systems
- Interviewers evaluating real-world GenAI experience


---

## How to Read This Repository

Each folder typically contains:
- A concise system overview
- Code focused on core logic
- Notes on trade-offs and failure modes
- Observations from practical usage

Start with:
- `01_llm_inference_engines/`
- then `02_rag_systems/`
- followed by `03_agent_architectures/`

---

## Author

Built and maintained by **Shiv**  
Senior GenAI / LLM Systems Engineer  
7+ years experience across ML, NLP, and production AI systems.

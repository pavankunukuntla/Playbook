---
title: "Specialty: AI Applications and Agents"
document_type: reference
category: "01-development-and-engineering"
status: proposed
owner: null
last_reviewed: null
related_documents:
  - "./README.md"
  - "../03-delivery-lifecycle/README.md"
  - "../04-engineering-standards/ai-assisted-development.md"
  - "../04-engineering-standards/security-and-privacy-engineering.md"
---

# Specialty: AI Applications and Agents

```yaml
specialty: ai-applications-and-agents
activation_status: unconfirmed
prescribed_stack: none # Intentionally unconfirmed
```

## 1. Purpose
Explores the candidate technical requirements, evaluation methods, security safeguards, and operational risks for building client deliverables incorporating Large Language Models (LLMs), Retrieval-Augmented Generation (RAG), and autonomous agents.

## 2. Proposed Scope
- LLM application architectures, prompt engineering pipelines, and context management.
- Retrieval-Augmented Generation (RAG) systems: vector databases, chunking strategies, embeddings, and hybrid search.
- Agentic systems: autonomous goal execution, multi-agent frameworks, tool use, and function calling.
- Model provider selection, API token cost management, latency optimization, and rate limiting.
- Quality evaluation: automated benchmarking, ground-truth eval sets, hallucination detection, and semantic drift monitoring.
- Security and data privacy: prompt injection defense, data redaction (PII filtering), zero-retention API policies, and sandboxed tool execution permissions.
- Human-in-the-loop (HITL) checkpoints and oversight mechanisms for consequential agent actions.

## 3. Applicability
Relevant when scoping, designing, building, or maintaining client deliverables that leverage generative AI models or agentic automation. (Activation status: **unconfirmed**).

## 4. Related Documents
- Shared Lifecycle: [`../03-delivery-lifecycle/README.md`](../03-delivery-lifecycle/README.md).
- Engineering Standards:
  - [`../04-engineering-standards/ai-assisted-development.md`](../04-engineering-standards/ai-assisted-development.md): Internal AI engineering practices.
  - [`../04-engineering-standards/security-and-privacy-engineering.md`](../04-engineering-standards/security-and-privacy-engineering.md): Data privacy and threat modeling.
  - [`../04-engineering-standards/testing-and-quality-engineering.md`](../04-engineering-standards/testing-and-quality-engineering.md): Non-deterministic testing strategies.

## 5. Specialty-Specific Research Questions
- What evaluation frameworks (e.g., Ragas, TruLens, DeepEval) provide actionable quality metrics for client RAG pipelines?
- How should autonomous agent tool-calling permissions be restricted to prevent unauthorized write/delete actions in production environments?
- What fallback architectures ensure business continuity when commercial model APIs experience outages, latency spikes, or sudden deprecations?

## 6. Known Unknowns
- Commercial pricing and profitability models for managing variable API token pass-through costs.
- Legal ownership of generated intellectual property and compliance with evolving AI regulations.
- Long-term maintainability of client RAG knowledge bases as source documents change.

## 7. Candidate Evidence and Artifacts
- RAG Quality & Semantic Retrieval Evaluation Benchmark.
- Prompt Injection & Data Redaction Security Test Suite.
- Agent Tool Permission Sandbox Architecture.

## 8. Next Action
Draft evaluation framework for RAG systems and define boundary policies for autonomous tool execution.

# Awesome AI Governance [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of frameworks, tools, papers, and standards for governing AI systems and AI agents — assurance, safety evals, red-teaming, policy guardrails, and tamper-evident audit trails.

AI is moving from models to autonomous agents. The hard question is no longer "can we build it?" but **"can we prove it's safe, compliant, and under control?"** This list collects the resources that answer that question — the standards auditors cite, the harnesses researchers trust, and the open-source tools builders actually ship with.

**How to use this list:** start with 📜 Frameworks & Standards to learn the language of AI assurance, pick an eval harness from 🧪 to measure your system, red-team it with 🎯, then put guardrails (🛡️), sandboxing (🧰), and audit trails (🔗) around it in production.

## Contents

- [📜 Frameworks & Standards](#-frameworks--standards)
- [🛡️ Policy Engines & Guardrails](#-policy-engines--guardrails)
- [🧪 Eval Harnesses](#-eval-harnesses)
- [🎯 Red-Teaming & Jailbreak Testing](#-red-teaming--jailbreak-testing)
- [🔗 Audit Trails & Provenance](#-audit-trails--provenance)
- [🧰 Agent Sandboxing & Kill Switches](#-agent-sandboxing--kill-switches)
- [📚 Papers & Books](#-papers--books)
- [🛠️ Open-Source Tools](#-open-source-tools)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

## 📜 Frameworks & Standards

The laws, standards, and voluntary frameworks that define what "responsible AI" means.

- [NIST AI Risk Management Framework (AI RMF 1.0)](https://www.nist.gov/itl/ai-risk-management-framework) — The voluntary US framework for managing AI risk across four functions: govern, map, measure, manage.
- [NIST Generative AI Profile (AI 600-1)](https://www.nist.gov/itl/ai-risk-management-framework/nist-generative-artificial-intelligence-profile) — Companion profile applying the AI RMF to generative AI risks such as confabulation, dangerous content, and data privacy.
- [EU AI Act](https://artificialintelligenceact.eu/) — The world's first comprehensive AI law: risk-based obligations from minimal risk to prohibited uses.
- [ISO/IEC 42001:2023](https://www.iso.org/standard/42001) — The international standard for AI management systems — plan-do-check-act for responsible AI.
- [ISO/IEC 23894:2023](https://www.iso.org/standard/77304.html) — Guidance on AI risk management for organizations developing or deploying AI.
- [OECD AI Principles](https://oecd.ai/en/ai-principles) — The intergovernmental standard for trustworthy AI, adopted by 40+ countries.
- [UK AI Safety Institute](https://www.gov.uk/government/organisations/ai-safety-institute) — The UK institute advancing frontier-model safety evaluations and research.
- [AI Verify Foundation](https://aiverifyfoundation.sg/) — Singapore's open-source testing toolkit and community for AI governance principles.

### 🌱 From my 500-repo build

- [eu-ai-act-mapper](https://github.com/ramtoo-cell/eu-ai-act-mapper) — Maps AI systems and use cases to EU AI Act risk tiers and obligations.

## 🛡️ Policy Engines & Guardrails

Enforce allow/deny rules on what models and agents can do — at the prompt, tool-call, and output layers.

- [Open Policy Agent](https://www.openpolicyagent.org/) — General-purpose policy engine; write allow/deny rules as code for any system, including agents.
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) — Programmable rails for LLM apps: topical, safety, and security guardrails via Colang.
- [Guardrails AI](https://github.com/guardrails-ai/guardrails) — Python framework for validating LLM outputs against schema-like rail specifications.
- [PurpleLlama](https://github.com/meta-llama/PurpleLlama) — Open trust & safety tooling including Llama Guard (input/output classifier) and CyberSecEval.
- [Rebuff](https://github.com/protectai/rebuff) — Self-hardening prompt-injection detector for LLM applications.

### 🌱 From my 500-repo build

- [agent-guardian](https://github.com/ramtoo-cell/agent-guardian) — AI agent governance sidecar: policy engine, budget guardrails, and a hash-chained audit log with red-team evals.
- [policy-engine](https://github.com/ramtoo-cell/policy-engine) — Declarative policy engine for constraining agent behavior at runtime.
- [agentgate](https://github.com/ramtoo-cell/agentgate) — Policy gateway for AI agents: allow/deny decisions at the tool-call boundary.

## 🧪 Eval Harnesses

Measure before you claim. Standard harnesses for benchmarking models and agents on safety, capability, and alignment.

- [LM Evaluation Harness](https://github.com/EleutherAI/lm-evaluation-harness) — The standard open framework for evaluating language models on 60+ benchmarks.
- [HELM](https://crfm.stanford.edu/helm/) — Stanford's Holistic Evaluation of Language Models: broad, multi-metric transparency.
- [Inspect](https://github.com/UKGovernmentBEIS/inspect_ai) — The UK AI Safety Institute's framework for LLM and agentic safety evaluations.
- [OpenAI Evals](https://github.com/openai/evals) — Framework for evaluating LLMs and systems, with a registry of community evals.
- [Ragas](https://github.com/explodinggradients/ragas) — Metrics and tooling for evaluating RAG pipelines.
- [DeepEval](https://github.com/confident-ai/deepeval) — Open-source LLM evaluation framework with 14+ metrics and red-teaming support.
- [Promptfoo](https://github.com/promptfoo/promptfoo) — CLI and library for testing prompts, models, and RAGs against repeatable test cases.
- [Vivaria](https://github.com/METR/vivaria) — METR's platform for running and scoring agentic evaluations.
- [BIG-bench](https://github.com/google/BIG-bench) — Beyond the Imitation Game: a collaborative benchmark of 200+ hard tasks for language models.
- [OpenCompass](https://github.com/open-compass/opencompass) — Open-source platform for large-model evaluation across 100+ datasets.

## 🎯 Red-Teaming & Jailbreak Testing

Think like the attacker. Frameworks and scanners for adversarial testing of AI systems.

- [MITRE ATLAS](https://atlas.mitre.org/) — Adversarial Threat Landscape for Artificial-Intelligence Systems: an ATT&CK-style matrix of AI attack techniques.
- [OWASP Top 10 for LLM Applications](https://genai.owasp.org/) — The top security risks for LLM apps, from prompt injection to insecure output handling.
- [garak](https://github.com/NVIDIA/garak) — LLM vulnerability scanner probing for jailbreaks, data leaks, and hallucinations.
- [PyRIT](https://github.com/Azure/PyRIT) — Python Risk Identification Toolkit for automating red-team operations against generative AI.
- [JailbreakBench](https://github.com/JailbreakBench/jailbreakbench) — Open benchmark for evaluating jailbreak attacks and defenses.
- [HarmBench](https://www.harmbench.org/) — Standardized evaluation framework for automated red teaming and robust refusal.

### 🌱 From my 500-repo build

- [jailbreak-fuzzer](https://github.com/ramtoo-cell/jailbreak-fuzzer) — Fuzzer for probing LLM jailbreak and prompt-injection weaknesses.

## 🔗 Audit Trails & Provenance

If it isn't logged, it didn't happen. Standards and primitives for tamper-evident records of what AI systems did.

- [C2PA](https://c2pa.org/) — Coalition for Content Provenance and Authenticity: open standard for certifying the origin of digital content.
- [in-toto](https://in-toto.io/) — Framework for securing software supply chains with verifiable, signed attestations.
- [SLSA](https://slsa.dev/) — Supply-chain Levels for Software Artifacts: standards and tooling for build integrity.
- [Sigstore](https://www.sigstore.dev/) — Keyless signing, certificate transparency, and timestamping for software artifacts.
- [The Update Framework (TUF)](https://theupdateframework.io/) — Specification for securing software update systems against repository compromise.
- [OpenTelemetry](https://opentelemetry.io/) — Vendor-neutral observability (traces, metrics, logs): the backbone of agent audit trails.

### 🌱 From my 500-repo build

- [audit-trail](https://github.com/ramtoo-cell/audit-trail) — Tamper-evident, hash-chained audit trail for agent actions.

## 🧰 Agent Sandboxing & Kill Switches

Contain the blast radius. Isolation runtimes and emergency controls for agents that act in the world.

- [E2B](https://github.com/e2b-dev/e2b) — Open-source sandboxed code-execution environments built for AI agents.
- [gVisor](https://github.com/google/gvisor) — Application kernel providing strong, lightweight container sandboxing.
- [Firecracker](https://github.com/firecracker-microvm/firecracker) — Lightweight microVMs for secure, fast workload isolation.
- [nsjail](https://github.com/google/nsjail) — Process isolation tool using Linux namespaces, seccomp, and capabilities.
- [Firejail](https://github.com/netblue30/firejail) — Lightweight SUID sandbox using Linux namespaces and seccomp-bpf.

### 🌱 From my 500-repo build

- [kill-switch](https://github.com/ramtoo-cell/kill-switch) — Emergency kill switch and containment controls for runaway agents.
- [mcp-server](https://github.com/ramtoo-cell/mcp-server) — Sandboxed MCP server template for tool-calling agents.

## 📚 Papers & Books

The ideas behind the tooling — from the founding agenda to modern agent-safety results.

- [Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565) — Amodei et al. (2016): the agenda-setting paper on AI safety research directions.
- [A Taxonomy of Risks Posed by Language Models](https://arxiv.org/abs/2112.04359) — Weidinger et al. (2022): a structured map of language-model harms.
- [Constitutional AI: Harmlessness from AI Feedback](https://arxiv.org/abs/2212.08073) — Bai et al. (2022): training harmless assistants with AI feedback and constitutions.
- [Sleeper Agents](https://arxiv.org/abs/2401.05566) — Hubinger et al. (2024): deceptive models whose backdoors persist through safety training.
- [Human Compatible](https://en.wikipedia.org/wiki/Human_Compatible) — Stuart Russell's book on aligning AI with human values.
- [The Alignment Problem](https://en.wikipedia.org/wiki/The_Alignment_Problem) — Brian Christian's narrative tour of machine-learning safety research.
- [Superintelligence: Paths, Dangers, Strategies](https://en.wikipedia.org/wiki/Superintelligence:_Paths,_Dangers,_Strategies) — Nick Bostrom's foundational book on advanced AI risk.

## 🛠️ Open-Source Tools

Production-grade open-source tooling for observing, tracing, and governing AI systems.

- [Langfuse](https://github.com/langfuse/langfuse) — Open-source LLM engineering platform: tracing, evals, and prompt management.
- [OpenLLMetry](https://github.com/traceloop/openllmetry) — OpenTelemetry-based observability for LLM applications.
- [AgentOps](https://github.com/AgentOps-AI/agentops) — Session replay, monitoring, and analytics for AI agents.
- [Phoenix](https://github.com/Arize-ai/phoenix) — Open-source AI observability: tracing, evaluation, and experimentation for LLM apps.

### 🌱 From my 500-repo build

- [agent-guardian](https://github.com/ramtoo-cell/agent-guardian) — AI agent governance sidecar: policy engine, budget guardrails, and a hash-chained audit log with red-team evals.

## 🤝 Contributing

Suggestions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## 📄 License

This list is released under the MIT License — see [LICENSE](LICENSE) for details.

---

*Curated by [Ramkumar Bharathan](https://github.com/ramtoo-cell). If this list helped you, please ⭐ star it — and PRs are always welcome.*

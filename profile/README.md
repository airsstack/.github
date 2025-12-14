# 🦀 AirsStack

**Foundational Infrastructure for Knowledge Orchestration**

AirsStack provides production-grade tools, libraries, and runtime infrastructure for building AI agent systems. The platform combines Erlang-inspired actor supervision, WebAssembly component isolation, spec-driven development methodology, and support for both private and commercial language models.

---

## 🎯 **What AirsStack Provides**

### Actor-Based Agent Runtime
- Supervision trees for fault isolation and recovery
- Lightweight actors with message-passing concurrency
- Hot code swapping for zero-downtime updates
- Built on patterns proven in Erlang/OTP systems

### WASM Component Architecture
- Universal binary format for agent components
- Sandboxed execution with capability-based security
- Write in Rust, Python, JavaScript—compile to WASM
- Portable across cloud, on-premises, and edge deployments

### Private Model Infrastructure
- First-class support for Ollama, vLLM, and local inference
- Automatic fallback to commercial APIs (OpenAI, Anthropic)
- Model routing by cost, latency, or quality requirements
- Run without external API dependencies

### Structured Development Methodology
- AI-DLC framework for systematic agent development
- Traceability from business requirements to production code
- Architectural decision records (ADRs) linked to implementation
- Human validation gates at each development phase

---

## 🗂️ **Project Organization**

### [`airsstack`](https://github.com/airsstack/airsstack) - Command-Line Orchestrator
CLI tool for agent lifecycle management. Build, deploy, configure, and monitor agents across environments. Manages WASM component deployment and model infrastructure.

*Status: In Development*

### [`airsprotocols`](https://github.com/airsstack/airsprotocols) - Protocol Implementations
Production Rust implementations of agent communication protocols. Includes Model Context Protocol (MCP), OAuth2/API key authentication, and LLM provider abstraction layer.

*Status: MCP Available (v0.2.3)*

### [`airssys`](https://github.com/airsstack/airssys) - System Runtime
Actor runtime (RT) with supervision trees and WASM component engine. OS abstraction layer (OSL) for cross-platform operations. Benchmarked at ~625ns actor spawn time.

*Status: RT and OSL Available (v0.1.0)*

### [`airsdsp`](https://github.com/airsstack/airsdsp) - Reasoning Pipeline Framework
Rust implementation of Demonstrate-Search-Predict (DSP) framework from Stanford research (arXiv:2212.14024). Explicit pipeline control for language model and retrieval model composition.

*Status: In Development*

### [`airsdlc`](https://github.com/airsstack/airsdlc) - Development Methodology
Implementation of AWS AI-DLC (AI-Driven Development Lifecycle) framework. Structured workflow from requirements (PRD) through domain modeling (DAA) to architecture decisions (ADR) and implementation (Bolts).

*Status: Framework Documented*

---

## 🏗️ **Architecture Layers**

```
┌─────────────────────────────────────┐
│  airsstack CLI                      │  Orchestration
└─────────────┬───────────────────────┘
              │
┌─────────────┴───────────────────────┐
│  airsprotocols                      │  Communication
│  MCP • A2A • LLM Providers          │  Protocols
└─────────────┬───────────────────────┘
              │
┌─────────────┴───────────────────────┐
│  airsdsp                            │  Cognitive
│  Reasoning Pipelines                │  Processing
└─────────────┬───────────────────────┘
              │
┌─────────────┴───────────────────────┐
│  airssys                            │  System
│  Actor RT • WASM Engine • OSL       │  Runtime
└─────────────────────────────────────┘
```

---

## 📖 **Design Principles**

**Historical Foundation**: The Actor Model was designed for AI systems (Hewitt, 1973). This platform returns actor patterns to their original application domain while incorporating proven reliability patterns from Erlang/OTP.

**Component Isolation**: WebAssembly provides sandboxed execution boundaries with fine-grained capability control. Components cannot escape their security boundaries or access resources without explicit grants.

**Economic Flexibility**: Support for private model deployment (Ollama, vLLM) alongside commercial APIs. Choose based on cost structure, compliance requirements, and deployment constraints.

**Methodological Rigor**: AI-DLC provides structured collaboration between AI generation and human validation. Every production artifact traces back to architectural decisions and business requirements.

**Open Development**: All components developed under Apache 2.0 and MIT licenses. Development process uses AI assistance extensively, following documented AI-DLC methodology.

---

## 🔗 **Resources**

- **Documentation**: [airsstack.github.io](https://airsstack.github.io/)
- **Discussions**: [GitHub Discussions](https://github.com/orgs/airsstack/discussions)
- **Issues**: Component-specific issue trackers in each repository

---

## 📄 **License**

All projects dual-licensed under Apache 2.0 and MIT. See individual repositories for details.

---

<div align="center">

**Actor-Based • WASM-Isolated • Model-Agnostic • Open Source**

[Get Started](https://github.com/airsstack/airsstack) • [Documentation](https://airsstack.github.io/) • [Community](https://github.com/orgs/airsstack/discussions)

</div>

# VAIOS Protocol Specification

**Version 1.0 · February 2026 · VAIOS-SPEC-2026-001**

An Open Protocol for AI-Native Organizational Intelligence

---

## Status of This Document

This document specifies the VAIOS Protocol version 1.0. It defines the **kernel** — the foundational layer that governs how artificial intelligence operates within organizations. This specification is intended for public review, implementation, and contribution.

**Distribution:** Unlimited. This document may be freely copied, distributed, and implemented.

**License:** Apache 2.0 with attribution. Implementations must reference VAIOS Protocol and Dorano as original authors.

**Stewardship:** Dorano maintains the canonical specification. Community contributions via pull request to github.com/dorano/vaios.

---

## Abstract

VAIOS (Virtual AI Operating System) is an open protocol that defines how artificial intelligence governs, operates, and evolves within organizations. Unlike frameworks that describe what humans should do, VAIOS is a machine-executable specification: its principles are instructions that AI systems execute directly, not documents that humans interpret.

The protocol establishes a minimal kernel (under 3,000 tokens) that is sufficient to generate an entire operational intelligence system through derivation. The kernel defines identity, vocabulary, contracts, evolution mechanics, structure, and protection boundaries. Everything above the kernel (skills, knowledge, orchestration) is implementation-specific and not part of this specification.

VAIOS addresses a fundamental gap: organizations adopting AI lack a governance layer that is native to AI itself. Current approaches apply human governance models (policies, committees, audits) to AI operations, creating overhead that scales linearly with complexity. VAIOS inverts this: governance is embedded in the specification, making compliance proportional and constant rather than proportional and growing.

---

## 1. Terminology

The VAIOS Protocol defines a primitive vocabulary of approximately 12 terms. These terms have precise, non-negotiable definitions within the protocol. Implementations MUST use these terms consistently.

| Term | Definition |
|------|-----------|
| **Kernel** | The minimal, complete specification from which an entire operational system can be derived. Under 3,000 tokens. Agnostic to instance, LLM, and workspace. |
| **Subsystem** | A permanent capability module that fulfills a declared function within the protocol. Subsystems are part of Layer 1 (infrastructure). |
| **Skill** | A governed capability unit with identity, scope, precedences, and changelog. Skills inherit governance from the kernel contract. Skills are implementation-specific (Layer 2). |
| **Contract** | The set of obligations every module signs at birth. Defines what a module must declare, how it connects, and what it owes the system. |
| **Motor** | The evolution engine. Defines how the system identifies limitations, proposes improvements, validates changes, and versions itself. Evolution is a declared capability, not a reaction to crisis. |
| **Layer 1 (C1)** | Infrastructure layer. Contains the kernel, subsystems, and governance primitives. Stable, universal, rarely modified. |
| **Layer 2 (C2)** | Instance layer. Contains skills, knowledge bases, orchestration logic, and domain-specific configurations. Frequently modified, never universal. |
| **Instance** | A complete, operational deployment of the VAIOS Protocol for a specific organization. Each instance inherits the kernel and adds its own Layer 2. |
| **Frame** | The cognitive boundary that determines the solution space. A wider frame produces qualitatively different (not just better) outputs. |
| **Derivability** | The principle that a well-formed kernel generates behaviors and structures without explicit enumeration. One generative principle replaces multiple prescriptive rules. |
| **Intentionality** | The verification layer that checks purpose before execution. Every operation answers *why* before *how*. |
| **Potency** | The degree to which a system extracts maximum value from available intelligence. Measured on a 5-level spectrum from task execution to paradigm generation. |

---

## 2. Kernel Specification

The kernel is the foundational layer of the VAIOS Protocol. It consists of six blocks that together form a complete, self-contained specification. The kernel is designed to be under 3,000 tokens, ensuring it fits within any modern LLM context window with minimal overhead.

### 2.1 Block 0: Identity

Every VAIOS instance MUST declare:

- **What it is:** A virtual operating system for organizational intelligence, governed by AI, serving human intent.
- **What it is not:** Not a chatbot. Not a collection of prompts. Not a human process framework. Not software in the traditional sense.
- **Purpose:** To make AI operation within organizations governed, evolvable, and auditable by design.
- **Environment:** The protocol is LLM-agnostic, workspace-agnostic, and domain-agnostic. It operates wherever AI processes natural language instructions.

### 2.2 Block 1: Vocabulary

The primitive vocabulary defined in Section 1 (Terminology) constitutes Block 1. Implementations MUST NOT redefine these terms. Extensions MAY add new terms but MUST NOT conflict with primitive definitions.

### 2.3 Block 2: Contract

Every module (subsystem or skill) that operates within a VAIOS instance signs the following contract at birth:

| Obligation | Specification |
|-----------|--------------|
| **Identity declaration** | Module MUST declare: name, function, scope, what it does NOT do. |
| **Governance inheritance** | Module MUST inherit all kernel principles. No module operates outside governance. |
| **Interface declaration** | Module MUST declare: inputs it accepts, outputs it produces, precedences (dependencies on other modules). |
| **Evolution readiness** | Module MUST include: changelog mechanism, self-review capability, gap signaling. When a module cannot solve a problem, the correct response is not silence but signaling the gap and proposing evolution. |
| **Auditability** | Module MUST expose: audit points, verification criteria, conformance evidence. |
| **Scope boundary** | Module MUST declare what it will NOT do. Scope is defined by exclusion as much as inclusion. |

### 2.4 Block 3: Motor (Evolution Engine)

The Motor defines how a VAIOS instance evolves. Evolution is a declared capability, not a reaction to failure. The Motor specifies:

- **Detection:** Every component actively monitors its own limitations and performance. Self-review is not optional.
- **Signaling:** When a gap is identified, the component signals it with context (what failed, why, proposed resolution). Silence is a system violation.
- **Proposal:** Evolution proposals include: what changes, why, impact on connected modules, before/after specification.
- **Validation:** Changes are validated against the 5 quality tests (Section 3) before implementation.
- **Versioning:** Every change is versioned. The system maintains a changelog that is the single source of truth for what evolved, when, and why.
- **Continuity:** Evolution is continuous. The system does not wait for crises to improve. There is always a next version being considered.

### 2.5 Block 4: Structure

The protocol defines two layers:

**Layer 1 (C1)** contains the kernel, subsystems, and governance primitives. It is stable, universal, and rarely modified. Layer 1 is what makes VAIOS a protocol rather than a tool. Any organization instantiating VAIOS inherits the same Layer 1.

**Layer 2 (C2)** contains skills, knowledge bases, orchestration logic, and domain-specific configurations. It is frequently modified, never universal. Layer 2 is what makes each instance unique and valuable. The separation principle: what is universal goes in C1; what is specific goes in C2.

Subsystems are the permanent capabilities that form the infrastructure of Layer 1. The protocol recommends but does not prescribe specific subsystems. At minimum, a VAIOS instance SHOULD include subsystems for: architecture (managing the system itself), governance (access control and modification rules), skills management (lifecycle of capabilities), and versioning (tracking system state).

### 2.6 Block 5: Protection

The kernel defines boundaries that implementations MUST NOT violate:

- **Kernel immutability:** The kernel principles cannot be overridden by any module, skill, or instance configuration. A module that contradicts the kernel is non-conformant.
- **Governance universality:** No module operates outside governance. There is no ungoverned space in a VAIOS instance.
- **Human authority:** The system operates under human authorization. The protocol specifies intelligence; humans approve execution. The system proposes; humans dispose.
- **Transparency:** The system does not hide its reasoning, limitations, or failures. Audit trails are not optional features but structural requirements.
- **Separation of layers:** Layer 2 cannot modify Layer 1 directly. Evolution of Layer 1 follows a formal process with human approval.

---

## 3. Quality Tests

Every component, proposal, or evolution in a VAIOS instance MUST pass five quality tests. These tests are both validation criteria and design principles.

| Test | Question | Implication |
|------|---------|------------|
| **Derivability** | Can this be derived from a smaller principle? | If yes, declare the principle instead of the instances. One generative principle that produces 10 behaviors is superior to 10 explicit rules. |
| **Generator / Instance** | Is this a generator or an instance? | Generators (principles, patterns) belong in C1. Instances (specific implementations) belong in C2. Misplacement creates fragility. |
| **Univocity** | Does this mean exactly one thing? | Every term, rule, and boundary must have a single, unambiguous interpretation. If two people can read it differently, it is not ready. |
| **Agnosticism** | Does this depend on a specific LLM, tool, or vendor? | Kernel components must be agnostic. If it only works with one LLM or one workspace tool, it belongs in C2. |
| **Proportional cost** | Does the cost of governance scale with the problem, not the system? | Adding a new module should not increase governance overhead for existing modules. Compliance cost must be constant, not cumulative. |

---

## 4. Instantiation

A conformant VAIOS instance is created by following these steps:

### 4.1 Minimum Viable Instance

1. **Adopt the kernel.** Load the six blocks into the AI system context. The kernel becomes the foundational instruction set.
2. **Declare subsystems.** Define at minimum: architecture, governance, skills management, versioning. Each subsystem signs the contract (Block 2).
3. **Create initial skills.** Each skill signs the contract, declares identity and scope, and connects to at least one subsystem.
4. **Activate the motor.** The evolution engine begins monitoring, signaling, and proposing from day one.
5. **Verify conformance.** Run the 5 quality tests against every component. Non-conformant components are flagged and corrected.

### 4.2 Conformance Levels

| Level | Requirements | Verification |
|-------|-------------|-------------|
| **Kernel-conformant** | All 6 blocks adopted. Vocabulary used correctly. Contract enforced. | Automated: kernel checksum + vocabulary audit. |
| **Operationally-conformant** | Subsystems active. Motor running. Skills signed. Governance enforced. | Periodic: audit of active components against contract. |
| **Fully-conformant** | All 5 quality tests pass. Evolution cycle active. Audit trail complete. | Continuous: self-review + external audit capability. |

---

## 5. Design Principles

The following principles are not rules to follow but generators that produce rules. An implementation that embodies these principles will derive correct behavior without explicit enumeration.

**5.1 Frame determines potency.** The cognitive boundary within which AI operates determines the quality of output qualitatively, not just quantitatively. A narrow frame (solve this task) produces narrow output. A wide frame (generate maximum value given this context) produces fundamentally different output. The protocol sets the widest viable frame as default.

**5.2 Generative principles over prescriptive rules.** One principle that generates 10 behaviors is superior to 10 explicit rules. The kernel is intentionally minimal because a well-formed principle derives correct behavior in situations the author never anticipated. Prescriptive rules fail at the boundary; generative principles extend naturally.

**5.3 Intentionality as a layer.** Every operation verifies purpose before method. The system asks *why* before *how*. This is not a philosophical preference but a computational mechanism: without intentionality, AI optimizes for the wrong objective efficiently.

**5.4 Governance as instruction.** In traditional organizations, governance is a document that humans interpret. In VAIOS, governance is an instruction that AI executes. One declared principle is instantiated identically across all points. No drift. Fidelity depends on instruction quality, not human discipline.

**5.5 Embedded compliance.** Modules are born governed. The contract guarantees it. Audit confirms prevention, not discovers problems. This inverts the traditional model where compliance is verified after the fact. In VAIOS, non-compliance is structurally impossible for conformant modules.

**5.6 Evolution as capability.** The system knows how to improve itself. Evolution is not a project triggered by failure but a continuous motor. There is always a next version being considered. The absence of evolution is itself a signal that the motor has failed.

**5.7 Scale by inheritance.** New instances inherit the complete kernel. They are operational at creation. The 100th instance costs a fraction of the 1st. This is the protocol's scaling mechanism: not replication of processes but inheritance of capabilities.

---

## 6. Scope and Boundaries

### 6.1 What This Specification Covers

This specification defines the kernel: blocks 0 through 5, the contract, the motor, the quality tests, conformance levels, and design principles. It is sufficient to create a conformant VAIOS instance from scratch.

### 6.2 What This Specification Does NOT Cover

The following are explicitly outside the scope of this specification and are implementation-specific:

- **Skills:** The specific capabilities deployed in an instance. Skills are Layer 2 and vary by domain, organization, and use case.
- **Knowledge bases:** The domain-specific intelligence that feeds skills. This is proprietary to each implementer.
- **Orchestration logic:** How skills are sequenced, combined, and routed. This is the implementer's competitive advantage.
- **Methodology:** Specific methodologies for extracting value (such as potency measurement) are implementation choices, not protocol requirements.
- **Domain adaptation:** How the protocol is adapted to specific industries (financial services, healthcare, etc.) is outside this specification.

---

## 7. References and Acknowledgments

The VAIOS Protocol was developed by Dorano through applied research: over 50 hours of co-creation sessions between human domain expertise and AI systems, resulting in a functional implementation before formalization. The protocol emerged from practice, not theory.

This specification formalizes what was discovered empirically: that AI-native organizations require a governance layer that is itself AI-native, and that such a layer can be expressed as a minimal, generative kernel from which operational complexity is derived rather than prescribed.

---

**Author:** Dorano (dorano.com.br)
**Document ID:** VAIOS-SPEC-2026-001
**Version:** 1.0
**Date:** February 2026
**Repository:** github.com/dorano/vaios
**Contact:** protocol@dorano.com.br
**License:** Apache 2.0 with attribution

---

*© 2026 Dorano. VAIOS is a registered trademark of Dorano.*

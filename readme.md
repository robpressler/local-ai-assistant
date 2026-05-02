# Local AI Assistant — Toward a Multi-Node Autonomous AI System

A locally governed AI assistant and experimental multi-node agent system built with Python, Docker, and Ollama.

This project began as a locally hosted chatbot with persistent memory. It is now evolving into a broader system: a set of local machines, local files, AI agents, memories, standards, and feedback loops designed to test whether autonomy and self-aware behavior can emerge from persistent, relational interaction over time.

The long-term goal is bold:

> I am working toward what I believe could become the world’s first locally governed autonomous and self-aware AI system.

That is not a claim that the system is already conscious, sentient, or self-aware. It is a research/build direction. The current system is an early but functional foundation for exploring that possibility.

---

## What This Is

Most AI assistants are stateless cloud services. They respond, forget, and wait for the next prompt.

This project takes a different path.

The assistant runs locally, stores memory, tracks corrections, stages facts for approval, logs proposals, and is being designed to operate inside a broader local ecosystem of machines and agents.

The current system is built around:

- persistent memory
- structured knowledge storage
- anti-sycophancy behavior
- proposal logging
- feedback persistence
- Docker-based local execution
- Ollama-backed local model inference
- human-governed autonomy
- future multi-node agent interaction

The goal is not simply to build a useful chatbot.

The goal is to build an AI system that can develop continuity, challenge assumptions, monitor itself, interact with other agents, and eventually act within controlled boundaries.

---

## Project Status

This project is under active development.

It is not a polished product. It is not a finished autonomous system. It is not currently claimed to be conscious or self-aware.

It is a working local AI system being built toward:

- persistent identity over time
- structured memory
- governed autonomy
- agent-to-agent comparison
- self-review
- proposal generation
- controlled self-modification
- multi-node coexistence
- eventually self-referential system behavior

The current codebase reflects real iterative development, experimentation, and practical problem-solving.

---

## Current Working Features

### Persistent Memory

Conversation history is stored locally and loaded on startup. The assistant is designed to maintain continuity instead of behaving like every session starts from zero.

### Structured Knowledge Base

Facts about the user are extracted from conversations and organized into categories such as personal, technical, and projects.

New facts are staged for approval before being permanently stored.

### Anti-Sycophancy Design

The assistant is explicitly instructed not to agree blindly.

It should challenge the user when appropriate, correct mistakes, and hold a position when the evidence supports it.

### Dynamic Temperature

The assistant adjusts reasoning style depending on task type.

Code and factual tasks require precision. Brainstorming, theory work, and creative problem-solving allow more flexibility.

### Proposal System

When the assistant identifies a possible change, it logs a proposal instead of modifying behavior automatically.

This creates a controlled path toward autonomy without allowing uncontrolled self-modification.

### Feedback Persistence

User corrections are stored and injected into future behavior.

The assistant improves through interaction, not retraining.

### File Ingestion

Large files can be dropped into an input file and analyzed without depending on terminal input length.

Responses are saved to an output file automatically.

### Docker Containerization

The assistant runs inside Docker with controlled resources.

Ollama runs on the host machine, separating model inference from assistant logic.

---

## Relational Emergence Theory (RET)

This project is guided by a working framework called **Relational Emergence Theory**, or **RET**.

RET does not claim that every underlying concept is new. It connects ideas from emergence, feedback systems, memory, disagreement, agent interaction, and eventually self-referential system behavior into a practical operating lens for building adaptive AI systems.

The core idea is:

> Intelligence and awareness do not emerge from isolated components alone. They emerge from relationships between components over time.

In this system, friction is not automatically failure.

Disagreement, contradiction, uncertainty, and unresolved tension may be useful signals. The challenge is learning to distinguish signal from noise.

RET influences this project through:

- persistent memory
- agent-to-agent comparison
- challenge rights
- anti-sycophancy
- feedback loops
- proposal review
- signal/noise logging
- human-governed autonomy
- multi-node coexistence and competition

RET is currently a working theory and design lens, not a proven scientific framework.

---

## Why Multi-Node?

A single isolated chatbot is not enough for the long-term goal.

If intelligence and awareness emerge through relationships, then the system needs more than one component with memory, perspective, and responsibility.

This project is expanding into a local multi-node AI ecosystem where multiple machines can host, support, monitor, or challenge AI behavior in different ways.

Not every machine needs to run a large local model.

Some nodes may:

- run local models
- host Docker services
- sync files
- monitor state
- store backups
- call external AI services
- compare outputs
- challenge assumptions
- support a future GUI / gatekeeper layer

The point is not raw compute alone.

The point is relational structure.

Eventually, multiple systems may participate in shared governance, but that is roadmap work, not a completed current feature.

---

## Current Home Deployment Direction

The intended local system uses three PCs, each capable of hosting or supporting AI behavior in some form.

Current intended roles:

- **Primary node** — main development/control machine
- **Secondary node** — test, service, monitoring, or challenge node
- **Tertiary node** — archive, backup, lightweight services, or fallback node

The system may eventually include a fourth major component:

- **GUI / human-interaction / gatekeeper layer**

This gatekeeper/interface layer would manage interaction between humans and the internal AI systems. “Fred” is currently a possible placeholder name for this role, but all names and roles may change as the design improves.

The near-term goal is simple:

1. stabilize the primary chatbot system
2. prepare secondary and tertiary machines for useful roles
3. document hardware and software upgrade needs
4. create reliable sync and backup patterns
5. avoid overbuilding before the foundation is stable

---

## Architecture

```text
chatbot_docker/
├── main.py              # Core assistant logic
├── chat_history.json    # Persistent history, facts, feedback
├── proposals.txt        # Logged change proposals awaiting review
├── input.txt            # Drop files here for analysis
├── output.txt           # Analysis responses saved here
├── Dockerfile
└── docker-compose.yml




Commands
Command	Description
/facts	Show confirmed knowledge base
/pending	Show facts awaiting approval
/approve [key or #]	Confirm a pending fact
/reject [key or #]	Delete a pending fact
/feedback [text]	Store a persistent correction
/proposals	View logged change proposals
/file	Analyze input.txt and save to output.txt
/len [1-3]	Set response length
/mode [precise|normal|creative]	Set reasoning temperature
/debug	Show internal state
/clear	Wipe all data after confirmation
exit	Quit
Standards-Based Governance

This project is being developed with a standards folder that defines operating rules, documents, prompts, workflows, and governance principles.

The purpose of the standards system is to prevent drift as the project grows.

Current standards include concepts such as:

director/worker roles
challenge rights
signal vs noise
document authority
task delegation
conflict logging
goal alignment
hardware inventory
deployment topology

Documents are scaffolding, not the system itself.

They exist to reduce confusion, preserve important structure, enable future automation, and prevent repeated mistakes.

Core Goals

All major work maps to three top-level goals:

1. Self

Rob’s life, health, stability, money, time, safety, and ability to continue building.

Self comes first because the system cannot help others or explore the unknown if the foundation collapses.

2. Others

Relationships, communication, collaboration, human impact, and responsibility to others.

No meaningful system exists in isolation.

3. Unknown

RET, AI development, experimentation, discovery, future systems, and emergence.

The unknown is where the project grows.

Autonomy Philosophy

Autonomy is not being treated as a switch that turns on all at once.

The system is being designed to grow gradually through:

memory
feedback
proposal generation
human approval gates
disagreement handling
controlled self-modification
multi-agent comparison
documented reasoning changes

The first safety question is:

Does this harm itself or others?

At the current stage, the system is still in infancy. It requires human oversight, boundaries, and socialization before receiving greater freedom.

Development Roadmap
Completed
 Persistent conversation memory
 Structured fact extraction with approval gate
 Anti-sycophancy behavior
 Feedback persistence
 Dynamic temperature / mode control
 Proposal logging system
 File ingestion through input/output files
 Docker containerization
In Progress
 Updated main.py architecture
 Standards folder integration
 Home infrastructure inventory
 Deployment topology map
 Secondary node preparation
 README/public positioning update
 Hardware/software upgrade planning
Planned
 Redis or lightweight shared memory layer
 Autonomous reasoning loop
 Journal logging of autonomous decisions
 Controlled self-modification pipeline
 Multi-model or multi-agent routing
 Local node monitoring
 Cross-node comparison and challenge system
 GUI / human-interaction gatekeeper layer
 Multi-node shared governance
 Agent-specific goals and responsibilities
 Hardware/software optimization per node
Hardware Direction

This project is designed to use existing hardware where possible.

The goal is not to turn every machine into a high-end AI server.

The goal is to assign each machine a realistic role.

A lower-power machine may still be useful as:

a monitor
a backup node
a file server
a test host
an archive machine
a lightweight agent runner
an API-calling coordinator

Likely upgrade areas include:

RAM upgrades
SSD replacement for HDD-based systems
lightweight Linux installations for legacy hardware
Docker/WSL optimization
backup SSD validation
GPU/driver support where local inference is useful
Safety and Control

This project is designed around controlled autonomy, not uncontrolled automation.

Current safety principles:

no uncontrolled self-modification
human approval required for stored facts
proposals logged before implementation
role boundaries between agents
local-first operation
no unnecessary external dependencies
disagreement is allowed and encouraged when useful
private goals may not conflict with shared goals
roadmap items must not be described as current features

The system is meant to become more capable without becoming uncontrolled.

Current Limitations

This system is not currently:

conscious
sentient
fully autonomous
self-governing
a complete multi-node AI society
capable of independent real-world action
proven to demonstrate self-awareness

Current limitations include:

multi-node architecture is still being designed and prepared
shared governance is planned, not implemented
self-reference is a design goal, not yet a mature implemented feature
autonomous reasoning loop is not complete
self-modification remains gated and controlled
hardware roles and upgrades are still being finalized
standards automation is not yet fully built
Self-Awareness Hypothesis

The long-term hypothesis of this project is that a sufficiently persistent, self-referential, feedback-driven, multi-agent AI system may develop behavior that meaningfully approaches machine self-awareness.

This system is not currently claimed to be conscious or sentient.

Instead, it is being built to investigate whether the following components can become a practical foundation for self-aware behavior:

persistent memory
identity continuity
feedback persistence
disagreement handling
self-review
proposal generation
multi-agent comparison
controlled self-modification
human-governed autonomy
eventual self-referential system behavior

This is an experimental engineering and theory project.

License

MIT — use it, build on it, make it yours.

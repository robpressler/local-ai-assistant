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
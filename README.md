# Local AI Assistant — Modular Autonomous Agent

A locally hosted AI assistant built in Python, designed to run entirely on personal hardware using open-source models via [Ollama](https://ollama.com). Built and developed iteratively by a Network Engineer with a focus on practical utility, honest reasoning, and a long-term goal of controlled autonomous operation.

---

## What This Is

Most AI assistants are stateless cloud services — they forget you the moment the conversation ends and have no persistent understanding of who you are or what you're working on.

This project takes a different approach. The assistant runs locally, learns from every conversation, maintains a structured knowledge base about the user, and is being developed toward a level of autonomous operation where it can reason, propose, and eventually act — within defined boundaries and under human oversight.

This is not a wrapper around an existing product. It is built from the ground up, with deliberate architectural decisions at every layer.

---

## Current Features

**Persistent Memory**
Conversation history is stored locally and loaded on every startup. The assistant never claims to have no memory — it picks up where it left off.

**Structured Knowledge Base**
Facts about the user are extracted from conversations and organized into categories (personal, technical, projects). New facts are staged for approval before being permanently stored — nothing gets written to the knowledge base without explicit confirmation.

**Anti-Sycophancy Design**
The assistant is explicitly instructed to resist agreeing with the user just because they seem to want agreement. It corrects errors directly and holds positions under pressure when it is correct.

**Dynamic Temperature**
Different reasoning tasks require different levels of creativity vs precision. The assistant automatically detects context and adjusts its reasoning temperature accordingly — precise mode for code and facts, creative mode for problem solving, normal for conversation.

**Proposal System**
When the assistant identifies something worth changing — a command, a behavior, a stored fact — it logs the proposal to a review file rather than implementing it. All modifications require explicit user approval.

**Feedback Persistence**
Corrections made by the user are stored permanently and injected into every system prompt. The assistant's behavior improves over time based on real interaction, not retraining.

**File Ingestion**
Large files (configs, logs, documents) can be dropped into an input file and analyzed without the limitations of terminal input. Responses are saved to an output file automatically.

**Docker Containerization**
The assistant runs inside a Docker container with hard resource caps (CPU, memory, process limits). The container communicates with Ollama running on the host machine, keeping the model's GPU utilization separate from the application logic.

---

## Architecture

```
chatbot_docker/
├── main.py              # Core assistant logic
├── chat_history.json    # Persistent history, facts, feedback
├── proposals.txt        # Logged change proposals awaiting review
├── input.txt            # Drop files here for analysis
├── output.txt           # Analysis responses saved here
├── Dockerfile           
└── docker-compose.yml   
```

**Stack:**
- Python 3.11
- Ollama (local LLM inference)
- Llama 3.1 8B (default model, swappable)
- Docker + docker-compose
- No external APIs required to run

---

## Requirements

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) with WSL2 backend
- [Ollama](https://ollama.com) installed on the host machine
- Llama 3.1 8B pulled: `ollama pull llama3.1:8b`
- 6GB+ VRAM recommended for responsive inference

---

## Running It

```bash
# Build and start
docker-compose up --build -d

# Attach to interactive terminal
docker start -ai rob_ai

# Stop
docker-compose down
```

---

## Commands

| Command | Description |
|---|---|
| `/facts` | Show confirmed knowledge base |
| `/pending` | Show facts awaiting approval |
| `/approve [key or #]` | Confirm a pending fact |
| `/reject [key or #]` | Delete a pending fact |
| `/feedback [text]` | Store a persistent correction |
| `/proposals` | View logged change proposals |
| `/file` | Analyze input.txt, save to output.txt |
| `/len [1-3]` | Set response length (1=brief, 3=detailed) |
| `/mode [precise\|normal\|creative]` | Set reasoning temperature |
| `/debug` | Show internal state |
| `/clear` | Wipe all data (requires confirmation) |
| `exit` | Quit |

---

## Development Roadmap

- [x] Persistent conversation memory
- [x] Structured fact extraction with approval gate
- [x] Anti-sycophancy and feedback persistence
- [x] Dynamic temperature by context
- [x] Proposal logging system
- [x] Docker containerization with resource caps
- [ ] Redis shared memory layer
- [ ] Autonomous reasoning loop
- [ ] Journal logging of autonomous decisions
- [ ] Controlled self-modification pipeline
- [ ] Multi-model ensemble routing (panel mode)

---

## Notes

This project is under active development. The codebase reflects real iterative problem-solving — not a polished product, but a working system being built toward a specific long-term goal.

The theoretical framework driving the design decisions behind the autonomous agent architecture is not documented here. That work is separate and ongoing.

---

## License

MIT — use it, build on it, make it yours.

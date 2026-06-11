<div align="center">
  <img src="assets/header.svg" alt="Rowter" width="100%">
</div>

**Rowter is an open-source agent for telecom work** — across standards, commercial frameworks, fraud and security, and the systems that sit on top. It grounds answers in cited sources, then reasons past them when they run thin and labels what it couldn't cite. It remembers what you work on, and turns your own files into a living wiki it keeps current. Each data source it draws on is a plugin — a body of documents plus the tools to search it. The plugins it ships with cover the standards bodies (3GPP, O-RAN, CAMARA, GSMA) and a catalog of open-source telecom software, and you can add your own. It runs on your machine; your data stays private.

→ **Start here: [`studio`](https://github.com/rawrter/studio)** — clone, run one command, start chatting. *No API key needed to boot.*

## How it fits together

<div align="center">
  <img src="assets/architecture.png" alt="evals wraps studio, which contains rowter calling toolkit and plugins" width="100%">
</div>

**rowter** is the agent. **studio** is the app you run it in. **toolkit** gives it retrieval; **plugins** give it data and tools. **evals** runs the whole thing through Inspect-AI checks so its behaviour stays consistent as it changes.

## The repositories

- **[studio](https://github.com/rawrter/studio)** — *start here.* The app you run: chat, knowledge bases, memory, plugins, settings. FastAPI + React, one command to boot.
- **[rowter](https://github.com/rawrter/rowter)** — *the agent.* The runtime: harness, prompts, profiles, the tool schema, and every native tool (`ask_user`, `save_memory`, search, knowledge).
- **[toolkit](https://github.com/rawrter/toolkit)** — *retrieval.* The search layer rowter calls: embeddings, ChromaDB vector store, chunking, ingest and search.
- **[plugins](https://github.com/rawrter/plugins)** — *data and tools.* Each manifest adds a data source and the tools that expose it (3GPP, O-RAN, CAMARA, catalog). Loaded on demand.
- **[evals](https://github.com/rawrter/evals)** — *checks.* The Inspect-AI suite that keeps Rowter's behaviour consistent.

## Open source

Apache-2.0 licensed. Runs on your machine. Built for the telecom community.

# 🌌 AstraAgent

### Advanced Autonomous Multi-Engine PowerShell ReAct Agent

AstraAgent is a standalone, lightweight, yet powerful security auditing engine engineered to bridge the gap between local LLMs (**Ollama**) and zero-cost cloud infrastructure (**OpenRouter Free Tier**). Utilizing a strict **Reason-Act-Observe (ReAct)** loop pattern parsed natively via JSON schemas, AstraAgent reasons through objectives, generates native Windows PowerShell payload instructions, dispatches background evaluation jobs, and ingests live environment telemetry—all within a unified, interactive console terminal.

---

## ⚡ Core Architecture Features

- **Pure ReAct Loop Cycle:** Operates via a rigid JSON state matrix (`thought`, `type`, `content`), decoupling system reasoning from command operational payloads.
- **Hybrid Intelligence Matrix:** Automated real-time endpoint harvesting supporting both offline **Ollama** runtimes and web-connected **OpenRouter API** clusters.
- **Trans-Net Resilience Pipeline:** Built-in HTTP retry matrix that gracefully absorbs transient network interruptions, API 500 faults, and cloud infrastructure **429 Rate Limits** without destabilizing session state.
- **Context Sliding Window Protection:** Automatically trims conversation history queues to prevent context-memory bloat, infinite loop states, and token-boundary exhaustion.
- **Isolated Job Spawner Engine:** Generates and executes target PowerShell payloads asynchronously inside background jobs. Features human-in-the-loop authorization thresholds (`[Y]es / [N]o / [EXIT]`), real-time loop-throttling validation, and immediate console kill-switches.

---

## 🛠️ Operational Prerequisites

- **Host Environment:** Windows PowerShell 5.1 or PowerShell Core 7.0+
- **Local Routing Matrix (Optional):** Active `Ollama` local host configuration environment (e.g., `http://127.0.0.1:11434`) pre-loaded with JSON-capable models (e.g., `llama3`, `mistral`, `qwen`).
- **Cloud Routing Matrix (Optional):** A valid OpenRouter API Key (`sk-or-...`) for automated free-tier harvesting deployment.

---

## 🚀 Deployment Guide

### 1. Initialize Script Locally
Ensure execution policy parameters allow execution inside your standalone laboratory environment, then call the master controller script entry point:

```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
.\AstraAgent.ps1
2. Configure Backend Pipeline Target
Upon boot initiation, select your desired backend ecosystem configuration layout:

Option 1 (Ollama): The script automatically queries the local runtime environment list and provides an Out-GridView display window for quick model profile selection.

Option 2 (OpenRouter): The script dynamically harvests current active free-tier models via OpenRouter endpoint registries, providing an automated list UI for cloud routing deployment.

🔒 Automated Lab Environment Disclaimer
CRITICAL NOTICE: AstraAgent is designed strictly for deployment inside isolated standalone laboratory topologies, sanctioned capture-the-flag (CTF) challenges, and authorized infrastructure security configuration auditing environments. Since the engine evaluates and runs dynamically generated system-level scripts natively through background runspaces, the operator maintains full operational accountability. Always utilize the integrated Human-In-The-Loop confirmation matrix when operating outside restricted sandboxes.

📜 License
Distributed under the MIT License. See LICENSE configuration file parameters for detailed usage authorization metrics.

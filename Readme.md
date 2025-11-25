# 5-Day AI Agents Intensive Course (Kaggle) 📚🤖

A hands-on, practical 5-day course designed to teach developers, data scientists, and AI engineers how to design, build, and deploy AI agents using Google's Agent Development Kit (ADK) and Vertex AI tools. The course contains a sequence of guided notebooks and supporting PDFs that walk learners from basic prompts to advanced agent orchestration, memory, observability, and deployment.

---

## 🚀 What you'll learn

- Build your first agent and learn how it takes actions (Day 1)
- Architect and orchestrate multi-agent systems (Day 1, Day 2)
- Integrate tools and model context protocol (MCP) interoperability (Day 2)
- Manage sessions and long-term memory for agents (Day 3)
- Improve agent quality with observability, evaluation, and testing methods (Day 4)
- Communicate across agents and deploy agents into production (Day 5)

---

## 📁 Repository Structure

This repo provides the course materials organized into five days. Each `DayN/` directory includes two notebooks (and one PDF reference):

- `Day1/`
	- `day-1a-from-prompt-to-action.ipynb` - Getting started: build your first agent, install ADK, use tools like Google Search and run a simple runner. Ideal for beginners.
	- `day-1b-agent-architectures-eb9049.ipynb` - Architectures & workflow patterns: single vs multi-agent, sequential/parallel/loop patterns and manager-agent styles.
	- `Introduction to Agents.pdf` - Supporting slides and explanations.

- `Day2/`
	- `day-2a-agent-tools.ipynb` - Agent tools (FunctionTool, AgentTool, custom tools), MCP, and tool orchestration.
	- `day-2b-agent-tools-best-practices-2af7d1.ipynb` - Best practices for tools, reliability and integration patterns.
	- `Agent Tools & Interoperability with Model Context Protocol (MCP).pdf` - Supporting slides.

- `Day3/`
	- `day-3a-agent-sessions (1).ipynb` - Session management patterns, event-driven architecture, and streaming agent interactions.
	- `day-3b-agent-memory.ipynb` - Memory management, memory services, consolidation, `load_memory` vs `preload_memory`, and automating memory with callbacks.
	- `Context Engineering_ Sessions & Memory.pdf` - Supporting slides.

- `Day4/`
	- `day-4a-agent-observability.ipynb` - Observability, logs, metrics, debugging and the ADK web UI for introspecting agent execution.
	- `day-4b-agent-evaluation.ipynb` - Agent evaluation techniques, testing & metrics.
	- `Agent Quality.pdf` - Supporting slides.

- `Day5/`
	- `day-5a-agent2agent-communication.ipynb` - Agent-to-agent communication patterns and orchestrations.
	- `day-5b-agent-deployment.ipynb` - Prototype-to-production steps, memory bank integration, secure deployments and scaling.
	- `Prototype to Production.pdf` - Supporting slides.

---

## ✅ Quick Start (Local Machine)

1. Install Python 3.10+ and a virtual environment manager (venv or conda recommended).
2. Clone this repository and open it in VS Code or your preferred editor.

```bash
python -m venv venv
source venv/bin/activate  # macOS / Linux
# OR on Windows PowerShell: .\venv\Scripts\Activate
pip install --upgrade pip
pip install jupyterlab
pip install google-adk
```

3. Run Jupyter Lab/Notebook and open the notebooks:

```bash
jupyter lab
# or jupyter notebook
```

Note: The Kaggle environment includes the ADK pre-installed. When using a local environment you may need to install and configure dependencies manually.

---

## 🧭 Running on Kaggle

- The materials were designed for Kaggle notebooks. To run them on Kaggle: open any notebook and click "Copy & Edit" to create your own copy.
- Add your Google API key as a Kaggle secret named `GOOGLE_API_KEY` if you want to call the Gemini API or other Google APIs.
- Avoid using "Run All" in the notebooks — run cells in order to prevent QPM or throttle issues.

Kaggle-specific tips:
- Use `UserSecretsClient` as shown in the notebooks to load `GOOGLE_API_KEY` into the runtime environment.
- When using the ADK web UI in Kaggle, do not share the generated proxy link (it contains sensitive tokens).

---

## 🔧 Configure Gemini API & ADK

1. Get an API key from Google AI Studio: https://aistudio.google.com/app/api-keys
2. Set `GOOGLE_API_KEY` as an environment variable or Kaggle secret.
3. Install ADK and its dependencies:

```bash
pip install google-adk
```

4. If you want to run the ADK Web UI locally, you can run `adk web` (you may need to configure a proxy and the ADK CLI).

---

## 📚 Notable Patterns and Concepts Covered

- Agent types: LlmAgent, SequentialAgent, ParallelAgent, LoopAgent
- Tools: FunctionTool, AgentTool, and built-in tools like `google_search`, `load_memory`, `preload_memory`
- Sessions vs Memory: short-term vs long-term context and consolidation
- Observability: callbacks, logging, tracing, and the ADK web UI
- Deployment & scaling: Vertex AI services, Memory Bank, and deployment best practices

---

## 🛡️ License & Attribution

Many of the notebooks include the Apache License 2.0 header from the original authors (Google / Kaggle course). Use or distribute content per the license terms. If you redistribute materials or create derivative works, please keep the original copyright and license headers.

---

## Contributing 🤝

Contributions are welcome. Suggested workflows:

1. Open issues for bugs or improvements.
2. Submit pull requests with the specific change, include a brief description and testing steps.
3. Please preserve the original license statements in notebooks when editing.

---

## Credits & Contact

Course material includes original content from Google / Kaggle contributors and course authors such as Kristopher Overholt and Sampath M.
If you'd like help customizing these notebooks or deploying sample agents, open an issue or create a PR and describe your request.

---

### 💡 Tips

- When reproducing outdoor or time-sensitive tasks (like Google Search examples), ensure you have a valid `GOOGLE_API_KEY` and use the `google_search` tool responsibly.
- Use `preload_memory` for guaranteed context, `load_memory` to reduce token usage by making retrieval reactive.
- For production, prefer managed memory services such as Vertex AI Memory Bank for consolidation and semantic search.

---

Thanks for exploring the 5-Day AI Agents course. Have fun — and if you'd like, I can also add a TL;DR README summary, a contributing template, or CI checks to help automate validations. ✅

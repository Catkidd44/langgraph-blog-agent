# Agentic Research  Agent 

> *Three AI agents walk into a blog post... one researches, one writes, one edits. The result? Actually pretty good.*

A LangGraph exploration project that uses a **multi-agent pipeline** to turn any topic into a polished blog post — fully automated, from web research to final draft.

---

## How it works

```
START --> Researcher --> Writer --> Editor --> END
```

| Agent | Job |
|-------|-----|
| **Researcher** | Searches the web with DuckDuckGo, extracts key facts and points |
| **Writer** | Turns research into a rough first draft |
| **Editor** | Polishes the draft into a publication-ready blog post |

Just give it a topic and watch three AI agents argue their way to a finished article.

---

## Tech Stack

- [LangGraph](https://github.com/langchain-ai/langgraph) — orchestrates the agent workflow and state machine
- [LangChain](https://github.com/langchain-ai/langchain) — agent tooling and OpenAI integration
- [OpenAI GPT-3.5-turbo](https://openai.com) — the brains behind each agent
- [DuckDuckGo Search](https://pypi.org/project/duckduckgo-search/) — web research without a paid API

---

## Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/Catkidd44/langgraph-blog-agent.git
cd langgraph-blog-agent
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Add your OpenAI key
Create a `.env` file in the project root (this file is gitignored — your key stays local):
```
OPENAI_API_KEY=your-key-here
```

### 4. Run the notebook
Open `LangChain Agent Mama.ipynb` in Jupyter and run all cells. Change the topic to whatever you want!

---

## Example

```python
result = app.invoke({"initial_topic": "Who will win this year's World Cup and why?"})
print(result["final_draft"])
```

The agents will research, draft, and edit a complete blog post on the topic.

---

## Notes

- `.env` is listed in `.gitignore` — your API key will never be committed
- Model temperature is set to `0.7` for a balance of creativity and consistency
- The graph can be visualized as a Mermaid diagram directly in the notebook

---

*Built as a hands-on exploration of LangGraph's multi-agent orchestration capabilities.*

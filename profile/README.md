## Novyx Labs

**Persistent memory for AI agents.** Store, recall, rollback, audit — so your agents never forget, and when they're wrong, you can undo it.

### Core

| Package | Install | Description |
|---------|---------|-------------|
| [**novyx**](https://pypi.org/project/novyx/) | `pip install novyx` | Python SDK — 78 methods, async support |
| [**novyx** (npm)](https://www.npmjs.com/package/novyx) | `npm install novyx` | JS/TS SDK |
| [**novyx-mcp**](https://pypi.org/project/novyx-mcp/) | `pip install novyx-mcp` | MCP server — 23 tools, local-first SQLite mode |
| [**novyx-langchain**](https://pypi.org/project/novyx-langchain/) | `pip install novyx-langchain` | LangChain integration |
| [**novyx-crewai**](https://pypi.org/project/novyx-crewai/) | `pip install novyx-crewai` | CrewAI integration |
| [**novyx-llamaindex**](https://pypi.org/project/novyx-llamaindex/) | `pip install novyx-llamaindex` | LlamaIndex integration |

### What makes Novyx different

- **Rollback** — undo any memory to any previous version
- **Audit trails** — SHA-256 hash-chained, tamper-proof, exportable
- **Replay** — counterfactual analysis and drift detection
- **Knowledge graph** — entity relationships stored as triples
- **Sentinel** — circuit breaker with RSA-4096 trace signing
- **Context spaces** — shared memory namespaces for multi-agent teams

### Get started

```python
from novyx import Novyx

nx = Novyx(api_key="your-key")
nx.remember("User prefers dark mode", tags=["prefs"])
result = nx.recall("user preferences")  # score: 0.94
nx.rollback(result.memories[0].uuid, to_version=1)
```

### Links

[Website](https://novyxlabs.com) · [API Docs](https://novyx-ram-api.fly.dev/docs) · [Try the demo](https://try.novyxlabs.com) · [Rollback demo](https://demo.novyxlabs.com)

Free tier available — no credit card required.

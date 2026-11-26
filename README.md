# NekoJob MCP Server

**Search live jobs in the UAE and the Gulf from Claude, ChatGPT and any MCP-compatible AI assistant.**

[NekoJob](https://nekojob.com/) is a job platform connecting job seekers from Africa and Asia with employers in the United Arab Emirates, Oman, Qatar and Saudi Arabia. This remote [Model Context Protocol](https://modelcontextprotocol.io/) server lets an AI assistant search NekoJob's open vacancies and return real jobs with links.

Ask your assistant things like:

- "Find cleaner jobs in Dubai"
- "Are there driver jobs in Abu Dhabi?"
- "Show me hotel jobs in Qatar"
- "How do I spot a fake job offer from Dubai?"

## Endpoint

| | |
|---|---|
| **URL** | `https://nekojob.com/wp-json/nkmcp/v1/mcp` |
| **Transport** | Streamable HTTP |
| **Authentication** | None (public, read-only) |

## Tools

| Tool | What it does |
|---|---|
| `search_jobs` | Search open jobs by keyword, location and category |
| `get_job` | Get the full details of one job, with its link on nekojob.com |
| `list_locations_and_categories` | List the countries, cities and job categories you can search |
| `job_safety_tips` | Practical tips to avoid job scams and fake offers |

## Connect it

### Claude (claude.ai / Claude Desktop)
Settings → Connectors → **Add custom connector** → paste the URL above.

### ChatGPT
Settings → Apps & Connectors → **Create** (developer mode) → paste the URL above.

### Any MCP client (JSON config)

```json
{
  "mcpServers": {
    "nekojob": {
      "type": "http",
      "url": "https://nekojob.com/wp-json/nkmcp/v1/mcp"
    }
  }
}
```

## Privacy and safety

- Read-only: the server only returns **open** job listings.
- No employer phone numbers, emails or WhatsApp numbers are shared, and no candidate data is ever exposed.
- NekoJob never asks job seekers to pay an employer or agent. Creating a profile is free; applying to jobs needs NekoJob Premium (from USD 7).

## Links

- Website: https://nekojob.com/
- Browse jobs: https://nekojob.com/job-list/
- Free AI CV builder: https://nekojob.com/cv-builder/
- Free UAE Gratuity Calculator: https://nekojob.com/tools/uae-gratuity-calculator/
- How to stay safe from job scams: https://nekojob.com/stay-safe/

Maintained by [NekoJob](https://nekojob.com/) (Neko Job Limited).

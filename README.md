# AI MCV

A quick navigation handbook for my AI tools and services configuration, just like a Mobile Construction Vehicle.

---

## Daily Chat

| Name | Model | Scene | Link |
|------|------|------|------|
| **Qianwen** (千问) | Qwen3-Max | Daily | <a href="https://www.qianwen.com/" target="_blank">qianwen.com</a> |
| **Google Gemini** | Gemini 3 | Creative | <a href="https://gemini.google.com/" target="_blank">gemini.google.com</a> |
| **ChatGPT** | GPT-5.2 | Technology | Ask on GitHub Copilot |


## Image Generation

| Name | Link |
|------|------|
| **Jimeng** (即梦) | <a href="https://jimeng.jianying.com/ai-tool/generate" target="_blank">jimeng.jianying.com</a> |

## Coding Assistant

### GitHub Copilot (VS Code)

- Link <a href="https://code.visualstudio.com/" target="_blank">code.visualstudio.com</a>

- Enabled Models

| Model | Mode | Scene | Cost |
|------|-------|--------|--------|
| **GPT-5 mini** | Inline Edit | - | 0x |
| **Claude Sonnet 4.5** | Ask, Agent | Most commonly used | 1x |
| **Claude Opus 4.5** | Agent | Difficult problem; 0 -> 1 with spec-kit | 3x |
| **GPT-5.2** | Ask | Inspirations; Cross-validation | 1x |
| **GPT-5.1-Codex-Max** | Agent | Buggy problems | 1x |

- Prompts - see [.github/prompts](.github/prompts)
  - my-common-prompts


### Claude Code (GLM-4.7)

```sh
npm install -g @anthropic-ai/claude-code
npx @z_ai/coding-helper
```

- Get API Key on <a href="https://bigmodel.cn/usercenter/proj-mgmt/apikeys" target="_blank">bigmodel.cn/usercenter/proj-mgmt/apikeys</a> .

- Commands - see [.claude/commands](.claude/commands) .

  - add-commit-push

  - my-common-prompts

- Skills - Official Skills

  ```
  /plugin marketplace add anthropics/skills
  ```

  - `doc-coauthoring`
  - `frontend-design`
  - `skill-creator`

### GitHub Copilot Remote Agent

- Link <a href="https://github.com/copilot" target="_blank">github.com/copilot</a>

- Environment setup can be annoying


## Spec-Driven Development

### spec-kit

```sh
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git
specify init --here --ai copilot
specify init --here --ai claude
```

- A must for 0->1, but think twice for spec 002 because Plan Mode might do better
- Common workflow

```
Constitution → Specify → Plan → Tasks → Implement
```

## MCP Server

### Context7

- Claude Code

```sh
claude mcp add --transport http context7 https://mcp.context7.com/mcp --header "CONTEXT7_API_KEY: YOUR_API_KEY"
```

- VS Code

See [.github/mcp.json](.github/mcp.json) .

### Playwright MCP

- Claude Code

```sh
claude mcp add playwright npx @playwright/mcp@latest
```

- VS Code

```sh
code --add-mcp '{"name":"playwright","command":"npx","args":["@playwright/mcp@latest"]}'
```

### GitHub MCP Server

- Claude Code

```sh
claude mcp add-json github '{"type":"http","url":"https://api.githubcopilot.com/mcp/","headers":{"Authorization":"Bearer YOUR_GITHUB_PAT"}}'
```

- VS Code

One-click install (OAuth): [![Install in VS Code](https://img.shields.io/badge/VS_Code-Install_Server-0098FF?style=flat-square&logo=visualstudiocode&logoColor=white)](https://insiders.vscode.dev/redirect/mcp/install?name=github&config=%7B%22type%22%3A%20%22http%22%2C%22url%22%3A%20%22https%3A%2F%2Fapi.githubcopilot.com%2Fmcp%2F%22%7D)

Or see [.github/mcp.json](.github/mcp.json) for manual configuration.

## LLM Gateway

### ZetaTechs

- Link <a href="https://api.zetatechs.com/" target="_blank">api.zetatechs.com</a>
- OpenAI Chat Completions, OpenAI Responses, Anthropic Messages, Gemini Generate Content
- OpenAI Embeddings

### ocoolAI

- Link <a href="https://one.ooo.cool/" target="_blank">one.ooo.cool</a>
- OpenAI Chat Completions mainly

---

*Last updated: 2026-01-12*


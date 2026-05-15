# Real User Stories: LLM Usage at Different Levels

Raw material collected via web search, May 2026. Personal stories of individual people and their tool stacks — not corporate case studies.

---

## Level 1: Web Chat — opened a tab and typed

### Amara Redfield — morning brief with Claude Projects
- Tool: Claude (Projects feature), ChatGPT
- Routine: opens a dedicated Claude Project every morning, pastes calendar + yesterday's notes, runs 3 prompts: day brief, priority challenge, first meeting prep
- Takes 8 minutes, replaced a 25-minute routine
- Uses Projects because custom instructions stay loaded permanently — no re-explaining context
- Source: medium.com/@amara-in-the-wild

### Ritik — switched from ChatGPT to Claude for UI design
- Tools: ChatGPT, Claude (Artifacts feature)
- Before: ChatGPT for brainstorming designs, but had to describe concepts and use separate tool for visuals
- After: Claude Artifacts — interactive prototypes directly in chat, "closer to vibe-coding"
- Larger context window (200K tokens) means long conversations don't lose context
- Source: xda-developers.com

### Andrew Beck — launched 3 startups with just chat + Zapier
- Tools: ChatGPT, Claude, Gemini, Chatronix (multi-model), Zapier, Notion, Carrd, Teachable
- Non-technical founder, no dev team, no VC money — built 3 businesses in 6 months
- SEO Agency: Claude wrote service agreements, ChatGPT handled client comms. First client from Reddit thread, $4,250 revenue in 1 week
- Resume AI: Gemini tailored resumes from live job listings, $1,516 in 2 days
- AI Microcourses: ChatGPT as the course tutor, $2,660 in 1 week
- Key: "I wasn't context switching. I was scaling."
- Source: metapress.com

---

## Level 2: Chat + files + research

### Preeti Bahuguna — 7-day experiment: ChatGPT vs Claude
- Tools: ChatGPT, Claude
- Developer. Replaced her daily ChatGPT workflow with Claude for a week
- Claude won on: large files (pasted entire service module — Claude handled without chunking), documentation generation (readable, real-tone README)
- ChatGPT won on: quick tactical requests (regex, data structure conversion, SQL queries)
- Ended up using both — "different modes of thinking, too useful to ignore"
- Source: medium.com/@bahuguna.preeti

### James Rowe — two subscriptions for different tasks
- Tools: Claude Pro ($20/mo) + ChatGPT Plus ($20/mo)
- Uses Claude for: coding (side-by-side Artifacts pane), less verbose responses
- Uses ChatGPT for: quicker, more decisive style when speed matters
- Tasks: brainstorming ideas ("third voice on the shoulder"), book review feedback, meeting agenda planning, maintaining AWS/Jekyll website, writing import scripts
- "Not a replacement of existing workflows, a wholly new approach to problem-solving"
- Source: jsrowe.com

---

## Level 3: Coding Agent — model writes, reviews, commits

### Christopher Penkin — plan mode changed everything
- Tools: Claude Desktop App (quick questions), Claude Code (project work)
- Claude Code workflow: `/init` builds CLAUDE.md from codebase → plan mode before every feature → agent executes → review diffs manually
- Real example: "Add postal code fields to employee addresses" — team estimated 4 hours, Claude did it in 5 minutes. Checked API, found it already supported the fields, only needed UI change
- Tips: keep tasks small and focused, clear context after each feature, Claude will ask clarifying questions in plan mode
- Source: penkin.me

### Mikul Gohil — Claude Code as core development tool for 1 year
- Tools: Claude Code, Claude Desktop, VS Code
- Morning: "What changed overnight?" — Claude reviews teammate PRs, checks diff against CLAUDE.md conventions, spots issues
- Feature work: Plan → implement in stages (data model → API route → UI component) → Claude reviews its own work as "different developer"
- Hooks: Prettier auto-formats on every file edit, safety hook blocks `git push --force` and `git reset --hard`
- "Not all LLM use cases benefit from AI. Used correctly, Claude has made me a better developer."
- Source: mikul.me

### Maciej Adamczyk — from Copilot to PRDs and worktrees
- Tools: GitHub Copilot, Claude Sonnet, VS Code
- Started with Copilot autocomplete, then found Claude Sonnet on reasoning + Artifacts
- Workflow: write PRD → system spec → CLAUDE.md → Plan mode → Agent mode
- Uses git worktrees: two features in parallel, two AI conversations, zero `git stash` gymnastics
- Permissions: "difference between giving a new colleague the office key and giving them the building's master key"
- Source: medium.com/@adamczyk.maciej01

---

## Level 4: Full self-hosted local stack

### Mo Abualruz — local stack wired into engineering pipeline
- Tools: Ollama (daily driver), llama.cpp (CPU fallback), vLLM (batch inference), Open WebUI (chat), Fulcrum (custom agent control plane)
- Homelab GPU, local LLM used alongside Postgres and Redis
- Automated code review before every PR: model reads diff, flags issues by severity — "catches obvious things before human review"
- Synthetic test data generation: local model generates user records, product catalogues, log lines cheaply with seed determinism
- Unfamiliar codebase exploration: "What does this file do?" → model gives a sketch → reads and corrects manually
- README/runbook first drafts: model beats blank-page problem in seconds, human edits for final quality
- Link synthesis: feeds bookmark list → model identifies which 3 links are worth reading in full
- Key insight: "Build the routing layer. Local for high-volume/cost-sensitive, cloud API for depth. That's where the 10× cost savings come from."
- Source: abualruz.com

### Local AI Master — 90-day local-only challenge
- Tools: Ollama + Open WebUI + Continue.dev (VS Code) + ComfyUI/Flux + Whisper (large-v3)
- Hardware: RTX 3090 24GB VRAM
- Started with: llama3.2:7b, codellama:13b, deepseek-coder-v2:16b
- Day 35: Whisper transcribed 90-minute client meeting in 12 minutes → model generated summary with action items. "20 minute post-meeting workflow instead of an hour."
- Day 42: RAG pipeline with local vector DB indexing entire project — Continue.dev fetches relevant snippets and includes in context window
- Day 68: Pulled Qwen 2.5 32B Q4_K_M (19GB, fits in 24GB VRAM, ~18 tok/s). "The jump from 7B to 32B was significant. Multi-step problems handled cleanly."
- Day 75: Flux prompting matured with ComfyUI presets — blog headers, social posts, product mockups, 30 sec per image
- Summary: replaced 3 paid tools → $0/month. "Doesn't need to outperform cloud models to be useful — just needs to be reliable, private, and always available."
- Source: localaimaster.com

### Derek Armstrong — family homelab, Ollama → vLLM migration
- Tools: Ollama → vLLM, Open WebUI, Cursor (connected to local endpoint)
- Multi-user household: wife doing research, son homework, himself running coding agent
- Problem: Ollama hit concurrency bottleneck on Qwen models (requests queued instead of parallel)
- Solution: vLLM with PagedAttention — "true parallel processing for enterprise-grade homelab workload"
- "vLLM is heavy. Docker container orchestration, manual parameter tuning... but the performance gains make the setup cost worth it."
- Key insight: "Pick one model, tune it, commit to it. Constantly switching models gives inconsistent results."
- "I own the stack, the model, and the prompts. No vendor pricing changes, no features removed."
- Source: derekarmstrong.dev

### Blake Oxford — Mac Mini M1 as production-grade microservice stack
- Tools: Ollama + Open WebUI (Docker) + Cloudflare Tunnel + LaunchDaemons
- Mac Mini M1, running 24/7
- Architecture: Ollama as non-admin LaunchDaemon (sandboxed), Docker container bound only to localhost, Cloudflare Tunnel for remote
- Self-healing: watchdog script checks container health, auto-restarts failures
- "The output quality is not always on par with ChatGPT, especially on M1. But everyday tasks like drafting text, summarizing files, querying data, or brainstorming code run beautifully offline."
- "Local models trade depth for independence — they think a little slower and dream a little smaller."
- Source: blakeoxford.com

---

## Level 5: Developer toolchain — open-source replacement stack

### Local AI Developer Toolchain — Continue.dev + Ollama + Aider
- Tools: Continue.dev (VS Code) + Ollama + Aider
- Coder trio in 24GB VRAM: Qwen2.5 Coder 1.5B (autocomplete) + 14B (chat) + DeepSeek R1 8B (code review)
- Full Continue.dev config: RAG indexing via nomic-embed-text, context providers for code/diff/terminal/file/codebase
- Aider: repo-wide refactors — "rename the User model to Customer across all files and update the migrations"
- "80% of what Cursor and Claude Code do for day-to-day development — the local stack matches them."
- Cost: $0 after hardware. Team deployment: share one Ollama server with OLLAMA_NUM_PARALLEL=8
- Source: localaimaster.com

### Jamie Tanna — tax return on a local model
- Tools: Ollama + OpenWebUI, AMD Radeon 7900 XTX (24GB VRAM) + MacBook Pro M4 Pro (48GB RAM)
- Models: gpt-oss:20b (daily driver), qwen3:30b (alternate)
- OpenWebUI feature: "ask multiple models" to compare answers
- Use cases: code (where quality isn't critical and ~60 sec wait is OK), tax return (data absolutely can't leave machine)
- "If it's something that I need to be the most accurate, or the most perfect code, I use it in cases where data shouldn't be sent to a hosted model — even with enterprise agreement."
- Source: jvt.me

### Yash Patel — rebuilt entire productivity workflow locally
- Tools: Ollama + Docker + Open WebUI + Logseq + Obsidian + Paperless-ngx + VS Code + AgenticSeek + Home Assistant
- Hardware: 32GB RAM, RTX 5070, 1TB SSD
- Logseq integration: expand bullet points into outlines, summarize notes, refine drafts
- Obsidian for long-form writing: refine paragraphs, simplify explanations without cloud
- Paperless-ngx: summarize long PDFs, ask questions over stored documents — nothing uploaded externally
- "With a local LLM, hesitation disappears. I can connect it with every tool without thinking about data exposure. I ended up using AI more consistently."
- "It doesn't need to outperform cloud models. It just needs to be reliable, private, and always available."
- Source: xda-developers.com

---

## Level 6: DIY Agent Architecture

### Martin Garramon — 13 Claude Code Skills replacing entire workflow
- Tools: Claude Code, custom skills (SKILL.md files with routing logic)
- Built 13 custom skills from scratch — started with a 200-line Upwork proposal template
- Routing table at the core: "proposal" → load references X, Y, Z; "article" → different references and voice
- Sales engine skill: 300+ lines with 6 reference files loaded on demand
- Personality rules embedded in skills: "Martin tends to over-prepare. Skill's job = push him to act."
- Research skill: 2 hours to build, saves 10+ hours/week — dispatches parallel search agents, runs quality control on sources, synthesizes findings, logs what it learned
- "The gap between a fresh Claude session and one loaded with 13 skills is enormous — like hiring someone smart vs someone smart who already knows your business."
- Source: medium.com/@martin_50671

### DEV User "wchatt" — Claude Code as personal executive assistant
- Tools: Claude Code + Slack + Custom node.js listener ("Cranium"), MEMORY.md, CLAUDE.md, MCP
- Runs two businesses solo: land acquisition company + e-commerce brand
- Architecture: Slack listener dispatches messages to Claude Code → reads CLAUDE.md + MEMORY.md on every invocation
- Capabilities: manages Notion task board, handles Shopify product updates, monitors Google Ads, takes voice calls, runs nightly health checks
- "It's like having a coworker who lives in your Slack workspace and is extremely smart."
- "No orchestrator, no vector database, no RAG pipeline, no fine-tuning. Just Claude, some markdown files, and a listener."
- Source: dev.to/wchatt

### James Kilby — full self-hosted AI platform
- Tools: Ollama + Open WebUI + Qdrant (vector DB) + Apache Tika (document parsing) + SearxNG (web search) + ComfyUI (image gen) + Whisper (STT) + SmarterRouter + n8n + Traefik + Cloudflare Tunnels
- Hardware: NVIDIA A10 24GB, Docker Compose orchestrated via Portainer
- SmarterRouter: profiles all available models at startup, routes each request to the best model based on prompt analysis + HuggingFace/LMSYS benchmarks
- n8n: native Ollama integration — "where AI capabilities get wired into actual processes"
- "I haven't fully moved away from commercial hosted AI tools, but I have significantly reduced their usage."
- Source: jameskilby.co.uk

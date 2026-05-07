# Экосистемы инструментов вокруг кодинг-агентов (Май 2026)

## Исследование для статьи: плагины, скиллы, тулзы, управление контекстом, память

---

## 1. PLUGIN / SKILL / TOOL MARKETPLACES

### 1.1. Claude Code (Anthropic)

- **Репозиторий**: `anthropics/claude-code` (121k звёзд, 20k форков)
- **Языки**: TypeScript, Python, Shell
- **Лицензия**: проприетарная (с открытым кодом в репозитории)
- **Плагин-система**:
  - Формат: `.claude-plugin/plugin.json` — манифест плагина
  - Компоненты: `skills/`, `commands/`, `agents/`, `hooks/`, `.mcp.json`, `monitors/`, `settings.json`
  - Плагины распространяются через маркетплейсы (официальный Anthropic marketplace + можно создавать свои)
  - Установка через `/plugin install`, разработка через `--plugin-dir`
- **MCP-серверы**: встроенная поддержка Model Context Protocol (MCP). MCP-серверы подключаются через `.mcp.json` или глобальный конфиг. Доступны reference-серверы (Filesystem, Git, Memory, Fetch, Sequential Thinking, Time), плюс сообщество создало тысячи серверов на Smithery, PulseMCP, mcp-get, mcpm.sh и др.
- **Скиллы**: AgentSkills стандарт — `SKILL.md` с YAML frontmatter + инструкциями; модель сама решает, когда активировать скилл.
- **Хуки**: 9 событий (PreToolUse, PostToolUse, SessionStart, Stop и др.), поддержка командных хуков и промптовых хуков.
- **Официальные плагины**: 13 штук (code-review, feature-dev, plugin-dev, hookify, frontend-design, pr-review-toolkit, security-guidance, ralph-wiggum и др.)
- **Маркетплейс**: официальный marketplace на claude.ai/settings/plugins, плюс можно создавать приватные маркетплейсы для команд

### 1.2. OpenClaw (openclaw/openclaw)

- **Репозиторий**: `openclaw/openclaw` (369k звёзд, 76k форков)
- **Языки**: TypeScript (основной), Python, Shell
- **Лицензия**: MIT
- **Плагин-система**:
  - Нативные плагины: `.openclaw.plugin.json` формат
  - Bundle-плагины: совместимость с Codex/Claude/Cursor форматами
  - Gateway-плагины для расширения функциональности
- **ClawHub** (`clawhub.ai`):
  - **5400+ скиллов** (на май 2026)
  - **52.7k инструментов**, 180k пользователей, 12M загрузок
  - Категории: self-improving agent, GitHub integration, security, soul, dashboard builder и сотни других
  - Скиллы: `Skills` — AgentSkills стандарт
  - Плагины: Gateway plugins
  - Публикация: любой пользователь GitHub может опубликовать скилл/плагин
- **MCP-серверы**: нативная поддержка
- **Скиллы**: workspace skills (`~/.openclaw/workspace/skills/`), инжектируемые промпт-файлы (`AGENTS.md`, `SOUL.md`, `TOOLS.md`)
- **Сандбоксинг**: Docker, SSH, OpenShell — изолированное выполнение
- **Каналы**: 20+ (WhatsApp, Telegram, Slack, Discord, Signal, iMessage и др.)

### 1.3. Pi (badlogic/pi-mono)

- **Репозиторий**: `badlogic/pi-mono` (45.8k звёзд, 5.4k форков)
- **Языки**: TypeScript 97%
- **Лицензия**: MIT
- **Архитектура**:
  - Монорепозиторий: `@mariozechner/pi-ai` (LLM API), `@mariozechner/pi-agent-core` (runtime), `@mariozechner/pi-coding-agent` (CLI), `@mariozechner/pi-tui` (TUI), `@mariozechner/pi-web-ui`
- **Плагин-система**:
  - Расширения через `.pi/` конфигурацию
  - Pi Packages: npm-распространение (`@mariozechner/pi-*`)
  - Skills: Собственная система через `.pi/skills/`; совместимость со стандартом AgentSkills (SKILL.md)
- **Интеграции**: Slack-бот через `earendil-works/pi-chat`
- **Уникальность**: Полностью открытый код, локальное выполнение, можно использовать с локальными моделями через vLLM pod
- **Доступ из РФ**: Не требует VPN для самого инструмента; ключи API — через OpenRouter/Proxy

### 1.4. Cline (cline/cline)

- **Репозиторий**: `cline/cline` (61.5k звёзд, 6.4k форков)
- **Языки**: TypeScript 98%
- **Лицензия**: Apache 2.0
- **Расширение VSCode**: marketplace.visualstudio.com
- **Плагин-система**:
  - **MCP-серверы**: встроенная поддержка Model Context Protocol
  - Уникальная фича: Cline может **создавать MCP-серверы из чата**. Достаточно сказать "add a tool that..." и агент сам создаст и установит новый MCP-сервер
  - Поддержка community MCP servers (через стандартные конфиги MCP)
  - Скиллы: `.agents/skills/` — поддержка формата AgentSkills
  - `.clinerules` — правила поведения агента
  - `.codex/environments` — окружения для Codex
- **Модели**: OpenRouter, Anthropic, OpenAI, Google Gemini, AWS Bedrock, Azure, GCP Vertex, Cerebras, Groq, LM Studio/Ollama (локальные)
- **Enterprise**: SSO (SAML/OIDC), аудит, приватные сети, self-hosted
- **Доступ из РФ**: VSCode маркетплейс может требовать VPN; OpenRouter как прокси для API

### 1.5. OpenCode → Crush (`opencode-ai/opencode` → `charmbracelet/crush`)

- **Статус**: ЗААРХИВИРОВАН (сентябрь 2025). Проект переехал в `charmbracelet/crush`
- **Репозиторий (архивный)**: `opencode-ai/opencode` (12.4k звёзд)
- **Языки**: Go 99%
- **Лицензия**: MIT
- **Плагин-система**:
  - MCP-серверы: встроенная поддержка (типы: stdio, SSE)
  - Custom Commands: Markdown-файлы в `~/.config/opencode/commands/` или `.opencode/commands/`
  - LSP-интеграция для любого языка
  - Shell-конфигурируемый
- **Crush** (преемник): разрабатывается командой Charm (charmbracelet), детали обновлённой плагин-системы уточняются

### 1.6. Aider (`Aider-AI/aider`)

- **Репозиторий**: `Aider-AI/aider` (44.5k звёзд, 4.4k форков)
- **Языки**: Python 80%
- **Лицензия**: Apache 2.0
- **Плагин-система**:
  - **Нет встроенного маркетплейса плагинов**
  - Конфигурация через `.aider.conf.yml`, `.env`, аргументы командной строки
  - Поддержка MCP в разработке (ограниченная)
  - Интеграция с линтерами и тестами — встроена
  - Карта кода (repo map) для контекста больших проектов
  - Voice-to-code, images/URLs
- **Ключевая особенность**: Git-интегрированный рабочий процесс; автоматические коммиты
- **Доступ из РФ**: pip install; API через OpenRouter

### 1.7. Другие агенты

| Агент | Расширения | MCP | Скиллы |
|-------|-----------|-----|--------|
| **Cursor** | `.cursor/rules`, `.cursor-plugin`, MCP servers | Да | AgentSkills |
| **Windsurf** | `.windsurfrules`, MCP servers | Да | Ограничено |
| **Cody** (Sourcegraph) | Sourcegraph API, custom commands | Да | Ограничено |
| **Codex** (OpenAI) | `.codex/environments`, skills, плагины | Да | AgentSkills |
| **Copilot** (GitHub) | MCP servers, custom instructions | Да | Ограничено |

**Общая тенденция**: MCP стал универсальным стандартом подключения инструментов. AgentSkills (SKILL.md) — стандарт для скиллов. Конвергенция форматов: OpenClaw поддерживает bundle-плагины Codex/Claude/Cursor.

---

## 2. CONTEXT MANAGEMENT / MEMORY TOOLS

### 2.1. Mem0 (`mem0ai/mem0`)

- **Репозиторий**: 55k звёзд, 6.2k форков
- **Языки**: Python 56%, TypeScript 35%
- **Лицензия**: Apache 2.0
- **Тип**: Open-source + Cloud (Mem0 Platform)
- **Описание**: Универсальный memory layer для AI-агентов. Извлекает и хранит пользовательские предпочтения, факты, контекст.
- **Алгоритм памяти (v3, апрель 2026)**:
  - Single-pass ADD-only экстракция (один вызов LLM, без UPDATE/DELETE)
  - Entity linking — сущности извлекаются, embedding'ятся и связываются между собой
  - Multi-signal retrieval: семантический + BM25 keyword + entity matching
  - Бенчмарки: 91.6 на LoCoMo, 93.4 на LongMemEval, 64.1 на BEAM (1M токенов)
- **Развёртывание**:
  - **Локально**: `pip install mem0ai` (библиотека), `docker compose up` (self-hosted сервер с векторной БД)
  - **Облако**: `app.mem0.ai` (managed service)
- **Интеграции**: Claude Code, OpenClaw, Codex, Cursor, Windsurf, OpenCode (AgentSkills)
- **SDK**: Python (`mem0ai`), TypeScript (`mem0ai` npm), CLI (`mem0-cli`)
- **MCP-сервер**: есть, можно подключить как внешнюю память к агенту
- **Россия**: локальное развёртывание доступно без ограничений; облачная версия — оплата картами (не российскими), нужен VPN для API

### 2.2. Letta (бывш. MemGPT) (`letta-ai/letta`)

- **Репозиторий**: 22.5k звёзд, 2.4k форков
- **Языки**: Python 99.5%
- **Лицензия**: Apache 2.0
- **Тип**: Open-source + Cloud (Letta API)
- **Описание**: Платформа для создания stateful-агентов с расширенной памятью. Агенты с самообучающейся памятью, которая улучшается со временем.
- **Letta Code**: CLI-инструмент для локального запуска (`npm install -g @letta-ai/letta-code`)
- **Letta API**: Хостинг-платформа с Python и TypeScript SDK
- **Ключевые концепции**:
  - Memory blocks: human, persona (как системные промпты)
  - Self-editing memory — агент сам обновляет свою память
  - Архивная память + recall (восстановление контекста из долгосрочной памяти)
- **Развёртывание**: docker compose, Kubernetes, облачный API
- **Скиллы**: поддержка AgentSkills, встроенные скиллы для памяти и continual learning
- **Россия**: локально — без ограничений; облако — VPN + иностранная оплата

### 2.3. LangMem (`langchain-ai/langmem`)

- **Репозиторий**: 1.4k звёзд, 163 форка
- **Языки**: Python 99%
- **Лицензия**: MIT
- **Тип**: Open-source (часть экосистемы LangChain)
- **Описание**: Memory SDK для LangGraph-агентов. Интегрируется с LangGraph Storage.
- **Возможности**:
  - Core memory API (работает с любым хранилищем)
  - Memory management tools — агент сам управляет памятью в "горячем пути"
  - Background memory manager — автоматическая экстракция и консолидация знаний
  - Нативная интеграция с LangGraph Long-term Memory Store
- **Развёртывание**: `pip install langmem`; хранилище: InMemory (для dev) или AsyncPostgresStore (для prod)
- **Россия**: полностью локальное, без ограничений

### 2.4. Zep (`getzep/zep`)

- **Репозиторий**: 4.5k звёзд, 618 форков
- **Языки**: Python 70%, Go 26%
- **Лицензия**: Apache 2.0
- **Тип**: Проприетарное облако + открытые примеры (Community Edition deprecated)
- **Описание**: End-to-end контекст-инжиниринговая платформа. Graph RAG с темпоральным knowledge graph (через Graphiti).
- **Graphiti** (`getzep/graphiti`): открытый temporal knowledge graph framework — строит графы знаний с фактами и временными метками (`valid_at`, `invalid_at`)
- **Ключевые фичи**:
  - Саб-200ms latency
  - Relationship-aware retrieval
  - Контекст собирается из чат-истории, бизнес-данных, документов, событий
  - SOC2 Type 2 / HIPAA
- **SDK**: Python (`zep-cloud`), TypeScript (`@getzep/zep-cloud`), Go
- **MCP-сервер**: `mcp/zep-mcp-server`
- **Россия**: облачное решение — потребуется VPN; локальный деплой Community Edition более недоступен

### 2.5. Векторные базы данных как memory backend

| БД | Звёзд | Язык | Лицензия | Локально | Облако | Особенности |
|----|-------|------|----------|----------|--------|-------------|
| **ChromaDB** | 27.8k | Rust 68%, Python 16% | Apache 2.0 | Да (embedded) | Chroma Cloud | Встроенная в Mem0 по умолчанию; API из 4 функций |
| **Qdrant** | 31.1k | Rust 87% | Apache 2.0 | Да (Docker) | Qdrant Cloud (бесплатный tier) | Квантование векторов (экономия RAM до 97%), фильтрация по payload |
| **Weaviate** | 16.1k | Go 97% | BSD-3 | Да (Docker) | Weaviate Cloud | Гибридный поиск, RAG, реранкинг, мультиарендность |
| **Milvus** | 44.2k | Go + C++ | Apache 2.0 | Да (Docker/K8s) | Zilliz Cloud (бесплатный tier) | GPU acceleration, fully distributed, 10B+ векторов |
| **Pinecone** | — | — | Проприетарная | Нет (cloud-only) | Pinecone Cloud | Serverless, SOC2/HIPAA; только API |

**Примечание по РФ**: Все open-source векторные БД разворачиваются локально без ограничений. Pinecone — только облако, нужен VPN.

### 2.6. Прочие memory-решения

| Решение | Тип | Статус | Примечание |
|---------|-----|--------|------------|
| **Memobase** | User memory | Умеренный интерес | `memobaseio/memobase` — 404 на GitHub (возможно, проект переименован или закрыт) |
| **LLM-встроенная память** | API | Актуально | Многие облачные LLM (Claude, GPT-5) предлагают встроенную память в рамках сессии, но не кросс-сессионную |

---

## 3. LOCAL VS API-BASED SOLUTIONS

### 3.1. Полностью локальные (без внешних API)

| Инструмент | Локальный код | Векторная БД | LLM | Модели |
|-----------|-------------|-------------|-----|--------|
| **Pi-agent** | Да | — | Через OpenRouter/Local | Ollama, vLLM |
| **Cline** | Да (VSCode) | — | Через API/Local | Ollama, LM Studio |
| **Aider** | Да | — | Через API | Ollama (ограничено) |
| **OpenClaw** | Да (Gateway) | — | Через API | OpenAI-совместимые |
| **Claude Code** | Частично (код открыт) | — | Только Claude API | — |

### 3.2. Memory-решения: локальные vs облачные

| Решение | Локально | Self-hosted | Cloud |
|---------|----------|-------------|-------|
| **Mem0** | `pip install mem0ai` (библиотека) | `docker compose up` (сервер) | app.mem0.ai |
| **Letta** | Letta Code (CLI) | `docker compose up` (API сервер) | app.letta.com |
| **LangMem** | `pip install langmem` | LangGraph Platform | LangSmith Cloud |
| **Zep** | ❌ (deprecated) | ❌ | Только Zep Cloud |
| **ChromaDB** | `pip install chromadb` (embedded) | Docker | Chroma Cloud |
| **Qdrant** | Docker / in-memory | Docker/K8s | Qdrant Cloud |
| **Weaviate** | Docker | Docker/K8s | Weaviate Cloud |
| **Milvus** | Docker/K8s / Milvus Lite | K8s | Zilliz Cloud |
| **Pinecone** | ❌ | ❌ | Только cloud |

### 3.3. Доступность из России (общая оценка)

| Слой | Статус | Необходимые меры |
|------|--------|-----------------|
| **GitHub** | Доступен без VPN (на май 2026) | — |
| **npm / PyPI** | Доступны без VPN | — |
| **Docker Hub** | Доступен | Зеркала на случай блокировки |
| **Anthropic API** | ❌ Заблокирован | VPN + зарубежная карта/криптовалюта |
| **OpenAI API** | ❌ Заблокирован | VPN + зарубежная карта |
| **OpenRouter** | Доступен (прокси) | Работает как прокси к большинству LLM |
| **Google Gemini API** | ❌ Заблокирован | VPN |
| **Локальные модели (Ollama)** | ✅ Полный доступ | Не требует внешнего API |
| **Векторные БД (локально)** | ✅ Полный доступ | Не требует внешнего API |
| **Mem0 Cloud / Letta Cloud** | ❌ (VPN) | VPN + зарубежная карта |

---

## 4. KEY FEATURES SUMMARY

### 4.1. Кодинг-агенты — сводная таблица

| Агент | Stars | OS | Язык | Лицензия | MCP | AgentSkills | Плагин-маркетплейс | Локальный LLM |
|-------|-------|----|------|----------|-----|-------------|-------------------|---------------|
| **Claude Code** | 121k | ❌* | TS/Py | Проприетарная | Да | Да | Да (официальный) | Нет (только Claude) |
| **OpenClaw** | 369k | Да | TS | MIT | Да | Да | Да (ClawHub, 5400+) | Да (любые) |
| **Cline** | 61.5k | Да | TS | Apache 2.0 | Да | Да | Нет (MCP сообщество) | Да (Ollama) |
| **Pi-agent** | 45.8k | Да | TS | MIT | Частично | Да | Нет (npm пакеты) | Да (vLLM) |
| **Aider** | 44.5k | Да | Py | Apache 2.0 | Ограничено | Нет | Нет | Да (частично) |
| **Crush** (ex-OpenCode) | 12.4k | Да | Go | MIT | Да | Нет | Нет | Да |

*код в репозитории открыт, но не полностью open-source по лицензии

### 4.2. Memory-решения — сравнение

| Решение | Stars | OS | Self-host | MCP | Подход |
|---------|-------|----|-----------|-----|--------|
| **Mem0** | 55k | Да | Да | Да | Multi-level memory (User/Session/Agent) + мультисигнальный retrieval |
| **Letta** | 22.5k | Да | Да | Нет* | Self-editing memory blocks + continual learning |
| **ChromaDB** | 27.8k | Да | Да | Да | Векторная БД, 4-функциональное API |
| **Qdrant** | 31.1k | Да | Да | Нет | Векторная БД с фильтрацией payload + квантование |
| **Weaviate** | 16.1k | Да | Да | Да | Векторная БД + гибридный поиск + RAG |
| **Milvus** | 44.2k | Да | Да | Нет | Распределённая векторная БД (Go+C++) |
| **LangMem** | 1.4k | Да | Да | Нет | Memory SDK для LangGraph |
| **Zep** | 4.5k | ❌ | ❌ | Да | Graph RAG + temporal knowledge graph |
| **Pinecone** | — | ❌ | ❌ | Нет | Serverless векторная БД (cloud only) |

*Letta имеет REST API, но не MCP

### 4.3. Рекомендуемый стек для РФ (2026)

**Для индивидуального разработчика:**
- CLI-агент: **Pi-agent** или **Aider** — полностью открытые, работают с OpenRouter/локальными моделями
- VSCode-агент: **Cline** — MCP, OpenRouter, локальные модели через Ollama
- Память: **Mem0** (локальный self-host) + **ChromaDB** (локально embedded)
- Модели: OpenRouter (прокси) или Ollama с локальными моделями (Gemma, Llama, Qwen)

**Для команды:**
- Gateway: **OpenClaw** — self-hosted, каналы (Telegram/WhatsApp/Slack), скиллы через ClawHub
- Плагины: ClawHub > 5400 скиллов, категоризировано
- Память: **Mem0 self-hosted** server или **Letta API self-hosted**
- Векторная БД: **Qdrant** или **Milvus** (оба self-host, Apache 2.0)
- MCP-серверы: сообщество MCP (85k звёзд на modelcontextprotocol/servers)

**Рекомендации по обходу ограничений:**
- Все open-source инструменты и векторные БД работают локально без VPN
- OpenRouter — ключевой прокси для доступа к западным LLM без прямого VPN
- Ollama / LM Studio для полностью офлайн-решений
- Оплата API: карты иностранных банков / криптовалюты / посредники
- GitHub, npm, PyPI, Docker Hub — на май 2026 доступны без VPN (рекомендуется настроить зеркала)

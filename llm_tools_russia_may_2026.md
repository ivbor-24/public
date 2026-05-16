---
layout: default
title: Инструменты LLM в России — май 2026
---

# Инструменты для работы с LLM в России — май 2026

Обзор рынка: онлайн-чаты, API-провайдеры, агентные инструменты, локальный инференс, репозитории моделей.

---

## 1. Онлайн-чаты (web-интерфейс)

### 1.1. Доступные без VPN

| Чат | Вендор | Страна | Текст | Изобр. | Ген. изобр. | Файлы | Голос | Код | Поиск | Уникальные фичи веб-интерфейса |
|---|---|---|---|---|---|---|---|---|---|---|
| **DeepSeek Chat** | DeepSeek | КНР | ✓ | ✓* | ✗ | ✓ | ✗ | ✓ | ✓ | V4-Pro с 1M токенов контекста; редкие обновления (V4 — апрель 2026); модель открыта (MIT) |
| **Qwen Chat** | Alibaba | КНР | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | Qwen Studio — переключение моделей (Qwen3.6-Plus и др.); встроенная генерация изображений (Qwen Image); **видеопонимание**; голосовой ввод; кодинг-режим с возможностью подключения репозитория |
| **Kimi** | Moonshot AI | КНР | ✓ | ✓ | ✗ | ✓ | ✗ | ✓ | ✓ | Сверхдлинный контекст (200K+ токенов); **встроенный генератор презентаций (PPT)**; Kimi+ — агенты для специализированных задач; кодинг-режим |
| **Doubao** | ByteDance | КНР | ✓ | ✓ | ✓ | ✓ | ✓ | ✗ | ✓ | **Голосовой диалог** — естественная речь; AI-персонажи; экосистема Douyin/TikTok |
| **Ernie Bot** | Baidu | КНР | ✓ | ✓ | ✓ | ✓ | ✗ | ✓ | ✓ | Плагины расширения; глубокая интеграция с поиском Baidu; ERNIE 4.5 |
| **Spark** | iFlytek | КНР | ✓ | ✓ | ✗ | ✓ | ✓ | ✗ | ✗ | **Лидер голосовых технологий** — распознавание и синтез речи; отраслевые ассистенты (медицина, право, образование) |
| **YandexGPT** | Яндекс | РФ | ✓ | ✗ | Шедеврум† | ✓ | ✓ | ✓ | ✓ | Интеграция с сервисами Яндекса (почта, карты, музыка); **Яндекс 300** — реферат лонгрида, подкаста или длинного видео по ссылке; Алиса Про (голос, по Плюсу); Шедеврум для изображений |
| **GigaChat** | Сбер | РФ | ✓ | ✓ | ✓ Kandinsky | ✓ | Салют† | ✓ | ✗ | **Kandinsky** — генерация изображений прямо в чате; экосистема Сбера (банк, умный дом); бесплатный тариф |
| **z.ai** | Zhipu AI | КНР | ✓ | ✓ | ✓ GLM-Image | ✓ | ✗ | ✓ | ✓ | GLM-5.1 (уровень Opus 4.6); Agent mode с генерацией .docx/.pdf/.xlsx; 200K контекст; бесплатно |
| **MiniMax** | MiniMax | КНР | ✓ | ✓ | ✗ | ✓ | ✓ | ✓ | ✓ | MiniMax-M1 — 1M контекст, open-weight; голосовой ввод/вывод; Agent mode; бесплатно без регистрации |
| **StepFun / 阶跃AI** | StepFun | КНР | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | Step-3.5-Flash; генерация видео; мультимодальность; бесплатно |

\* Чтение текста из изображений, без генерации. † Отдельный сервис/ассистент, не в веб-интерфейсе чата.

**Примечания:**
- Все китайские чаты работают без VPN в РФ (май 2026). Интерфейс почти везде есть на русском (бывают редкие поблемы со шрифтами).
- **DeepSeek** — регистрация по email+паролю (или Google-аккаунт). Самый популярный китайский чат. Полностью бесплатный. Самый большой контекст.
- **Qwen Chat** — регистрация по email, интерфейс на русском. Мультимодальность + генерация изображений.
- **Kimi, Doubao, Ernie Bot, Spark** — требуют китайский номер телефона для регистрации, варианты с регистрацией по почте есть, но работают не всегда.
- **z.ai** — регистрация по Google-аккаунту. GLM-5.1 — флагман уровня Claude Opus 4.6, SWE-Bench Pro 58.4.
- **MiniMax** — без регистрации. MiniMax-M1: 1M контекст, open-weight, гибридное внимание.
- **YandexGPT** — лучший русскоязычный опыт. Часть функций по подписке Яндекс Плюс (~299 ₽/мес).
- **GigaChat** — базовый тариф бесплатный. Платные тарифы MAX/Pro.

### 1.2. Требуют VPN

| Чат | Вендор | Ключевые модели (май 2026) | Уникальные фичи веб-интерфейса | Плата |
|---|---|---|---|---|
| **ChatGPT** | OpenAI (США) | GPT-5.5, GPT-5.4 | Canvas (интерактивное редактирование текста/кода), DALL-E 3 (изображения), Sora (видео), **GPT-магазин** кастомных агентов, Deep Research, Code Interpreter, Projects | $20–200/мес, нужна иностранная карта |
| **Claude** | Anthropic (США) | Opus 4.7, Sonnet 4.6, Haiku 4.5 | **Artifacts** — интерактивные мини-приложения прямо в чате; **Cowork** — автономное выполнение задач в десктоп-приложении; Projects; 1M контекст; Skills | $20–200/мес, нужна иностранная карта |
| **Gemini** | Google (США) | Gemini 2.5 Pro/Flash | **Deep Research**; Gems (кастомные ассистенты); Canvas; **глубокая интеграция** с Gmail, Docs, Drive, YouTube, Maps, Calendar; NotebookLM; Veo (видео) | Бесплатно / Advanced $20/мес |
| **Grok** | xAI (США) | Grok 4, Grok 4.1 | Deep/Deeper Search; **Aurora** — генерация изображений; **интеграция с X (Twitter)** — анализ твитов; Big Brain; «Fun Mode» — менее фильтрованные ответы | Требуется X-аккаунт |
| **Perplexity** | Perplexity AI (США) | Sonar / GPT-5.5 / Claude / Grok | **Pro Search** с уточняющими вопросами и полным цитированием; Pages — генератор статей; Spaces; Collections; Focus-режимы (Academic, Writing, Math) | Бесплатно / Pro $20/мес |
| **Mistral** | Mistral AI (Франция) | Mistral Large | Le Chat Agents (настраиваемые); Canvas; Flux (генерация изображений); Code Interpreter | Бесплатно / Pro / Team |
| **Microsoft Copilot** | Microsoft (США) | GPT-4.1/4.5 | DALL-E 3, Deep Research, Pages, интеграция с M365/Edge/Windows | Бесплатно / Pro $20/мес |
| **Meta AI** | Meta (США) | Llama 4 | Интеграция с WhatsApp/Instagram/Facebook; Imagine (генерация изображений); голосовой режим | Бесплатно |

**Для всех:** требуется VPN + иностранная карта для платной подписки (кроме Perplexity Free, Mistral Free и Meta AI).

---

## 2. API-провайдеры

### 2.1. Сводная таблица

| Провайдер | Тип | VPN | Оплата из РФ | Ключевые модели | Способ оплаты |
|---|---|---|---|---|---|
| **DeepSeek** | Вендор | ✗ | Ограничена | V4-Pro (1.6T MoE), V4-Flash | UnionPay / PayPal (не РФ) / посредники |
| **Qwen (Alibaba)** | Вендор | ✗ | Ограничена | Qwen3.6, Qwen3.5, Qwen3-VL | Иностранная карта / бизнес-контракт / посредники |
| **Moonshot/Kimi** | Вендор | ✗ | Ограничена | Kimi-K2.6 (MoE, 256K) | Китайские платёжные системы |
| **Z.ai** | Вендор | ✗ | Ограничена | GLM-5.1, GLM-5, GLM-5-Turbo, GLM-4.7 | Иностранная карта / посредники (**есть free tier!**) |
| **Nvidia** | **Вендор** (Nemotron + хостинг через NIM) | ✗ | Ограничена | Nemotron 3 Nano Omni 30B-A3B (reasoning), DeepSeek V4 Pro, GLM-5.1, Gemma 4, Llama (затюненные варианты) | Иностранная карта (**есть free tier!**) |
| **OpenRouter** | **Агрегатор** (400+ моделей) | ✗ | ✅ **Крипта!** | GPT-5.5, Claude, Gemini, DeepSeek, Qwen, Kimi, GLM, Llama и др. | **Криптовалюта (USDT/BTC)** — лучший вариант для РФ |
| **DeepInfra** | Агрегатор (100+ моделей) | ✗ | Ограничена | DeepSeek V4, Kimi K2.6, Qwen, GLM | Иностранная карта |
| **Together AI** | Агрегатор (200+ моделей) | ✗ | Ограничена | DeepSeek, Qwen, Kimi, Llama, Mistral, FLUX | Иностранная карта / Enterprise-инвойс |
| **Groq** | Агрегатор (LPU-чипы) | ✗ | Ограничена | Llama, Qwen, Mistral, DeepSeek (open-source) | Иностранная карта (**есть free tier!**) |
| **Cerebras** | Агрегатор (CS-3 wafer-scale чипы) | ✗ | Ограничена | GPT-OSS-120B, Llama 4 Scout/Maverick, Llama 3.3-70B, Qwen 3-235B (Thinking), GLM-4.7 | Иностранная карта (**есть free tier!**) — до 3 000 токенов/с |
| **OpenCode** | **Агрегатор** (12+ моделей, агентно-оптимизированные) | ✗ | Ограничена | DeepSeek V4 Pro/Flash, Qwen3.6 Plus, Qwen3.5 Plus, Kimi K2.6, GLM-5.1, MiniMax M2.7, MiMo-V2.5-Pro | **Zen**: pay-as-you-go ($20 пополнение, нулевая наценка, карта). **Go**: подписка $10/мес ($5 первый месяц) |
| **Fireworks AI** | Агрегатор | ✗ | Ограничена | DeepSeek V4, Kimi K2.6, Qwen3.6, GLM | Иностранная карта |
| **OpenAI** | Вендор | ✓ | Заблокирована | GPT-5.5, GPT-5, o4-pro | Только иностранная карта + VPN |
| **Anthropic** | Вендор | ✓ | Заблокирована | Claude Opus 4.7, Sonnet 4.6 | Только иностранная карта + VPN |
| **Google AI** | Вендор | ✓ | Заблокирована | Gemini 2.5 Pro/Flash | Только иностранная карта + VPN |
| **YandexGPT** | **Вендор (РФ)** | ✗ | ✅ **Полная** | YandexGPT Pro/Lite/Summarization, YandexART | **Российские карты, Яндекс.Облако, счёт юрлицам** |
| **GigaChat** | **Вендор (РФ)** | ✗ | ✅ **Полная** | GigaChat 2 Max/Pro/Lite, Kandinsky, Embeddings | **Российские карты, Сбер ID, счёт юрлицам** |
| **MTS AI** | **Вендор (РФ)** | ✗ | ✅ **Полная** | MTS AI Chat/Vision | Российские карты |

### 2.2. Ключевые выводы

- **OpenRouter + криптовалюта** — оптимальный способ получить доступ к западным моделям без VPN и иностранной карты. За каждый платеж OpenRouter возьмет комиссию — 5.5%.
- **DeepSeek API** — доступен напрямую без VPN, но оплата через китайские платёжные системы.
- **Nvidia NIM** — free tier с доступом к собственным затюненным моделям Nemotron и популярным open-source моделям. Оплата иностранной картой.
- **Z.ai API** — free tier, GLM-5.1 (уровень Opus 4.6), оптимизирован под Claude Code и OpenClaw.
- **OpenCode (Zen/Go)** — агрегатор, заточенный под использование в кодинг-агентах (в первую очередь, под их же опен-сорцный OpenCode. Тариф Zen — pay-as-you-go ($20, без наценки), тариф Go — $10/мес с щедрыми лимитами на open-source модели. Работает без VPN, но нужна иностранная карта.
- **Groq** — free tier без VPN. Быстрый инференс за счёт собственных LPU-чипов.
- **Cerebras** — сверхбыстрый инференс на wafer-scale чипах CS-3 (до 3 000 токенов/с). Free tier. Pay-per-token от $10.
- **Российские провайдеры** (YandexGPT, GigaChat, MTS AI) — полная поддержка российских карт, данные в РФ, но качество моделей отстаёт от западных/китайских флагманов.
- **GigaChat** — самый выгодный российский вариант: Freemium с 1M бесплатных токенов.

---

## 3. Инструменты для агентной работы

### 3.1. Агенты общего назначения (ассистенты)

| Инструмент | Интерфейс | Каналы | Память | Self-host | MCP | Самообучение | Язык | GitHub | Цена |
|---|---|---|---|---|---|---|---|---|---|
| **OpenClaw** | CLI (TUI) / Gateway + Web UI / iOS + Android / Desktop | 24+ (WhatsApp, Telegram, Slack, Discord, Signal, iMessage, Matrix и др.) | Config-файлы, context engine | Да (Docker/локально) | Да (bundle-плагины) | Частично | TypeScript | 369K ★ | Бесплатно (MIT) |
| **Hermes Agent** | CLI (TUI) / Gateway / Web UI | Telegram, Discord, Slack, WhatsApp, Signal, Email, CLI | MEMORY.md, USER.md, FTS5 поиск | Да (Python/VPS) | Да | **Да** (auto-skills) | Python + TS | 104K ★ | Бесплатно (MIT) |
| **Moltis** | Web UI / CLI | Telegram, WhatsApp, Discord, Slack, Matrix, Nostr, Teams | SQLite + FTS + vector | Да (single binary, Rust) | Да | Нет | Rust | — | Бесплатно |
| **Leon** | Web UI / CLI | Web, голос | Layered memory | Да (Node.js) | Нет | Нет | TS + Python | 17K ★ | Бесплатно (MIT) |
| **OpenAkita** | GUI / CLI | Telegram, Feishu, WeCom, DingTalk, QQ | Daily health-check | Да (Python) | Да | Да (self-taught skills) | Python + TS + Rust | 1.7K ★ | Бесплатно (Apache 2.0) |

**Примечание:** OpenClaw — не кодинг-агент, а персональный AI-ассистент с мультиканальным Gateway. Агентный движок на Pi-agent SDK. Skills-система ClawHub — 5400+ навыков.

**Примечание:** Hermes Agent (Nous Research) — самообучающийся агент с persistent memory. Создаёт reusable skills из опыта, встроенный cron-планировщик, субагенты, браузерная автоматизация. 18+ LLM-провайдеров.

### 3.2. Кодинг-агенты (open-source)

| Инструмент | Тип клиента | Интерфейс | Windows | macOS | Linux | Плагины/MCP | GitHub | Цена |
|---|---|---|---|---|---|---|---|---|
| **OpenCode** | Отдельный | CLI / Desktop / IDE / Web | ✓ | ✓ | ✓ | MCP, плагины | 150K ★ | Бесплатно |
| **Cline** | Встройка | VS Code / CLI | ✓ | ✓ | ✓ | MCP (создание из чата) | 61.5K ★ | Бесплатно |
| **Pi-agent** | Отдельный | CLI (TUI) / RPC / SDK | ✓ (WSL2) | ✓ | ✓ | Extensions + Skills (**нет MCP**) | 45.8K ★ | Бесплатно (MIT) |
| **Aider** | Отдельный | CLI | ✓ | ✓ | ✓ | Нет | 44.5K ★ | Бесплатно |
| **Continue** | Встройка | VS Code / JetBrains / CLI | ✓ | ✓ | ✓ | MCP, агенты как Markdown | 33K ★ | Бесплатно |
| **Qwen Code** | Отдельный | CLI / VS Code / JetBrains / Zed | ✓ | ✓ | ✓ | MCP, Skills, SubAgents | 24K ★ | Бесплатно |
| **Roo Code** | Встройка | VS Code | ✓ | ✓ | ✓ | MCP, Custom Modes | 24K ★ | Бесплатно |
| **LangChain** | Фреймворк | Библиотека (Python/TS) | ✓ | ✓ | ✓ | MCP, Deep Agents | 136K ★ | Бесплатно |
| **CrewAI** | Фреймворк | Библиотека / CLI | ✓ | ✓ | ✓ | MCP | 51K ★ | Бесплатно |
| **AutoGPT** | Отдельный | Платформа / CLI / Web | ✓ | ✓ | ✓ | Частично | 184K ★ | Бесплатно |
| **MetaGPT** | Отдельный | CLI | ✓ | ✓ | ✓ | Нет | 68K ★ | Бесплатно |

**Примечание:** Pi-agent — минималистичный terminal-based harness. Философия: «адаптируй pi под себя». 4 режима: TUI, Print/JSON, RPC, SDK. Собственный TUI-движок (`@mariozechner/pi-tui`). MCP не поддерживает принципиально.

### 3.3. Кодинг-агенты (проприетарные)

| Инструмент | Тип клиента | Вендор | Интерфейс | Windows | macOS | Linux | MCP | Особенности | Цена |
|---|---|---|---|---|---|---|---|---|---|
| **Codex** | Отдельный | OpenAI (США) | Desktop / VS Code / CLI / Web | ✓ | ✓ | ✓ | Да | Cloud-агенты, worktrees, computer use, 90+ плагинов | В подписке ChatGPT ($20–200/мес) |
| **Claude Code** | Отдельный | Anthropic (США) | CLI / IDE / Desktop / Web | ✓ | ✓ | ✓ | Да | Автономная работа с кодом и PR; худшая доступность в РФ | $20–200/мес |
| **Claude Cowork** | Отдельный | Anthropic (США) | Desktop GUI / Web | ✓ | ✓ | — | Плагины | Автономные задачи для нетехнических | В подписке |
| **Cursor** | Отдельный | Anysphere (США) | AI IDE / CLI / Slack | ✓ | ✓ | ✓ | MCP | Composer 2; Tab-модель; 50%+ Fortune 500 | Free–$40/мес |
| **GitHub Copilot** | Встройка | Microsoft (США) | VS Code / JetBrains / Xcode / CLI / Web | ✓ | ✓ | ✓ | MCP | Copilot, Claude, Codex — модель на выбор | Free–$39/мес |
| **Windsurf** | Отдельный | Cognition AI (США) | AI IDE / JetBrains | ✓ | ✓ | ✓ | MCP | Cascade + Devin; Agent Command Center | Free–$15/мес |
| **Antigravity** | Отдельный | **Google** (США) | Desktop (Electron) | ✓ | ✓ | ✓ | Cloud Code endpoint | Регионально ограничен; есть community patcher | Freemium |
| **Cody** | Встройка | Sourcegraph (США) | VS Code / JetBrains / VS / Web / CLI | ✓ | ✓ | ✓ | MCP | Глубокое понимание кодовой базы | Freemium |

### 3.4. Российские агентные инструменты

Специализированных российских AI-агентов для работы с кодом по состоянию на май 2026 **не существует**. YandexGPT и GigaChat — LLM общего назначения, не agentic tools. Адаптация open-source решений (Cline, Aider, Qwen Code) с локальными или российскими API-провайдерами — основной путь для разработчиков в РФ.

---

## 4. Экосистемы расширений и дополнительные инструменты

Поверх агентов выстраиваются целые экосистемы плагинов, скиллов и вспомогательных инструментов. Они добавляют агентам новые способности, управляют контекстом между сессиями, хранят долговременную память.

### 4.1. Плагины и MCP-серверы

Плагины расширяют функциональность агента — дают доступ к файловой системе, базам данных, API, браузеру, терминалу. Без плагинов агент умеет только генерировать текст.

**MCP (Model Context Protocol)** стал универсальным стандартом подключения инструментов. Репозиторий `modelcontextprotocol/servers` — 85K звёзд, 10K форков, тысячи community-серверов. MCP работает через stdio или HTTP/SSE, позволяет подключить любой внешний инструмент без написания кода внутри самого агента.

**Реестры MCP-серверов:**

| Реестр | Кол-во серверов | Бесплатно | Платные | Особенности |
|---|---|---|---|---|
| **Smithery** (smithery.ai) | 1000+ | ✓ | ✓ | Крупнейший каталог, рейтинг, отзывы, one-click install |
| **PulseMCP** (pulsemcp.com) | 500+ | ✓ | — | Полностью бесплатный, open-source каталог |
| **MCPM** (mcpm.sh) | 300+ | ✓ | — | CLI-менеджер: установка, обновление, конфигурация MCP |
| **mcp-get** (mcp-get.com) | 200+ | ✓ | — | npm-подобный менеджер: `npx mcp-get install <server>` |

**Нативные плагины vs MCP:** нативные плагины (`.openclaw.plugin.json`, `.claude-plugin/`) глубже интегрированы в агента, имеют доступ к хукам и внутренним событиям. MCP-серверы универсальны, но работают в изолированном процессе.

| Агент | Формат плагинов | MCP | Особенности |
|---|---|---|---|
| **OpenClaw** | Native (`.openclaw.plugin.json`) + bundle (Codex/Claude/Cursor) | Да (через bundle) | Крупнейшая экосистема; ClawHub — 5400+ скиллов, 52.7K инструментов |
| **Claude Code** | `.claude-plugin/plugin.json` + хуки (9 событий) | Да (`.mcp.json`) | 13 официальных плагинов: code-review, feature-dev, pr-review-toolkit |
| **Cline** | MCP (создание из чата) | Да | **Уникальная фича:** агент сам пишет и устанавливает MCP-серверы по текстовому описанию |
| **Pi-agent** | Extensions (TypeScript-модули), Pi Packages (npm) | Нет (принципиально) | Extensions регистрируют инструменты, команды, hotkeys, UI-компоненты |
| **OpenCode** | Custom Commands (Markdown), MCP | Да | MCP через stdio/SSE; 75+ LLM-провайдеров; LSP-автозагрузка |
| **Cursor** | `.cursor/rules`, `.cursor-plugin` | Да | AgentSkills |
| **Windsurf** | `.windsurfrules` | Да | Ограничено |

### 4.2. Скиллы (Skills)

Скилл — это не код, а **инструкция + контекст**. Файл `SKILL.md` с YAML frontmatter описывает, что агент должен делать в определённой ситуации. Модель сама решает, когда активировать скилл, по ключевым словам и контексту задачи.

**Главное отличие от плагинов:** плагин добавляет новый инструмент (функцию, API-вызов), скилл добавляет новые знания и поведенческие паттерны. Скилл не требует программирования — это markdown-файл с инструкциями.

**Стандарт AgentSkills (SKILL.md)** — совместим между Pi, Claude Code, Cline, OpenClaw, OpenCode. YAML frontmatter содержит `name`, `description`, `triggers` — по ним модель определяет, какой скилл применить.

**Реестры скиллов:**

| Реестр | Кол-во | Агент | Доступ |
|---|---|---|---|
| **ClawHub** (clawhub.ai) | 5400+ скиллов, 52.7K инструментов | OpenClaw | Открытый, любой пользователь GitHub может опубликовать |
| **Anthropic Marketplace** | 13 официальных + приватные для команд | Claude Code | Официальный + приватные маркетплейсы |
| **Community Skills** | Сотни в репозиториях | Cline, Pi-agent, OpenCode | GitHub, `.agents/skills/` |

**Конвергенция форматов:** OpenClaw поддерживает bundle-плагины Codex/Claude/Cursor, SKILL.md работает в 5+ агентах, MCP принят всеми основными игроками. Экосистема движется к единому стандарту.

### 4.3. Контекст-файлы

Помимо плагинов и скиллов, поведение агента задаётся через markdown-файлы в корневой директории проекта. Это самый простой способ «настроить» агента без единой строчки кода:

| Файл | Назначение | Где используется |
|---|---|---|
| **AGENTS.md** | Общие инструкции для всех агентов в проекте | OpenClaw, Cline, Codex, Cursor |
| **SOUL.md** | Личность, стиль общения, ценности агента | OpenClaw, Hermes Agent, Vellum |
| **TOOLS.md** | Описание доступных инструментов и когда их применять | OpenClaw |
| **USER.md** | Профиль пользователя: предпочтения, стиль, проекты | Hermes Agent, OpenClaw |
| **MEMORY.md** | Долговременная память агента | Hermes Agent |
| **.clinerules** | Правила поведения для Cline | Cline |
| **.cursorrules** | Правила поведения для Cursor | Cursor |
| **.windsurfrules** | Правила поведения для Windsurf | Windsurf |
| **.codex/environments** | Окружения и конфигурации для Codex | Codex |

Эти файлы автоматически подхватываются агентом при старте сессии и инжектируются в системный промпт. Их можно версионировать в Git, шарить между проектами и командами.

### 4.4. Память агентов

Обычный агент «забывает» всё после завершения сессии. Memory-решения сохраняют и извлекают релевантный контекст из прошлых взаимодействий.

**Типы памяти:**
- **Session memory** — контекст внутри одной сессии (есть у всех агентов)
- **Cross-session memory** — предпочтения, факты, стиль пользователя между сессиями
- **Long-term / archival memory** — архив с recall-механизмом для восстановления контекста

| Решение | Тип | Звёзд | Self-host | MCP | Подключение | Цена | Особенности |
|---|---|---|---|---|---|---|---|
| **Mem0** | Open-source (Apache 2.0) + Cloud | 55K | Да (`pip install mem0ai` / Docker) | Да | Библиотека / Docker / Cloud | Бесплатно (self-host) / Cloud от $20/мес | Multi-level memory (User/Session/Agent); v3: single-pass ADD-only экстракция, entity linking, multi-signal retrieval; бенчмарки 91.6 LoCoMo / 93.4 LongMemEval |
| **Letta** (ex-MemGPT) | Open-source (Apache 2.0) + Cloud | 22.5K | Да (Docker) | Нет (REST API) | Docker / Cloud | Бесплатно (self-host) / Cloud от $25/мес | Self-editing memory blocks; агент сам обновляет память; архивная память + recall |
| **LangMem** | Open-source (MIT) | 1.4K | Да (`pip install langmem`) | Нет | Библиотека | Бесплатно | Memory SDK для LangGraph; core memory API; background memory manager |
| **Zep** | Проприетарное облако | 4.5K | ❌ (deprecated) | Да | Cloud only | От $49/мес | Graph RAG + temporal knowledge graph (Graphiti); sub-200ms latency; SOC2/HIPAA |

### 4.5. Векторные базы данных

Все memory-решения опираются на векторные БД для хранения и поиска. Для продвинутых пользователей — возможность развернуть свой memory backend без готовых решений.

| БД | Звёзд | Язык | Лицензия | Сложность | Локально | Облако | Особенности |
|---|---|---|---|---|---|---|---|
| **ChromaDB** | 27.8K | Rust + Python | Apache 2.0 | ★☆☆ (легко) | Да (embedded / Docker) | Chroma Cloud | API из 4 функций; встроена в Mem0 по умолчанию; `pip install chromadb` |
| **Qdrant** | 31.1K | Rust | Apache 2.0 | ★★☆ (средне) | Да (Docker / in-memory) | Qdrant Cloud (free tier) | Квантование векторов (экономия RAM до 97%); фильтрация по payload |
| **Milvus** | 44.2K | Go + C++ | Apache 2.0 | ★★★ (сложно) | Да (Docker/K8s, Milvus Lite) | Zilliz Cloud (free tier) | GPU acceleration, fully distributed, 10B+ векторов |
| **Weaviate** | 16.1K | Go | BSD-3 | ★★☆ (средне) | Да (Docker) | Weaviate Cloud | Гибридный поиск, RAG, реранкинг, мультиарендность |
| **Pinecone** | — | — | Проприетарная | ★☆☆ (легко) | ❌ (cloud only) | Pinecone Cloud | Serverless, SOC2/HIPAA; только API |

**Когда нужна векторная БД:** если вы строите RAG-систему, работаете с большими документами, или хотите кастомную память агента с семантическим поиском. Для большинства пользователей достаточно Mem0 (self-hosted) с ChromaDB — это минимум кода и максимум результата.

### 4.6. Доступность из России и рекомендации

**Полностью локальные решения** (Pi-agent, Cline, Aider + Mem0 self-hosted + ChromaDB/Qdrant/Milvus локально + Ollama) — работают без VPN, без внешних API, без иностранных карт. Это полноценный офлайн-стек.

**Смешанные решения** — агент локально, LLM через OpenRouter (крипта), память локально. Доступ к GitHub, npm, PyPI, Docker Hub — без VPN (май 2026).

**Облачные решения** (Zep Cloud, Mem0 Cloud, Letta Cloud, Pinecone) — требуют VPN и иностранную карту. Для российского пользователя предпочтительны self-hosted альтернативы.

Рекомендуемый стек: **Cline (VSCode) или Pi-agent (CLI) + OpenRouter (API-прокси) + Mem0 self-hosted (память) + Qdrant (векторная БД) + MCP-серверы сообщества** — всё локально, кроме LLM, которая идёт через OpenRouter без VPN.

---

## 5. Инструменты для локального инференса

### 5.1. Движки инференса (backend)

| Инструмент | Тип | Платформы | Распределённый | API | Форматы | GPU | Ключевые особенности | Звёзды |
|---|---|---|---|---|---|---|---|---|
| **llama.cpp** | Open-source (C++) | Win, Lin, Mac, iOS, Android, RISC-V | ✓ Multi-GPU + **Multi-node RPC** | OpenAI-совместимый (`llama-server`) | GGUF | CUDA, Metal, Vulkan, SYCL, HIP, MUSA, CANN | 200+ архитектур; квантование 1.5–8 бит; **чистый C++**; CPU+GPU гибрид | 109K |
| **Ollama** | Проприетарная обёртка | Win, Lin, Mac | ✗ | OpenAI-совместимый; Ollama Cloud | GGUF (llama.cpp) | CUDA, Metal | **Простейшая установка**: `ollama run llama3`; реестр моделей; платный Pro/Max | 109K |
| **vLLM** | Open-source (Python) | Linux; NVIDIA/AMD/Intel/TPU/Ascend | ✓ Tensor/Pipeline/Data/Expert parallelism; **Multi-node** | OpenAI + Anthropic API + gRPC | HF, GGUF, GPTQ/AWQ, FP8, INT4/8 | CUDA, ROCm, Gaudi, TPU, Ascend | PagedAttention; 200+ архитектур; continuous batching; `pip install vllm` | 79.3K |
| **SGLang** | Open-source (Python) | Linux; NVIDIA/AMD | ✓ Tensor parallelism; Multi-node | OpenAI-совместимый | HF, GGUF | CUDA, ROCm | **RadixAttention** — prefix caching 85-95% (RAG/multi-turn); **xGrammar** для структурированного JSON; на 29% быстрее vLLM на RAG-нагрузках | 18K |
| **MLX** | Open-source (Apple) | Mac (Apple Silicon), Linux | Multi-device (CPU+GPU unified) | Python API (`mlx-lm`); finetuning (LoRA) | MLX, HF, GGUF | Apple Silicon GPU | **Разработан Apple**; NumPy-подобный API; lazy computation; autograd | 26K |
| **ExLlamaV3** | Open-source (Python/C++) | Win, Lin (только NVIDIA) | Multi-GPU | TabbyAPI (OpenAI-совместимый) | GPTQ, EXL2, EXL3 (2–8 бит) | CUDA | Преемник ExLlamaV2; максимальная производительность на NVIDIA | 4.5K |
| **TensorRT-LLM** | Open-source (NVIDIA) | Linux (только NVIDIA) | ✓ Tensor parallelism | OpenAI-совместимый | HF, TensorRT engine | CUDA (только NVIDIA) | **Максимальная пропускная способность** на H100/B200; FP4 inference; 28 мин компиляции на модель | 12K |

### 5.2. Интерфейсы и платформы (frontend)

| Инструмент | Тип | Платформы | Подключение | MCP | RAG | Ключевые особенности | Звёзды |
|---|---|---|---|---|---|---|---|
| **Open WebUI** | Open-source (Web) | Docker, K8s, pip | Ollama, OpenAI, Anthropic, vLLM, любой OpenAI-compatible | Да | ✓ (9 векторных БД, 15+ поисковых провайдеров) | **Де-факто стандарт** self-hosted; multi-user с RBAC; Python-функции/пайплайны; code execution; voice/video calls; генерация изображений; 290M+ загрузок | 137K |
| **LM Studio** | Проприетарное (GUI) | Win, Lin, Mac | Встроенный (llama.cpp), Ollama, удалённые инстансы | Да (клиент) | ✗ | **Десктопный GUI**; встроенный каталог моделей; side-by-side сравнение; headless (`llmster`); бесплатный для коммерческого использования | — |
| **TextGen (oobabooga)** | Open-source (Python) | Win, Lin, Mac | Встроенный (Transformers, llama.cpp, ExLlamaV3, TensorRT-LLM) | Да (сервер) | ✗ | **Веб-интерфейс (Gradio)**; multimodal; LoRA-тренировка; генерация изображений; TTS; 100% оффлайн | 47K |
| **GPT4All** | Open-source (GUI) | Win, Lin, Mac | Встроенный (llama.cpp) | ✗ | ✓ (LocalDocs) | LocalDocs — чат с документами без интернета; Python API; Vulkan-ускорение (NVIDIA + AMD) | 77.4K |
| **KoboldCpp** | Open-source (C++) | Win, Lin, Mac, **Android (Termux)**, RPi | Встроенный (llama.cpp) | ✗ | ✗ | **Один исполняемый файл**; LLM + Image Gen + Video Gen + STT + TTS + Music Gen; KoboldAI Lite UI | 10.4K |
| **Jan** | Open-source (Desktop) | Win, Lin, Mac | Встроенный (llama.cpp, ONNX), облачные провайдеры | ✗ | ✗ | Приватный десктопный GUI; гибридный локальный/облачный режим; простой старт для non-tech | 82K |
| **LocalAI** | Open-source (Go) | Docker, Linux, Mac | Встроенный (llama.cpp, stablediffusion, whisper) | ✗ | ✗ | **Drop-in замена OpenAI API**; текст + изображения (SD) + TTS + STT через один endpoint | 26K |

**Когда что выбирать:**
- **Просто запустить модель** → Ollama (`ollama run llama3`) или LM Studio (GUI)
- **Максимум контроля** → llama.cpp напрямую (C++, квантование, все платформы)
- **Продакшен с высокой нагрузкой** → vLLM (универсальный) или SGLang (RAG/multi-turn, структурированный вывод)
- **Полноценная self-hosted платформа** → Open WebUI поверх Ollama/vLLM (multi-user, RAG, MCP, функции)
- **Apple Silicon** → MLX (разработан Apple, нативная оптимизация)
- **Максимум на NVIDIA** → TensorRT-LLM (H100/B200, FP4)

### 5.3. Российские инструменты для локального инференса

**Отсутствуют** как класс. Российские модели (GigaChat, Kandinsky) запускаются через стандартные международные инструменты (llama.cpp, vLLM). Из российских наработок:
- **GGUF-квантизации GigaChat 3.1** — опубликованы ai-sage на Hugging Face. Загружаются и запускаются через llama.cpp / Ollama как обычные GGUF.
- **GPT2Giga** (ai-forever) — FastAPI-прокси, подменяющий вызовы на GigaChat API, эмулирует OpenAI-совместимый endpoint.
- **GigaChain** — адаптер для LangChain под GigaChat API.

---

## 6. Репозитории открытых моделей

### 6.1. Доступные без VPN

| Репозиторий | Назначение | Примечание |
|---|---|---|
| **Hugging Face** (huggingface.co) | Основной мировой репозиторий — 2M+ моделей | ✅ Доступен из РФ (май 2026). Некоторые аккаунты РФ-организаций (sberbank-ai) удалены, но сайт открыт. |
| **GitHub** (github.com) | Хостинг кода, Git LFS для моделей, релизы | ✅ Доступен. |
| **ModelScope** (modelscope.cn) | Китайский аналог HF от Alibaba. Китайские модели (Qwen, DeepSeek, GLM, Yi и др.) | ✅ Доступен. Некоторые модели эксклюзивно на ModelScope. |
| **Ollama Library** (ollama.com/library) | Встроенный реестр моделей Ollama | ✅ Доступен. |
| **CivitAI** (civitai.com) | Репозиторий моделей для генерации изображений (SD, Flux) | ✅ Доступен. |

### 6.2. С VPN

- Hugging Face — формально доступен, но скачивание больших файлов с `cdn-lfs.huggingface.co` может работать нестабильно без VPN.
- Некоторые HF Spaces геоблокированы владельцами.

### 6.3. Российские открытые модели и их размещение

Собственного российского репозитория моделей (аналога Hugging Face) **не существует на май 2026**.

| Модель | Разработчик | Параметры | Где доступна |
|---|---|---|---|
| **GigaChat 3.1** | Сбер / ai-sage | 702B MoE (36B активных) | Hugging Face (ai-sage), GGUF, bf16 |
| **GigaChat 3.1** | Сбер / ai-sage | 11B MoE (1.8B активных) | Hugging Face (ai-sage), GGUF — 7.8K скачиваний |
| **GigaChat 3** | Сбер / ai-sage | 702B / 11B MoE | Hugging Face (ai-sage) |
| **ruGPT-3.5** (13B) | Сбер / ai-forever | 13B | GitHub (ai-forever/ru-gpts) |
| **Kandinsky 2–3** | Сбер / ai-forever | Diffusion | GitHub / Hugging Face |
| **YandexGPT** | Яндекс | Не раскрыты | **Только Yandex Cloud API** — закрытая модель |

Российские open-source модели представлены практически исключительно экосистемой Сбера и распространяются через Hugging Face (организация ai-sage). Яндекс не публикует открытых весов.

---

## 7. Итоговые рекомендации

### Для пользователя чатов в РФ (приоритет по качеству/удобству):

| Сценарий | Рекомендация |
|---|---|
| Бесплатно, без VPN, лучшая модель | **DeepSeek** — V4-Pro, Deep Think, английский интерфейс |
| Мультимодальность + генерация изображений без VPN | **Qwen Chat** — видеоанализ, Qwen Image |
| Лучший русскоязычный опыт | **YandexGPT** / **GigaChat** |
| Программирование (с VPN) | **Claude** (Artifacts, Cowork) или **ChatGPT** (Canvas, Code Interpreter) |

### Для разработчика API:

| Сценарий | Рекомендация |
|---|---|
| Нужны западные флагманы, нет иностранной карты | **OpenRouter + криптовалюта** — 400+ моделей |
| Бесплатный старт | **Groq Free Tier** или **GigaChat Freemium** (1M токенов) |
| Российский проект с требованиями к хранению данных в РФ | **GigaChat API** или **YandexGPT API** |
| Локальный инференс open-source моделей | **Ollama** (простота) → **llama.cpp / vLLM** (кастомная настройка) |

### Для агентной работы с кодом:

| Сценарий | Рекомендация |
|---|---|
| Бесплатный агент в VS Code | **Cline** или **Roo Code** + OpenRouter (крипта) / Groq |
| CLI-агент, любитель Git | **Aider** — автокоммиты, Repomap |
| Нужна мультиплатформенность (IDE + CLI + Web) | **OpenCode** |
| Проприетарный IDE (деньги есть) | **Cursor** (Pro $20/мес) или **GitHub Copilot** |
| Российский агент с нуля | Собрать связку **Cline + GigaChat API** или **Aider + OpenRouter** |

---

*Обзор составлен на основе открытых данных. Актуальность — 7 мая 2026. Ситуация с блокировками, ценами и доступностью может меняться.*

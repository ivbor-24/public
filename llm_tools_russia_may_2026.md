# Инструменты для работы с LLM в России — май 2026

Обзор рынка: онлайн-чаты, API-провайдеры, агентные инструменты, локальный инференс, репозитории моделей.

---

## 1. Онлайн-чаты

### 1.1. Доступные без VPN

| Чат | Вендор | Страна | Текст | Изобр. | Ген. изобр. | Файлы | Голос | Код | Поиск | Уникальные фичи веб-интерфейса |
|---|---|---|---|---|---|---|---|---|---|---|
| **DeepSeek Chat** | DeepSeek | КНР | ✓ | ✓* | ✗ | ✓ | ✗ | ✓ | ✓ | Deep Think (R1) — показ цепочки мыслей; V4-Pro с 1M токенов контекста; редкие обновления (V4 — апрель 2026); модель открыта (MIT) |
| **Qwen Chat** | Alibaba | КНР | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | Qwen Studio — переключение моделей (Qwen3.6-Plus и др.); встроенная генерация изображений (Qwen Image); **видеопонимание**; голосовой ввод |
| **Kimi** | Moonshot AI | КНР | ✓ | ✓ | ✗ | ✓ | ✗ | ✓ | ✓ | Сверхдлинный контекст (200K+ токенов); **встроенный генератор презентаций (PPT)**; Kimi+ — агенты для специализированных задач |
| **Doubao** | ByteDance | КНР | ✓ | ✓ | ✓ | ✓ | ✓ | ✗ | ✓ | **Голосовой диалог** — естественная речь; AI-персонажи; экосистема Douyin/TikTok |
| **Ernie Bot** | Baidu | КНР | ✓ | ✓ | ✓ | ✓ | ✗ | ✓ | ✓ | Плагины расширения; глубокая интеграция с поиском Baidu; ERNIE 4.5 |
| **Spark** | iFlytek | КНР | ✓ | ✓ | ✗ | ✓ | ✓ | ✗ | ✗ | **Лидер голосовых технологий** — распознавание и синтез речи; отраслевые ассистенты (медицина, право, образование) |
| **YandexGPT** | Яндекс | РФ | ✓ | ✗ | Шедеврум† | ✓ | ✓ | ✓ | ✓ | Интеграция с сервисами Яндекса (почта, карты, музыка); **Яндекс 300** — реферат по ссылке; Алиса Про (голос, по Плюсу); Шедеврум для изображений |
| **GigaChat** | Сбер | РФ | ✓ | ✓ | ✓ Kandinsky | ✓ | Салют† | ✓ | ✗ | **Kandinsky** — генерация изображений прямо в чате; экосистема Сбера (банк, умный дом); бесплатный тариф |

\* Чтение текста из изображений, без генерации. † Отдельный сервис/ассистент, не в веб-интерфейсе чата.

**Примечания:**
- Все китайские чаты работают без VPN в РФ (май 2026). Интерфейс преимущественно на китайском; DeepSeek и Qwen также на английском.
- **DeepSeek** — регистрация по email+паролю (или Google-аккаунт). Самый популярный среди западной аудитории китайский чат. Полностью бесплатный.
- **Qwen Chat** — регистрация по email, интерфейс на английском. Мультимодальность + генерация изображений.
- **Kimi, Doubao, Ernie Bot, Spark** — могут требовать китайский номер телефона для регистрации.
- **YandexGPT** — лучший русскоязычный опыт. Часть функций по подписке Яндекс Плюс (~299 ₽/мес).
- **GigaChat** — базовый тариф бесплатный. Платные тарифы MAX/Pro.

### 1.2. Требуют VPN

| Чат | Вендор | Ключевые модели (май 2026) | Уникальные фичи веб-интерфейса | Плата |
|---|---|---|---|---|
| **ChatGPT** | OpenAI (США) | GPT-5.5, GPT-5, o4-pro, o4-mini | Canvas (интерактивное редактирование текста/кода), DALL-E 3 (изображения), Sora (видео), **GPTs-магазин** кастомных агентов, Deep Research, Code Interpreter, Projects | $20–200/мес, нужна иностранная карта |
| **Claude** | Anthropic (США) | Opus 4.7, Sonnet 4.6, Haiku 4.5 | **Artifacts** — интерактивные мини-приложения прямо в чате; **Cowork** — автономное выполнение задач в десктоп-приложении; Projects; 1M контекст; Skills | $20–200/мес, нужна иностранная карта |
| **Gemini** | Google (США) | Gemini 2.5 Pro/Flash | **Deep Research**; Gems (кастомные ассистенты); Canvas; **глубокая интеграция** с Gmail, Docs, Drive, YouTube, Maps, Calendar; NotebookLM; Veo (видео) | Бесплатно / Advanced $20/мес |
| **Grok** | xAI (США) | Grok 4, Grok 4.1 | Deep/Deeper Search; **Aurora** — генерация изображений; **интеграция с X (Twitter)** — анализ твитов; Big Brain; «Fun Mode» — менее фильтрованные ответы | Требуется X-аккаунт |
| **Perplexity** | Perplexity AI (США) | Sonar / GPT-5.5 / Claude / Grok | **Pro Search** с уточняющими вопросами и полным цитированием; Pages — генератор статей; Spaces; Collections; Focus-режимы (Academic, Writing, Math) | Бесплатно / Pro $20/мес |
| **Mistral** | Mistral AI (Франция) | Mistral Large | Le Chat Agents (настраиваемые); Canvas; Flux (генерация изображений); Code Interpreter | Бесплатно / Pro / Team |

**Для всех:** требуется VPN + иностранная карта для платной подписки (кроме Perplexity Free и Mistral Free).

---

## 2. API-провайдеры

### 2.1. Сводная таблица

| Провайдер | Тип | VPN | Оплата из РФ | Ключевые модели | Способ оплаты |
|---|---|---|---|---|---|
| **DeepSeek** | Вендор | ✗ | Ограничена | V4-Pro (1.6T MoE), V4-Flash | UnionPay / PayPal (не РФ) / посредники |
| **Qwen (Alibaba)** | Вендор | ✗ | Ограничена | Qwen3.6, Qwen3.5, Qwen3-VL | Иностранная карта / бизнес-контракт / посредники |
| **Moonshot/Kimi** | Вендор | ✗ | Ограничена | Kimi-K2.6 (MoE, 256K) | Китайские платёжные системы |
| **OpenRouter** | **Агрегатор** (400+ моделей) | ✗ | ✅ **Крипта!** | GPT-5.5, Claude, Gemini, DeepSeek, Qwen, Kimi, GLM, Llama и др. | **Криптовалюта (USDT/BTC)** — лучший вариант для РФ; также инвойсы |
| **DeepInfra** | Агрегатор (100+ моделей) | ✗ | Ограничена | DeepSeek V4, Kimi K2.6, Qwen, GLM | Иностранная карта |
| **Together AI** | Агрегатор (200+ моделей) | ✗ | Ограничена | DeepSeek, Qwen, Kimi, Llama, Mistral, FLUX | Иностранная карта / Enterprise-инвойс |
| **Groq** | Агрегатор (LPU-чипы) | ✗ | Ограничена | Llama, Qwen, Mistral, DeepSeek (open-source) | Иностранная карта (**есть free tier!**) |
| **Fireworks AI** | Агрегатор | ✗ | Ограничена | DeepSeek V4, Kimi K2.6, Qwen3.6, GLM | Иностранная карта |
| **OpenAI** | Вендор | ✓ | Заблокирована | GPT-5.5, GPT-5, o4-pro | Только иностранная карта + VPN |
| **Anthropic** | Вендор | ✓ | Заблокирована | Claude Opus 4.7, Sonnet 4.6 | Только иностранная карта + VPN |
| **Google AI** | Вендор | ✓ | Заблокирована | Gemini 2.5 Pro/Flash | Только иностранная карта + VPN |
| **YandexGPT** | **Вендор (РФ)** | ✗ | ✅ **Полная** | YandexGPT Pro/Lite/Summarization, YandexART | **Российские карты, Яндекс.Облако, счёт юрлицам** |
| **GigaChat** | **Вендор (РФ)** | ✗ | ✅ **Полная** | GigaChat 2 Max/Pro/Lite, Kandinsky, Embeddings | **Российские карты, Сбер ID, счёт юрлицам** |
| **MTS AI** | **Вендор (РФ)** | ✗ | ✅ **Полная** | MTS AI Chat/Vision | Российские карты |

### 2.2. Ключевые выводы

- **OpenRouter + криптовалюта** — оптимальный способ для россиян получить доступ к 400+ западным моделям без VPN и иностранной карты. Комиссия платформы — 5.5%.
- **DeepSeek API** — доступен напрямую без VPN, модель V4-Pro сравнима с флагманами OpenAI/Anthropic, но оплата через китайские платёжные системы.
- **Groq** — free tier без VPN. Быстрый инференс за счёт собственных LPU-чипов.
- **Российские провайдеры** (YandexGPT, GigaChat, MTS AI) — полная поддержка российских карт, данные в РФ, но качество моделей отстаёт от западных/китайских флагманов.
- **GigaChat** — самый выгодный российский вариант: Freemium с 1M бесплатных токенов.

---

## 3. Инструменты для агентной работы

### 3.1. Open-source

| Инструмент | Интерфейс | Windows | macOS | Linux | Плагины/MCP | Клиент-сервер | Язык | Интеграции | GitHub | Цена |
|---|---|---|---|---|---|---|---|---|---|---|
| **OpenCode** | CLI / Desktop / IDE / Web | ✓ | ✓ | ✓ | MCP, плагины | Мультисессии, headless, Web | TypeScript | 75+ провайдеров, GitHub Copilot, LSP | 150K ★ | Бесплатно |
| **Qwen Code** | CLI / VS Code / JetBrains / Zed | ✓ | ✓ | ✓ | MCP, Skills, SubAgents | Headless (`qwen -p`), SDK | TypeScript | OpenAI-API, Anthropic, локальные (Ollama/vLLM), OpenRouter | 24K ★ | Бесплатно |
| **Cline** | VS Code / CLI | ✓ | ✓ | ✓ | MCP (создание MCP-серверов из чата) | Интегрирован в IDE | TypeScript | OpenRouter, Anthropic, OpenAI, AWS Bedrock, локальные (Ollama/LM Studio) | 61.5K ★ | Бесплатно |
| **Aider** | CLI | ✓ | ✓ | ✓ | Нет | CLI, headless, watch-режим | Python | Claude, DeepSeek, OpenAI, локальные; Git-автокоммиты; голос | 44.5K ★ | Бесплатно |
| **Continue** | VS Code / JetBrains / CLI | ✓ | ✓ | ✓ | MCP, агенты как Markdown-файлы | CLI-проверки в CI/CD | TypeScript | GitHub (статус-чеки на PR), любые LLM | 33K ★ | Бесплатно |
| **Roo Code** | VS Code | ✓ | ✓ | ✓ | MCP, Custom Modes | Интегрирован в IDE | TypeScript | Все основные провайдеры; поддержка русского в интерфейсе | 24K ★ | Бесплатно |
| **LangChain** | Библиотека (Python/TS) | ✓ | ✓ | ✓ | MCP, Deep Agents | LangSmith (платный облачный мониторинг) | Python | Стандартные интерфейсы для LLM, эмбеддингов, векторных БД; LangGraph | 136K ★ | Бесплатно |
| **CrewAI** | Библиотека / CLI | ✓ | ✓ | ✓ | MCP | Crews (автономные) + Flows (event-driven) | Python | Multi-agent оркестрация | 51K ★ | Бесплатно |
| **AutoGPT** | Платформа / CLI / Web | ✓ | ✓ | ✓ | Частично | Self-hosted + Cloud beta | Python | Agent Builder, Marketplace | 184K ★ | Бесплатно |
| **MetaGPT** | CLI | ✓ | ✓ | ✓ | Нет | CLI / HuggingFace Space | Python | Роли PM, архитектора, инженера в одной системе | 68K ★ | Бесплатно |

### 3.2. Проприетарные

| Инструмент | Вендор | Интерфейс | Windows | macOS | Linux | MCP | Клиент-сервер | Особенности | Цена |
|---|---|---|---|---|---|---|---|---|---|
| **Claude Code** | Anthropic (США) | CLI / IDE / Desktop / Web | ✓ | ✓ | ✓ | Да, Skills, Hooks | Headless, Remote Control, GitHub Actions | Автономная работа с кодом и PR; худшая доступность в РФ (нужен и VPN, и иностранная карта) | $20–200/мес |
| **Claude Cowork** | Anthropic (США) | Desktop GUI / Web | ✓ | ✓ | — | Плагины (Google Drive, Docusign) | Десктоп + Web | Автономные задачи для нетехнических пользователей; доступ к файловой системе | В подписке |
| **GitHub Copilot** | Microsoft (США) | VS Code / JetBrains / Xcode / CLI / Web | ✓ | ✓ | ✓ | MCP, Copilot Spaces | Облачные агенты, CLI | Самый распространённый AI-инструмент; Copilot, Claude, Codex — модель на выбор | Free–$39/мес |
| **Cursor** | Anysphere (США) | AI IDE / CLI / Slack | ✓ | ✓ | ✓ | MCP, Rules | IDE + Cloud Agents | Composer 2; Tab-модель сверхточного автодополнения; 50%+ Fortune 500 | Free–$40/мес |
| **Windsurf** | Cognition AI (США) | AI IDE / JetBrains | ✓ | ✓ | ✓ | MCP, Cascade | Cascade (локальный агент) + Devin (облачный) | Первый «agentic IDE»; Agent Command Center — канбан для агентов | Free–$15/мес |
| **Antigravity** | **Google** (США) | Desktop (Electron) | ✓ | ✓ | ✓ | Cloud Code endpoint | Облачный (Google Cloud) | Регионально ограничен; сообщество создало `open-antigravity-patcher` (GPL 3.0) для РФ | Freemium |
| **Cody** | Sourcegraph (США) | VS Code / JetBrains / VS / Web / CLI | ✓ | ✓ | ✓ | MCP | Sourcegraph Enterprise (сервер) | Глубокое понимание кодовой базы через Search API | Freemium |

### 3.3. Российские агентные инструменты

Специализированных российских AI-агентов для работы с кодом по состоянию на май 2026 **не существует**. YandexGPT и GigaChat — LLM общего назначения, не agentic tools. Адаптация open-source решений (Cline, Aider, Qwen Code) с локальными или российскими API-провайдерами — основной путь для разработчиков в РФ.

---

## 4. Инструменты для локального инференса

| Инструмент | Тип | Платформы | Распределённый инференс | API-сервер | Форматы моделей | GPU-бэкенды | Ключевые особенности | Звёзды |
|---|---|---|---|---|---|---|---|---|
| **llama.cpp** | Open-source (C++) | Win, Lin, Mac, iOS, Android, RISC-V, Docker | ✓ Multi-GPU (tensor split) + **Multi-node через RPC** | OpenAI-совместимый (`llama-server`); embedding, reranking, параллельный декодинг | GGUF (конвертация из HF через `convert_hf_to_gguf.py`) | CUDA, Metal, Vulkan, SYCL, HIP (AMD), MUSA, CANN, OpenCL, ZenDNN, WebGPU | 200+ архитектур; квантование 1.5–8 бит; **чистый C++ без зависимостей**; CPU+GPU гибрид | 109K |
| **Ollama** | Проприетарная обёртка | Win, Lin, Mac (Apple Silicon) | ✗ | OpenAI-совместимый; собственный API + Ollama Cloud | GGUF (llama.cpp под капотом) | CUDA, Metal | **Простейшая установка**: `curl ... | sh`; собственный реестр моделей; `ollama run llama3`; платный облачный уровень Pro/Max | 109K |
| **vLLM** | Open-source (Python) | Linux (основная); NVIDIA/AMD/Intel/TPU/Ascend | ✓ Tensor/Pipeline/Data/Expert/Context parallelism; **Multi-node** | OpenAI-совместимый + Anthropic Messages API + gRPC | HF (PyTorch), GGUF, GPTQ/AWQ, FP8, INT4/8, NVFP4 | CUDA, ROCm, Intel Gaudi, Google TPU, Huawei Ascend, Apple Silicon | PagedAttention; 200+ архитектур; continuous batching; максимальная пропускная способность; `pip install vllm` | 79.3K |
| **LM Studio** | Проприетарное (GUI) | Win, Lin, Mac (Apple Silicon) | LM Link — удалённые инстансы (апрель 2026) | OpenAI-совместимый; JS/Python SDK; MCP-клиент; headless (`llmster`) | GGUF, MLX (Apple) | CUDA, Metal, Vulkan | **Десктопный GUI**; встроенный каталог моделей; самый простой старт для начинающих | — |
| **GPT4All** | Open-source (C++/Python) | Win, Lin, Mac | ✗ | Docker-based, OpenAI-совместимый; Python API (`gpt4all`); интеграция с LangChain | GGUF (llama.cpp) | Vulkan (NVIDIA + AMD) | LocalDocs — приватный чат с документами; Python API: `from gpt4all import GPT4All` | 77.4K |
| **TextGen (oobabooga)** | Open-source (Python) | Win, Lin, Mac (портабельные сборки) | ✓ Multi-GPU (tensor split + tensor parallelism) | OpenAI-совместимый + Anthropic-совместимый; MCP-сервер | GGUF, Transformers, ExLlamaV3, TensorRT-LLM | CUDA, Vulkan, ROCm | **Веб-интерфейс (Gradio)**; multimodal (vision); LoRA-тренировка; генерация изображений; TTS; 100% оффлайн | 47K |
| **KoboldCpp** | Open-source (C++) | Win, Lin, Mac, **Android (Termux)**, RPi, Docker | Multi-GPU (Vulkan/CUDA) | Множественные endpoints (Kobold, OpenAI, Ollama, Whisper, TTS) | GGUF + GGML | CUDA, Vulkan | **Один исполняемый файл**; LLM + Image Gen + Video Gen + STT + TTS + Music Gen; KoboldAI Lite UI для ролевых игр | 10.4K |
| **ExLlamaV2** | Open-source (Python/C++) | Win, Lin (только NVIDIA) | Multi-GPU через `--gpu_split` | TabbyAPI (OpenAI-совместимый), ExUI | GPTQ, EXL2 (2–8 бит, смешанное квантование) | CUDA (только NVIDIA) | Экстремально быстрый: 257 t/s на 4090; speculative decoding; заархивирован в пользу ExLlamaV3 | 4.5K |
| **MLX** | Open-source (Apple) | Mac (Apple Silicon), Linux | Multi-device (CPU+GPU unified memory) | Python API (`mlx-lm`); finetuning (LoRA) | MLX, HF-конвертация, GGUF | Apple Silicon GPU (Metal) | **Разработан Apple**; NumPy-подобный Python API; lazy computation; autograd | 26K |
| **llama.rn** | Open-source | **iOS (Metal), Android (OpenCL/NPU)** | ✗ (мобильные устройства) | React Native binding для llama.cpp | GGUF | Metal, OpenCL, Hexagon NPU | Нативный мобильный инференс; multimodal; tool calling | 931 |

### 4.1. Российские инструменты для локального инференса

**Отсутствуют** как класс. Российские модели (GigaChat, Kandinsky) запускаются через стандартные международные инструменты (llama.cpp, vLLM). Из российских наработок:
- **GGUF-квантизации GigaChat 3.1** — опубликованы ai-sage на Hugging Face. Загружаются и запускаются через llama.cpp / Ollama как обычные GGUF.
- **GPT2Giga** (ai-forever) — FastAPI-прокси, подменяющий вызовы на GigaChat API, эмулирует OpenAI-совместимый endpoint.
- **GigaChain** — адаптер для LangChain под GigaChat API.

---

## 5. Репозитории открытых моделей

### 5.1. Доступные без VPN

| Репозиторий | Назначение | Примечание |
|---|---|---|
| **Hugging Face** (huggingface.co) | Основной мировой репозиторий — 2M+ моделей | ✅ Доступен из РФ (май 2026). Некоторые аккаунты РФ-организаций (sberbank-ai) удалены, но сайт открыт. |
| **GitHub** (github.com) | Хостинг кода, Git LFS для моделей, релизы | ✅ Доступен. |
| **ModelScope** (modelscope.cn) | Китайский аналог HF от Alibaba. Китайские модели (Qwen, DeepSeek, GLM, Yi и др.) | ✅ Доступен. Некоторые модели эксклюзивно на ModelScope. |
| **Ollama Library** (ollama.com/library) | Встроенный реестр моделей Ollama | ✅ Доступен. |
| **CivitAI** (civitai.com) | Репозиторий моделей для генерации изображений (SD, Flux) | ✅ Доступен. |

### 5.2. С VPN

- Hugging Face — формально доступен, но скачивание больших файлов с `cdn-lfs.huggingface.co` может работать нестабильно без VPN.
- Некоторые HF Spaces геоблокированы владельцами.

### 5.3. Российские открытые модели и их размещение

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

## 6. Итоговые рекомендации

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

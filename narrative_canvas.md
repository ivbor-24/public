---
layout: default
title: LLM в России — дорожная карта
---

# LLM в России: дорожная карта пользователя (май 2026)

---

### Во первых строках

Май 2026. Большие языковые модели перестали быть диковинкой. И даже на ЛОРе под аккомпанимент из ворчания "старичков" появился раздел про ИИшечку. Правда, выясняется, что далеко не все даже в технарском сообществе знают, что собой предтавляет современный ландшафт ЛЛМок: что они умеют, как их применяют, зачем они вообще нужны. 

Серьезно усложняет погружение в актуальный контекст (в человеческом смысле слова) уникальный "русский путь": блокировки со стороны западных разработциков и провайдеров, блокировки от родного РКН и (с недавних пор) ФСБ. Отсюда следуют: платёжные ограничения, обилие китайских альтернатив, собственные разработки Яндекса и Сбера как бенчмарк и пример LLM ( последний пункт - это очень, очень плохо). 

Поэтому в недрах моей черепной коропки и на серверах Shēndù Qiúsuǒ (в большей степени) родился следующий текст. Он о том, как большинство пользователей знакомится с БЯМами, какие этапы в работе с модельками проходит, и какие есть варианты выбора в море способов взаимодействия с очень Искусственным не очень Интеллектом.

Текст большой, поэтому вот оглавление:
1. [Первое касание: веб-чаты](#%D0%BF%D0%B5%D1%80%D0%B2%D0%BE%D0%B5-%D0%BA%D0%B0%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B2%D0%B5%D0%B1-%D1%87%D0%B0%D1%82%D1%8B)
2. [Коготок (claw) застрял - всей птичке пропасть: связка Агент + API](#%D0%BA%D0%BE%D0%B3%D0%BE%D1%82%D0%BE%D0%BA-claw-%D0%B7%D0%B0%D1%81%D1%82%D1%80%D1%8F%D0%BB---%D0%B2%D1%81%D0%B5%D0%B9-%D0%BF%D1%82%D0%B8%D1%87%D0%BA%D0%B5-%D0%BF%D1%80%D0%BE%D0%BF%D0%B0%D1%81%D1%82%D1%8C-%D1%81%D0%B2%D1%8F%D0%B7%D0%BA%D0%B0-%D0%B0%D0%B3%D0%B5%D0%BD%D1%82--api)
    * [Поставщики «мозгов» бывают двух сортов](#%D0%BF%D0%BE%D1%81%D1%82%D0%B0%D0%B2%D1%89%D0%B8%D0%BA%D0%B8-%D0%BC%D0%BE%D0%B7%D0%B3%D0%BE%D0%B2-%D0%B1%D1%8B%D0%B2%D0%B0%D1%8E%D1%82-%D0%B4%D0%B2%D1%83%D1%85-%D1%81%D0%BE%D1%80%D1%82%D0%BE%D0%B2)
    * [Агенты: open-source, проприетарные и общего назначения](#%D0%B0%D0%B3%D0%B5%D0%BD%D1%82%D1%8B-open-source-%D0%B8-%D0%BF%D1%80%D0%BE%D0%BF%D1%80%D0%B8%D0%B5%D1%82%D0%B0%D1%80%D0%BD%D1%8B%D0%B5)
3. [А внутри у ней - нейронка: плагин, память и контекст](#%D0%B0-%D0%B2%D0%BD%D1%83%D1%82%D1%80%D0%B8-%D1%83-%D0%BD%D0%B5%D0%B9---%D0%BD%D0%B5%D0%B9%D1%80%D0%BE%D0%BD%D0%BA%D0%B0-%D0%BF%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD-%D0%BF%D0%B0%D0%BC%D1%8F%D1%82%D1%8C-%D0%B8-%D0%BA%D0%BE%D0%BD%D1%82%D0%B5%D0%BA%D1%81%D1%82)
    * [Рынок плагинов и MCP-серверы](#%D1%80%D1%8B%D0%BD%D0%BE%D0%BA-%D0%BF%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D0%BE%D0%B2-%D0%B8-mcp-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D1%8B)
    * [Скиллы (Skills)](#%D1%81%D0%BA%D0%B8%D0%BB%D0%BB%D1%8B-skills)
    * [Контекст-файлы](#%D0%BA%D0%BE%D0%BD%D1%82%D0%B5%D0%BA%D1%81%D1%82-%D1%84%D0%B0%D0%B9%D0%BB%D1%8B)
    * [Память агента](#%D0%BF%D0%B0%D0%BC%D1%8F%D1%82%D1%8C-%D0%B0%D0%B3%D0%B5%D0%BD%D1%82%D0%B0)
    * [Векторные базы как фундамент памяти](#%D0%B2%D0%B5%D0%BA%D1%82%D0%BE%D1%80%D0%BD%D1%8B%D0%B5-%D0%B1%D0%B0%D0%B7%D1%8B-%D0%BA%D0%B0%D0%BA-%D1%84%D1%83%D0%BD%D0%B4%D0%B0%D0%BC%D0%B5%D0%BD%D1%82-%D0%BF%D0%B0%D0%BC%D1%8F%D1%82%D0%B8)
4. [Полный суверенитет и абсолютное погружение: локальный инференс](#%D0%BF%D0%BE%D0%BB%D0%BD%D1%8B%D0%B9-%D1%81%D1%83%D0%B2%D0%B5%D1%80%D0%B5%D0%BD%D0%B8%D1%82%D0%B5%D1%82-%D0%B8-%D0%B0%D0%B1%D1%81%D0%BE%D0%BB%D1%8E%D1%82%D0%BD%D0%BE%D0%B5-%D0%BF%D0%BE%D0%B3%D1%80%D1%83%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B9-%D0%B8%D0%BD%D1%84%D0%B5%D1%80%D0%B5%D0%BD%D1%81)
    * [Репозитории моделей](#%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B8-%D0%BC%D0%BE%D0%B4%D0%B5%D0%BB%D0%B5%D0%B9)
    * [Инструменты запуска](#%D0%B8%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D1%8B-%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA%D0%B0)
5. [Напоследок](#%D0%BD%D0%B0%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%D0%B4%D0%BE%D0%BA)

Двигаемся по уровням погружения.

---

### Первое касание: веб-чаты

Вы только знакомитесь с LLM. У вас нет ни API-ключа, ни желания разбираться с токенами и эндпоинтами. Нужна вкладка в браузере, куда можно написать вопрос и получить ответ. Благо, в 2026 году вариантов — море. Начнём с того, что доступно прямо здесь и сейчас, без обмазывания проксями и ВПНами, бесплатно, иногда с СМС.

[<strong>DeepSeek</strong>](https://chat.deepseek.com/) — главный хит среди китайских чатов. Регистрация по email, с апреля - модель V4-Pro с контекстным окном в миллион токенов. Работает только с текстом и файлами, генерации изображений нет. Бесплатно.

[<strong>Qwen Chat</strong>](https://chat.qwen.ai/) от Alibaba — если хочется мультимодальности. Генерация изображений? Встроена. Видеопонимание? Пожалуйста. Голосовой ввод? Есть. Qwen Studio позволяет переключаться между разными версиями моделей. Есть мостик к тем самым кодинг-агентам (о них позже) - кодинг-режим прямо из веб-интерфейса. С возможность подключения своего git-репо, с работой в git-образном окошке.

[<strong>Kimi</strong>](https://www.kimi.com/) от Moonshot AI навалил массу фич прямо в веб интерфейс. Тут и кодинг-окошко, и конструктор сайтов. И даже мечта офисного работника - автогенерация презенташек. Загрузил документ — получил готовый PPT.

[<strong>Doubao</strong>](https://www.dola.com/chat/) (ByteDance) делает ставку на голосовой диалог — естественную речь, AI-персонажей, экосистему TikTok. Можно делать картинки, переводить тексть, выполнять домашку. Модно, молодежно, для неразвлекательных целей - малоприменимо.

[<strong>Ernie Bot</strong>](https://ernie.baidu.com/) (Baidu) и [<strong>Spark</strong>](https://www.iflytek.com/en/products/ai/spark-ai.html) (iFlytek) — ещё два китайских товарища. Ernie щеголяет плагинами и интеграцией с поиском Baidu, Spark — лучшими в Китае голосовыми технологиями и мультяшными цифровыми аватарками. Для российского пользователя - не особо полезно.

[<strong>z.ai</strong>](https://z.ai/) — Хороший базовый набор в веб-чате: генерация текстов, слайдов, таблиц, дашбордов, кода. Из России работает нестабильно, могут не работать некоторые функции. Годится в качестве тест-режима модельки GLM-5.1 перед покупкой API-ключа.

[<strong>MiniMax</strong>](https://agent.minimax.io/) — Комбайн в вебе: тут и "агенты", и "скиллы", и создание артефактов от табличек до видео. Фишка - режим "Эксперты": режим диалога с моделью системными промптами и MCP заточенной под конкретные задачи. Раньше много было бесплатно, теперь эти функции - в месячном "триале" перед базовой подпиской.

[<strong>StepFun / 阶跃AI</strong>](https://www.stepfun.com/) — Дипсик на минималках. Примечателен бешеным количеством рекламы: продвигают свой форк OpenClaw и API-подписку к нему.

Все эти чаты доступны из России без VPN. Минус: часть требует китайский номер для регистрации.

<details>
<summary> Таблица 1.1 Чат-боты, доступные без VPN </summary>

<table>
<thead>
<tr>
<th>Чат</th>
<th>Вендор</th>
<th>Страна</th>
<th>Текст</th>
<th>Изобр.</th>
<th>Ген. изобр.</th>
<th>Файлы</th>
<th>Голос</th>
<th>Код</th>
<th>Поиск</th>
<th>Уникальные фичи веб-интерфейса</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>DeepSeek Chat</strong></td>
<td>DeepSeek</td>
<td>КНР</td>
<td>✓</td>
<td>✓*</td>
<td>✗</td>
<td>✓</td>
<td>✗</td>
<td>✓</td>
<td>✓</td>
<td>V4-Pro с 1M токенов контекста; редкие обновления (V4 — апрель 2026); модель открыта (MIT)</td>
</tr>
<tr>
<td><strong>Qwen Chat</strong></td>
<td>Alibaba</td>
<td>КНР</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>Qwen Studio — переключение моделей (Qwen3.6-Plus и др.); встроенная генерация изображений (Qwen Image); <strong>видеопонимание</strong>; голосовой ввод; кодинг-режим с возможностью подключения репозитория</td>
</tr>
<tr>
<td><strong>Kimi</strong></td>
<td>Moonshot AI</td>
<td>КНР</td>
<td>✓</td>
<td>✓</td>
<td>✗</td>
<td>✓</td>
<td>✗</td>
<td>✓</td>
<td>✓</td>
<td>Сверхдлинный контекст (200K+ токенов); <strong>встроенный генератор презентаций (PPT)</strong>; Kimi+ — агенты для специализированных задач; кодинг-режим</td>
</tr>
<tr>
<td><strong>Doubao</strong></td>
<td>ByteDance</td>
<td>КНР</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✗</td>
<td>✓</td>
<td><strong>Голосовой диалог</strong> — естественная речь; AI-персонажи; экосистема Douyin/TikTok</td>
</tr>
<tr>
<td><strong>Ernie Bot</strong></td>
<td>Baidu</td>
<td>КНР</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✗</td>
<td>✓</td>
<td>✓</td>
<td>Плагины расширения; глубокая интеграция с поиском Baidu; ERNIE 4.5</td>
</tr>
<tr>
<td><strong>Spark</strong></td>
<td>iFlytek</td>
<td>КНР</td>
<td>✓</td>
<td>✓</td>
<td>✗</td>
<td>✓</td>
<td>✓</td>
<td>✗</td>
<td>✗</td>
<td><strong>Лидер голосовых технологий</strong> — распознавание и синтез речи; отраслевые ассистенты (медицина, право, образование)</td>
</tr>
<tr>
<td><strong>YandexGPT</strong></td>
<td>Яндекс</td>
<td>РФ</td>
<td>✓</td>
<td>✗</td>
<td>Шедеврум†</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>Интеграция с сервисами Яндекса (почта, карты, музыка); <strong>Яндекс 300</strong> — реферат лонгрида, подкаста или длинного видео по ссылке; Алиса Про (голос, по Плюсу); Шедеврум для изображений</td>
</tr>
<tr>
<td><strong>GigaChat</strong></td>
<td>Сбер</td>
<td>РФ</td>
<td>✓</td>
<td>✓</td>
<td>✓ Kandinsky</td>
<td>✓</td>
<td>Салют†</td>
<td>✓</td>
<td>✗</td>
<td><strong>Kandinsky</strong> — генерация изображений прямо в чате; экосистема Сбера (банк, умный дом); бесплатный тариф</td>
</tr>
<tr>
<td><strong>z.ai</strong></td>
<td>Zhipu AI</td>
<td>КНР</td>
<td>✓</td>
<td>✓</td>
<td>✓ GLM-Image</td>
<td>✓</td>
<td>✗</td>
<td>✓</td>
<td>✓</td>
<td>GLM-5.1 (уровень флагманов); Agent mode с генерацией .docx/.pdf/.xlsx; 200K контекст; бесплатно</td>
</tr>
<tr>
<td><strong>MiniMax</strong></td>
<td>MiniMax</td>
<td>КНР</td>
<td>✓</td>
<td>✓</td>
<td>✗</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MiniMax-M1 — 1M контекст, open-weight; голосовой ввод/вывод; Agent mode; бесплатно без регистрации (ограниченный режим)</td>
</tr>
<tr>
<td><strong>StepFun / 阶跃AI</strong></td>
<td>StepFun</td>
<td>КНР</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>Step-3.5-Flash; генерация видео; мультимодальность; бесплатно</td>
</tr>
</tbody>
</table>

</details>

<strong>Российские решения</strong> — варианта два и оба так себе: [<strong>YandexGPT</strong>](https://alice.yandex.ru/) aka <strong>AlisaAI</strong> и [<strong>GigaChat</strong>](https://giga.chat/). Отстают от флагманов западного моделестроения очень сильно. Для серьезной работы (по крайней мере, с текстами, картинками и видео) - почти не пригодны. Но плюcы, конечно есть. Русский язык для них родной. YandexGPT встроен в поиск Яндекса, в Алису, в сервис [<strong>«Яндекс 300»</strong>](https://300.ya.ru/) (гусары,молчать!) - краткий пересказ статей, подкастов и видео. GigaChat от Сбера умеет генерировать изображения (Kandinsky) прямо в чате. Оба работают без VPN, Яндекс еще и доступен при режиме "белых списков" (почти всегда), принимают российские карты для премиум-функций.

А теперь — веб-чаты, которые без VPN <strong>не открываются</strong>: [ChatGPT](https://chatgpt.com/), [<strong>Claude</strong>](https://claude.ai/), [<strong>Gemini</strong>](https://gemini.google.com/app), [<strong>Grok</strong>](https://grok.com/), [<strong>Perplexity</strong>](https://www.perplexity.ai/), [<strong>Mistral</strong>](https://mistral.ai/), [<strong>Microsoft Copilot</strong>](https://copilot.microsoft.com/), запрещенная и экстремистская [<strong>Meta AI</strong>](https://www.meta.ai/). Это западные флагманы. У каждого — арсенал уникальных фич: Artifacts у Claude, Canvas и GPTs у ChatGPT, Perplexity с полным цитированием источников. Есть все, что и у web-реализаций из Поднебесной и с горкой. Но дверь заперта. Нужны VPN и, для платных подписок, иностранная карта. Досадно, но ладно.

<details>
<summary> Таблица 1.2 Чат-боты, доступные с VPN </summary>

<table>
<thead>
<tr>
<th>Чат</th>
<th>Вендор</th>
<th>Ключевые модели (май 2026)</th>
<th>Уникальные фичи веб-интерфейса</th>
<th>Плата</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>ChatGPT</strong></td>
<td>OpenAI (США)</td>
<td>GPT-5.5, GPT-5.4</td>
<td>Canvas (интерактивное редактирование текста/кода), DALL-E 3 (изображения), Sora (видео), <strong>GPT-магазин</strong> кастомных агентов, Deep Research, Code Interpreter, Projects</td>
<td>$20–200/мес, нужна иностранная карта</td>
</tr>
<tr>
<td><strong>Claude</strong></td>
<td>Anthropic (США)</td>
<td>Opus 4.7, Sonnet 4.6, Haiku 4.5</td>
<td><strong>Artifacts</strong> — интерактивные мини-приложения прямо в чате; <strong>Cowork</strong> — автономное выполнение задач в десктоп-приложении; Projects; 1M контекст; Skills</td>
<td>$20–200/мес, нужна иностранная карта</td>
</tr>
<tr>
<td><strong>Gemini</strong></td>
<td>Google (США)</td>
<td>Gemini 2.5 Pro/Flash</td>
<td><strong>Deep Research</strong>; Gems (кастомные ассистенты); Canvas; <strong>глубокая интеграция</strong> с Gmail, Docs, Drive, YouTube, Maps, Calendar; NotebookLM; Veo (видео)</td>
<td>Бесплатно / Advanced $20/мес</td>
</tr>
<tr>
<td><strong>Grok</strong></td>
<td>xAI (США)</td>
<td>Grok 4, Grok 4.1</td>
<td>Deep/Deeper Search; <strong>Aurora</strong> — генерация изображений; <strong>интеграция с X (Twitter)</strong> — анализ твитов; Big Brain; «Fun Mode» — менее фильтрованные ответы</td>
<td>Требуется X-аккаунт</td>
</tr>
<tr>
<td><strong>Perplexity</strong></td>
<td>Perplexity AI (США)</td>
<td>Sonar / GPT-5.5 / Claude / Grok</td>
<td><strong>Pro Search</strong> с уточняющими вопросами и полным цитированием; Pages — генератор статей; Spaces; Collections; Focus-режимы (Academic, Writing, Math)</td>
<td>Бесплатно / Pro $20/мес</td>
</tr>
<tr>
<td><strong>Mistral</strong></td>
<td>Mistral AI (Франция)</td>
<td>Mistral Large</td>
<td>Le Chat Agents (настраиваемые); Canvas; Flux (генерация изображений); Code Interpreter</td>
<td>Бесплатно / Pro / Team</td>
</tr>
<tr>
<td><strong>Microsoft Copilot</strong></td>
<td>Microsoft (США)</td>
<td>GPT-4.1/4.5</td>
<td>DALL-E 3, Deep Research, Pages, интеграция с M365/Edge/Windows</td>
<td>Бесплатно / Pro $20/мес</td>
</tr>
<tr>
<td><strong>Meta AI</strong></td>
<td>Meta (запрещенная+экстремистская)</td>
<td>Llama 4</td>
<td>Интеграция с WhatsApp/Instagram/Facebook; Imagine (генерация изображений); голосовой режим</td>
<td>Бесплатно</td>
</tr>
</tbody>
</table>

</details>

---

### Коготок (claw) застрял - всей птичке пропасть: связка Агент + API

Вы распробовали чаты. Теперь хочется большего: чтобы нейросеть работала с кодом, файловой системой, терминалом. Чтобы сама коммитила в Git, открывала PR, запускала тесты. Сделала rm -rf /*, наконец. Для этого нужны две вещи: <strong>агент</strong>(к агентности в философском или daemon смысле не имеет никакого отношения, просто так повелось называть) - это софт, который оркестрирует взаимодействие и предоставляет инструметы расширяюшие или ограничивающие работу модели и <strong>API-провайдер</strong> - тот, кто поставляет доступ к самой LLM, развернутой на серверах китайских товарищей или буржуйских супостатов.

#### Поставщики «мозгов» бывают двух сортов

<strong>Вендоры</strong> — разработчики моделей: [<strong>OpenAI</strong>](https://openai.com/api/), [<strong>Anthropic</strong>](https://platform.claude.com/docs/en/api/overview), [<strong>Google</strong>](https://aistudio.google.com/app/api-keys) (<em>бесплатные flash-модели по API!!!</em>), [<strong>DeepSeek</strong>](https://platform.deepseek.com/), [<strong>Alibaba (Qwen)</strong>](https://modelstudio.console.alibabacloud.com/), [<strong>Z.ai API</strong>](https://docs.z.ai/), [<strong>MiMo (Xiaomi)</strong>](https://platform.xiaomimimo.com/). У них прямой доступ к собственным моделям.
<strong>Агрегаторы</strong> — посредники, собирающие модели от разных вендоров под одной крышей: [<strong>OpenRouter</strong>](https://openrouter.ai/) <em>есть бесплатный план</em>, [<strong>DeepInfra</strong>](https://deepinfra.com/deepstart), [<strong>Together AI</strong>](https://docs.together.ai/docs/api-keys-authentication), [<strong>Groq</strong>](https://console.groq.com/keys) <em>есть бесплатный план</em>, [<strong>Fireworks AI</strong>](https://docs.fireworks.ai/api-reference/introduction), [<strong>OpenCode (Zen/Go)</strong>](https://opencode.ai/) <em>есть бесплатный план</em>, [<strong>Cerebras</strong>](https://cloud.cerebras.ai/) <em>есть бесплатный план</em>. Список можно продолжать и продолжать, заканчивая помойками-однодневками от успешных васянов с ветхими стойками в древних ЦОДах. Отмечу, многие из агрегаторов не только продают доступ к общим инференс-инстансам, для солидных господ есть предложения о покупке отдельного инстанса или, натурально, выделенного вычислительного кластера для рассупонивания модельки.


<details>
<summary> Таблица 2.1 Провайдеры API. Сводная </summary>

<table>
<thead>
<tr>
<th>Провайдер</th>
<th>Тип</th>
<th>VPN</th>
<th>Оплата из РФ</th>
<th>Ключевые модели</th>
<th>Способ оплаты</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>DeepSeek</strong></td>
<td>Вендор</td>
<td>✗</td>
<td>Ограничена</td>
<td>V4-Pro (1.6T MoE), V4-Flash</td>
<td>UnionPay / PayPal (не РФ) / посредники</td>
</tr>
<tr>
<td><strong>Qwen (Alibaba)</strong></td>
<td>Вендор</td>
<td>✗</td>
<td>Ограничена</td>
<td>Qwen3.6, Qwen3.5, Qwen3-VL</td>
<td>Иностранная карта / бизнес-контракт / посредники</td>
</tr>
<tr>
<td><strong>Moonshot/Kimi</strong></td>
<td>Вендор</td>
<td>✗</td>
<td>Ограничена</td>
<td>Kimi-K2.6 (MoE, 256K)</td>
<td>Китайские платёжные системы</td>
</tr>
<tr>
<td><strong>Z.ai</strong></td>
<td>Вендор</td>
<td>✗</td>
<td>Ограничена</td>
<td>GLM-5.1, GLM-5, GLM-5-Turbo, GLM-4.7</td>
<td>Иностранная карта / посредники (<strong>есть free tier!</strong>)</td>
</tr>
<tr>
<td><strong>Nvidia</strong></td>
<td><strong>Вендор</strong> (Nemotron + хостинг через NIM)</td>
<td>✗</td>
<td>Ограничена</td>
<td>Nemotron 3 Nano Omni 30B-A3B (reasoning), DeepSeek V4 Pro, GLM-5.1, Gemma 4, Llama (затюненные варианты)</td>
<td>Иностранная карта (<strong>есть free tier!</strong>)</td>
</tr>
<tr>
<td><strong>OpenRouter</strong></td>
<td><strong>Агрегатор</strong> (400+ моделей)</td>
<td>✗</td>
<td>✅ <strong>Крипта</strong></td>
<td>GPT-5.5, Claude, Gemini, DeepSeek, Qwen, Kimi, GLM, Llama и др.</td>
<td><strong>Криптовалюта (USDT/BTC)</strong> — главное не светить свою страну( некоторые пользователи сообщают о блокировках)</td>
</tr>
<tr>
<td><strong>DeepInfra</strong></td>
<td>Агрегатор (100+ моделей)</td>
<td>✗</td>
<td>Ограничена</td>
<td>DeepSeek V4, Kimi K2.6, Qwen, GLM</td>
<td>Иностранная карта</td>
</tr>
<tr>
<td><strong>Together AI</strong></td>
<td>Агрегатор (200+ моделей)</td>
<td>✗</td>
<td>Ограничена</td>
<td>DeepSeek, Qwen, Kimi, Llama, Mistral, FLUX</td>
<td>Иностранная карта / Enterprise-инвойс</td>
</tr>
<tr>
<td><strong>Groq</strong></td>
<td>Агрегатор (LPU-чипы)</td>
<td>✗</td>
<td>Ограничена</td>
<td>Llama, Qwen, Mistral, DeepSeek (open-source)</td>
<td>Иностранная карта (<strong>есть free tier!</strong>)</td>
</tr>
<tr>
<td><strong>Cerebras</strong></td>
<td>Агрегатор (CS-3 wafer-scale чипы)</td>
<td>✗</td>
<td>Ограничена</td>
<td>GPT-OSS-120B, Llama 4 Scout/Maverick, Llama 3.3-70B, Qwen 3-235B (Thinking), GLM-4.7</td>
<td>Иностранная карта (<strong>есть free tier!</strong>) — до 3 000 токенов/с</td>
</tr>
<tr>
<td><strong>OpenCode</strong></td>
<td><strong>Агрегатор</strong> (12+ моделей, агентно-оптимизированные)</td>
<td>✗</td>
<td>Ограничена</td>
<td>DeepSeek V4 Pro/Flash, Qwen3.6 Plus, Qwen3.5 Plus, Kimi K2.6, GLM-5.1, MiniMax M2.7, MiMo-V2.5-Pro</td>
<td><strong>Zen</strong>: pay-as-you-go ($20 пополнение, нулевая наценка, карта). <strong>Go</strong>: подписка $10/мес ($5 первый месяц)</td>
</tr>
<tr>
<td><strong>Fireworks AI</strong></td>
<td>Агрегатор</td>
<td>✗</td>
<td>Ограничена</td>
<td>DeepSeek V4, Kimi K2.6, Qwen3.6, GLM</td>
<td>Иностранная карта</td>
</tr>
<tr>
<td><strong>OpenAI</strong></td>
<td>Вендор</td>
<td>✓</td>
<td>Заблокирована</td>
<td>GPT-5.5, GPT-5, o4-pro</td>
<td>Только иностранная карта + VPN</td>
</tr>
<tr>
<td><strong>Anthropic</strong></td>
<td>Вендор</td>
<td>✓</td>
<td>Заблокирована</td>
<td>Claude Opus 4.7, Sonnet 4.6</td>
<td>Только иностранная карта + VPN</td>
</tr>
<tr>
<td><strong>Google AI</strong></td>
<td>Вендор</td>
<td>✓</td>
<td>Заблокирована</td>
<td>Gemini 2.5 Pro/Flash</td>
<td>Только иностранная карта + VPN</td>
</tr>
<tr>
<td><strong>YandexGPT</strong></td>
<td><strong>Вендор (РФ)</strong></td>
<td>✗</td>
<td>✅ <strong>Полная</strong></td>
<td>YandexGPT Pro/Lite/Summarization, YandexART</td>
<td><strong>Российские карты, Яндекс.Облако, счёт юрлицам</strong></td>
</tr>
<tr>
<td><strong>GigaChat</strong></td>
<td><strong>Вендор (РФ)</strong></td>
<td>✗</td>
<td>✅ <strong>Полная</strong></td>
<td>GigaChat 2 Max/Pro/Lite, Kandinsky, Embeddings</td>
<td><strong>Российские карты, Сбер ID, счёт юрлицам</strong></td>
</tr>
<tr>
<td><strong>MTS AI</strong></td>
<td><strong>Вендор (РФ)</strong></td>
<td>✗</td>
<td>✅ <strong>Полная</strong></td>
<td>MTS AI Chat/Vision</td>
<td>Российские карты</td>
</tr>
</tbody>
</table>

</details>

Отдельного упоминания стоит <strong>[nVidia](https://build.nvidia.com/nvidia)</strong> - эти ребята производят не только лучшие GPU и NPU на сегодняшний день, они еще и файн-тюнят открытые модельки, предоставляют API и держат репозиторий открытых моделей (что это и зачем - дальше по тексту). Почти все провайдеры требуют иностранную карту. Но есть обходные пути: оформление иностранных карт, посредники с разнообразных платежных сервисов (тысячи их), старая добрая крипта.

Российские вендоры [<strong>YandexGPT</strong>](https://aistudio.yandex.ru/ru/model-gallery) и [<strong>GigaChat</strong>](https://developers.sber.ru/portal/products/gigachat-api) тоже предоставляют доступ к моделькам через API. Полная поддержка российских карт, данные на серверах в РФ. GigaChat даёт 1M токенов бесплатно при регистрации. Кто-то пользуется.

#### Агенты: open-source и проприетарные

Агент — это программа, которая превращает LLM из собеседника в деятеля. Агент читает код, пишет файлы, запускает команды, ищет в интернете, подключается к базам данных. Его принято ставить в Doker'ы, на виртуалки, на отдельные ПК (все любят MAC mini). На самом деле, если вы не кулхацкер, то для задач регулярной генерации текстов, создания скриптов для локальных автоматизаций, кодинга своего уютного сайтика - вполне можно разворачивать локально на машинке в юзер-директории (большинство агентов сами вам напомнят, что надо высовывать в сеть, а что нет, и в каких случаях). Так или иначе, все инструменты из нашего обзора делятся на три лагеря:

<strong>Open-source агенты:</strong>

[<strong>OpenCode</strong>](https://github.com/anomalyco/opencode) (150K ★) — CLI/Desktop/IDE/Web. TypeScript. Поддерживает 75+ провайдеров, включая локальные модели. Может работать в headless-режиме. Кроссплатформенный. Универсальный.
[<strong>Cline</strong>](https://github.com/cline/cline) (61.5K ★) — расширение VS Code. MCP из коробки, умеет генерировать MCP-серверы прямо из чата. Подтверждение каждого действия (human-in-the-loop).
[<strong>Kilocode</strong>](https://github.com/Kilo-Org/kilocode) (19K ★) — позиционируется как "инженерная платформа", кроссплатформенный, расширенный функции автоматизации/ выполнения циклических задач.
[<strong>Aider</strong>](https://github.com/Aider-AI/aider) (44.5K ★) — CLI, Python. Фишка: Repomap — карта репозитория для навигации модели.
[<strong>Qwen Code</strong>](https://github.com/QwenLM/qwen-code) (24K ★) — CLI от Alibaba. Заточен под семейство Qwen, но работает с любыми моделями. Поддержка Skills и SubAgents.
[<strong>Roo Code</strong>](https://github.com/RooCodeInc/Roo-Code) (24K ★) — форк Cline с фокусом на кастомизацию режимов. Поддерживает русский язык в интерфейсе.
<strong>[LangChain](https://github.com/langchain-ai/langchain), [CrewAI](https://github.com/crewAIInc/crewAI), [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT), [MetaGPT](https://github.com/FoundationAgents/MetaGPT), [Qwen Agent](https://github.com/QwenLM/Qwen-Agent)</strong> — фреймворки для построения собственных агентных систем. От библиотек до платформ с marketplace.
[<strong>Pi-agent</strong>](https://github.com/earendil-works/pi) (45.8K ★) — минималистичный terminal-based harness от Mario Zechner. Философия: «адаптируй pi под себя, а не наоборот». Собственный TUI-движок. Не поддерживает MCP принципиально — всё необходимое строится через extensions. По сути — эталонный каркас для построения LLM-агентов: на его SDK построен, в частности, OpenClaw.

<details>
<summary> Таблица 2.2 Агенты с открытым кодом </summary>

<table>
<thead>
<tr>
<th>Инструмент</th>
<th>Тип клиента</th>
<th>Интерфейс</th>
<th>Windows</th>
<th>macOS</th>
<th>Linux</th>
<th>Плагины/MCP</th>
<th>Клиент-сервер</th>
<th>Язык</th>
<th>Интеграции</th>
<th>GitHub</th>
<th>Цена</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>OpenCode</strong></td>
<td>Отдельный</td>
<td>CLI / Desktop / IDE / Web</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP, плагины</td>
<td>Мультисессии, headless, Web</td>
<td>TypeScript</td>
<td>75+ провайдеров, GitHub Copilot, LSP</td>
<td>150K ★</td>
<td>Бесплатно</td>
</tr>
<tr>
<td><strong>Cline</strong></td>
<td>Встройка</td>
<td>VS Code / CLI</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP (создание из чата)</td>
<td>Интегрирован в IDE</td>
<td>TypeScript</td>
<td>OpenRouter, Anthropic, OpenAI, AWS Bedrock, локальные</td>
<td>61.5K ★</td>
<td>Бесплатно</td>
</tr>
<tr>
<td><strong>Pi-agent</strong></td>
<td>Отдельный</td>
<td>CLI (TUI) / RPC / SDK</td>
<td>✓ (WSL2)</td>
<td>✓</td>
<td>✓</td>
<td>Extensions + Skills (нет MCP)</td>
<td>RPC (stdin/stdout JSONL), SDK</td>
<td>TypeScript</td>
<td>25+ провайдеров; tmux, контейнеры</td>
<td>45.8K ★</td>
<td>Бесплатно (MIT)</td>
</tr>
<tr>
<td><strong>Aider</strong></td>
<td>Отдельный</td>
<td>CLI</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>Нет</td>
<td>CLI, headless, watch-режим</td>
<td>Python</td>
<td>Claude, DeepSeek, OpenAI, локальные; Git-автокоммиты</td>
<td>44.5K ★</td>
<td>Бесплатно</td>
</tr>
<tr>
<td><strong>Continue</strong></td>
<td>Встройка</td>
<td>VS Code / JetBrains / CLI</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP, агенты как Markdown</td>
<td>CLI-проверки в CI/CD</td>
<td>TypeScript</td>
<td>GitHub (статус-чеки на PR), любые LLM</td>
<td>33K ★</td>
<td>Бесплатно</td>
</tr>
<tr>
<td><strong>Qwen Code</strong></td>
<td>Отдельный</td>
<td>CLI / VS Code / JetBrains / Zed</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP, Skills, SubAgents</td>
<td>Headless (`qwen -p`), SDK</td>
<td>TypeScript</td>
<td>OpenAI-API, Anthropic, локальные, OpenRouter</td>
<td>24K ★</td>
<td>Бесплатно</td>
</tr>
<tr>
<td><strong>Roo Code</strong></td>
<td>Встройка</td>
<td>VS Code</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP, Custom Modes</td>
<td>Интегрирован в IDE</td>
<td>TypeScript</td>
<td>Все основные провайдеры; русский в интерфейсе</td>
<td>24K ★</td>
<td>Бесплатно</td>
</tr>
<tr>
<td><strong>LangChain</strong></td>
<td>Фреймворк</td>
<td>Библиотека (Python/TS)</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP, Deep Agents</td>
<td>LangSmith (платный мониторинг)</td>
<td>Python</td>
<td>Стандартные интерфейсы для LLM, эмбеддингов, векторных БД</td>
<td>136K ★</td>
<td>Бесплатно</td>
</tr>
<tr>
<td><strong>CrewAI</strong></td>
<td>Фреймворк</td>
<td>Библиотека / CLI</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP</td>
<td>Crews (автономные) + Flows</td>
<td>Python</td>
<td>Multi-agent оркестрация</td>
<td>51K ★</td>
<td>Бесплатно</td>
</tr>
<tr>
<td><strong>AutoGPT</strong></td>
<td>Отдельный</td>
<td>Платформа / CLI / Web</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>Частично</td>
<td>Self-hosted + Cloud beta</td>
<td>Python</td>
<td>Agent Builder, Marketplace</td>
<td>184K ★</td>
<td>Бесплатно</td>
</tr>
<tr>
<td><strong>MetaGPT</strong></td>
<td>Отдельный</td>
<td>CLI</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>Нет</td>
<td>CLI / HuggingFace Space</td>
<td>Python</td>
<td>Роли PM, архитектора, инженера</td>
<td>68K ★</td>
<td>Бесплатно</td>
</tr>
</tbody>
</table>

</details>

<strong>Проприетарные агенты:</strong>

<strong>[Claude Code](https://claude.com/product/claude-code)</strong> (Anthropic) — терминальный AI-разработчик. Автономная работа с кодом, коммиты, PR. Но: в РФ нужен и VPN, и иностранная карта. Худшая доступность.
<strong>[VS Code](https://code.visualstudio.com/)</strong> — база. Минималистичный, расширяемый. Самый распространённый. <strong>GitHub Copilot</strong> - это по сути то же самое.
<strong>[Cursor](https://cursor.com/get-started)</strong> — AI IDE (форк VS Code). Composer 2, сверхточное автодополнение, облачные агенты.
<strong>[Windsurf](https://www.windsurf.dev/)</strong> — ещё один agentic IDE. Cascade (локальный агент) + Devin (облачный). Agent Command Center — канбан-доска для управления агентами.
<strong>[Antigravity](https://antigravity.google/)</strong> (Google) — десктоп-приложение. Регионально ограничен, но сообщество поддерживает `open-antigravity-patcher` для обхода блокировок в РФ.

<details>
<summary> Таблица 2.3 Агенты с закрытым кодом </summary>

<table>
<thead>
<tr>
<th>Инструмент</th>
<th>Тип клиента</th>
<th>Вендор</th>
<th>Интерфейс</th>
<th>Windows</th>
<th>macOS</th>
<th>Linux</th>
<th>MCP</th>
<th>Клиент-сервер</th>
<th>Особенности</th>
<th>Цена</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Codex</strong></td>
<td>Отдельный</td>
<td>OpenAI (США)</td>
<td>Desktop / VS Code / CLI / Web</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>Да</td>
<td>Cloud-агенты, worktrees</td>
<td>Cloud-агенты, worktrees, computer use, 90+ плагинов</td>
<td>В подписке ChatGPT</td>
</tr>
<tr>
<td><strong>Claude Code</strong></td>
<td>Отдельный</td>
<td>Anthropic (США)</td>
<td>CLI / IDE / Desktop / Web</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>Да</td>
<td>Headless, Remote Control</td>
<td>Автономная работа с кодом и PR; худшая доступность в РФ</td>
<td>$20–200/мес</td>
</tr>
<tr>
<td><strong>Claude Cowork</strong></td>
<td>Отдельный</td>
<td>Anthropic (США)</td>
<td>Desktop GUI / Web</td>
<td>✓</td>
<td>✓</td>
<td>—</td>
<td>Плагины</td>
<td>Десктоп + Web</td>
<td>Автономные задачи для нетехнических</td>
<td>В подписке</td>
</tr>
<tr>
<td><strong>GitHub Copilot</strong></td>
<td>Встройка</td>
<td>Microsoft (США)</td>
<td>VS Code / JetBrains / Xcode / CLI / Web</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP</td>
<td>Облачные агенты, CLI</td>
<td>Copilot, Claude, Codex — модель на выбор</td>
<td>Free–$39/мес</td>
</tr>
<tr>
<td><strong>Cursor</strong></td>
<td>Отдельный</td>
<td>Anysphere (США)</td>
<td>AI IDE / CLI / Slack</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP</td>
<td>IDE + Cloud Agents</td>
<td>Composer 2; Tab-модель; 50%+ Fortune 500</td>
<td>Free–$40/мес</td>
</tr>
<tr>
<td><strong>Windsurf</strong></td>
<td>Отдельный</td>
<td>Cognition AI (США)</td>
<td>AI IDE / JetBrains</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP</td>
<td>Cascade + Devin</td>
<td>Agent Command Center — канбан для агентов</td>
<td>Free–$15/мес</td>
</tr>
<tr>
<td><strong>Antigravity</strong></td>
<td>Отдельный</td>
<td>Google (США)</td>
<td>Desktop (Electron)</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>Cloud Code endpoint</td>
<td>Облачный (Google Cloud)</td>
<td>Регионально ограничен; community patcher для РФ</td>
<td>Freemium</td>
</tr>
<tr>
<td><strong>Cody</strong></td>
<td>Встройка</td>
<td>Sourcegraph (США)</td>
<td>VS Code / JetBrains / VS / Web / CLI</td>
<td>✓</td>
<td>✓</td>
<td>✓</td>
<td>MCP</td>
<td>Sourcegraph Enterprise</td>
<td>Глубокое понимание кодовой базы</td>
<td>Freemium</td>
</tr>
</tbody>
</table>

</details>

<strong>Агенты общего назначения</strong> стоят особняком от кодинг-агентов. Это не встройка в IDE и не CLI-утилита для работы с репозиторием — это персональные ассистенты, которые живут на вашем сервере/локальной машине, помнят контекст между сессиями и доступны через Telegram, Discord, Slack и другие каналы.

<details>
<summary> Таблица 2.4 Агенты общего назначения (ассистенты) </summary>

<table>
<thead>
<tr>
<th>Инструмент</th>
<th>Интерфейс</th>
<th>Каналы</th>
<th>Память</th>
<th>Self-host</th>
<th>MCP</th>
<th>Самообучение</th>
<th>Язык</th>
<th>GitHub</th>
<th>Цена</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>OpenClaw</strong></td>
<td>CLI (TUI) / Gateway + Web UI / iOS + Android</td>
<td>24+ (WhatsApp, Telegram, Slack, Discord, Signal, iMessage)</td>
<td>Config-файлы, context engine</td>
<td>Да (Docker/локально)</td>
<td>Да (bundle-плагины)</td>
<td>Частично</td>
<td>TypeScript</td>
<td>369K ★</td>
<td>Бесплатно (MIT)</td>
</tr>
<tr>
<td><strong>Hermes Agent</strong></td>
<td>CLI (TUI) / Gateway / Web UI</td>
<td>Telegram, Discord, Slack, WhatsApp, Signal, Email, CLI</td>
<td>MEMORY.md, USER.md, FTS5 поиск</td>
<td>Да (Python/VPS)</td>
<td>Да</td>
<td><strong>Да</strong> (auto-skills)</td>
<td>Python + TS</td>
<td>104K ★</td>
<td>Бесплатно (MIT)</td>
</tr>
<tr>
<td><strong>Moltis</strong></td>
<td>Web UI / CLI</td>
<td>Telegram, WhatsApp, Discord, Slack, Matrix, Nostr, Teams</td>
<td>SQLite + FTS + vector</td>
<td>Да (single binary, Rust)</td>
<td>Да</td>
<td>Нет</td>
<td>Rust</td>
<td>—</td>
<td>Бесплатно</td>
</tr>
<tr>
<td><strong>Leon</strong></td>
<td>Web UI / CLI</td>
<td>Web, голос</td>
<td>Layered memory</td>
<td>Да (Node.js)</td>
<td>Нет</td>
<td>Нет</td>
<td>TS + Python</td>
<td>17K ★</td>
<td>Бесплатно (MIT)</td>
</tr>
<tr>
<td><strong>OpenAkita</strong></td>
<td>GUI / CLI</td>
<td>Telegram, Feishu, WeCom, DingTalk, QQ</td>
<td>Daily health-check</td>
<td>Да (Python)</td>
<td>Да</td>
<td>Да (self-taught skills)</td>
<td>Python + TS + Rust</td>
<td>1.7K ★</td>
<td>Бесплатно (Apache 2.0)</td>
</tr>
</tbody>
</table>

</details>

<strong>Важный нюанс:</strong> почти все агенты — «агностики». Они не привязаны к конкретному вендору. Вы можете направить Cline на OpenRouter, Aider — на DeepSeek API, OpenCode — на локальную Ollama. Связка выбирается под задачу и бюджет. Исключения: Claude Code работает только с моделями Anthropic; Qwen Code оптимизирован под Qwen, но принимает и другие эндпоинты.

<strong>[OpenClaw](https://github.com/openclaw/openclaw)</strong> (369K ★) — лидер среди ассистентов общего назначения (см. таблицу 2.4). Это не чисто кодинг-агент, а персональный AI-ассистент с мультиканальным Gateway (24+ каналов). Агентный движок построен на Pi-agent SDK. Влияние на экосистему колоссально: именно OpenClaw популяризировал TUI-интерфейс среди массовой аудитории, а его система навыков ClawHub (5400+ skills) задала стандарт для реестров агентных умений.

<strong>[Hermes Agent](https://github.com/nousresearch/hermes-agent)</strong> (104K ★) — самообучающийся агент от Nous Research. Создаёт reusable skills из опыта, улучшает их в процессе работы. Встроенный cron-планировщик, субагенты, браузерная автоматизация. 18+ LLM-провайдеров.

Выбор агента — вопрос привычек (CLI/IDE/Web) и языка реализации. Выбор API — вопрос доступности, цены и качества модели для конкретной задачи. Специализированных российских AI-агентов для работы с кодом по состоянию на май 2026 <strong>не существует</strong>. YandexGPT и GigaChat — LLM общего назначения, не agentic tools. Адаптация open-source решений (Cline, Aider, Qwen Code) с локальными моделями или российскими API-провайдерами — основной путь для разработчиков и вайб-кодеров в РФ.

---

### А внутри у ней - нейронка: плагин, память и контекст

Вы собрали связку «агент + API» и она работает. Но со временем приходит понимание: агент, который после каждой сессии «забывает» всё на свете — это пол-агента. Ему нужна память, причем такая, которая не сжигает все контекстное окно еще до старта задачи. Ему нужны инструменты, хорошо бы мониторируемые и логируемые. Не лишним будет распараллеливание работы, запуск отдельных суб-агентов. Для простых ребят, не владеющих тайным мастерством программирования, желательно, чтобы эти инструменты кто-то уже написал.

К счастью, вокруг каждого крупного агента выросла экосистема. И она быстро конвергирует к единым стандартам.

#### Рынок плагинов и MCP-серверы

Плагины расширяют функциональность агента — дают доступ к файловой системе, базам данных, API, браузеру, терминалу. Без плагинов агент умеет только генерировать текст.

<strong>MCP (Model Context Protocol)</strong> стал универсальным стандартом подключения инструментов. Репозиторий `modelcontextprotocol/servers` — 85K звёзд, 10K форков, тысячи community-серверов. MCP работает через stdio или HTTP/SSE, позволяет подключить любой внешний инструмент без написания кода внутри самого агента.

Самый раздутый маркетплейс — <strong>[ClawHub](https://clawhub.ai/)</strong> у OpenClaw. 5400+ скиллов, 52 тысячи инструментов, 180 тысяч пользователей, 12 миллионов загрузок. У <strong>Claude Code</strong> — [официальный маркетплейс от Anthropic](https://code.claude.com/docs/en/discover-plugins) — 13 официальных плагинов. <strong>Cline</strong> — агент сам создаёт MCP-серверы из чата.

Реестры MCP-серверов: <strong>[Smithery](https://smithery.ai/)</strong> — Большой пул MCP общего назначения: поисковые, аналитика по блокчейнам, астрологические прогнозы. Бесплатно 50 000 вызовов в месяц.

, <strong>[PulseMCP](https://pulsemcp.com/)</strong> — Агрегатор MCP - сам доступ не раздает. Все серверы свалены в кучу, не для всех опубликованы эндпоинты (т.е. нашел какой-то MCP - идешь к провайдеру и смотришь как привязаться).

, <strong>[MCPM](https://mcpm.sh/)</strong> — Фишка - есть свой "MCP Manager". Инструмент интегрируется с "ассистентами" и "кодинг-агентами" позволяет искать и настраивать MCP без походов по сайтам и репозиториям.


.

<details>
<summary> Таблица 3.1 Форматы плагинов для разных экосистем </summary>

<table>
<thead>
<tr>
<th>Агент</th>
<th>Формат плагинов</th>
<th>MCP</th>
<th>Особенности</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>OpenClaw</strong></td>
<td>Native (`.openclaw.plugin.json`) + bundle (Codex/Claude/Cursor)</td>
<td>Да (через bundle)</td>
<td>Крупнейшая экосистема; ClawHub — 5400+ скиллов, 52.7K инструментов</td>
</tr>
<tr>
<td><strong>Claude Code</strong></td>
<td>`.claude-plugin/plugin.json` + хуки (9 событий)</td>
<td>Да (`.mcp.json`)</td>
<td>13 официальных плагинов: code-review, feature-dev, pr-review-toolkit</td>
</tr>
<tr>
<td><strong>Cline</strong></td>
<td>MCP (создание из чата)</td>
<td>Да</td>
<td><strong>Уникальная фича:</strong> агент сам пишет и устанавливает MCP-серверы</td>
</tr>
<tr>
<td><strong>Pi-agent</strong></td>
<td>Extensions (TypeScript), Pi Packages (npm)</td>
<td>Нет (принципиально)</td>
<td>Extensions регистрируют инструменты, команды, hotkeys, UI-компоненты</td>
</tr>
<tr>
<td><strong>OpenCode</strong></td>
<td>Custom Commands (Markdown), MCP</td>
<td>Да</td>
<td>MCP через stdio/SSE; 75+ LLM-провайдеров; LSP-автозагрузка</td>
</tr>
<tr>
<td><strong>Cursor</strong></td>
<td>`.cursor/rules`, `.cursor-plugin`</td>
<td>Да</td>
<td>AgentSkills</td>
</tr>
<tr>
<td><strong>Windsurf</strong></td>
<td>`.windsurfrules`</td>
<td>Да</td>
<td>Ограничено</td>
</tr>
</tbody>
</table>

</details>

#### Скиллы (Skills)

Скилл — это не код, а <strong>инструкция + контекст</strong>. Файл `SKILL.md` с YAML frontmatter описывает, что агент должен делать в определённой ситуации. Модель сама решает, когда активировать скилл.

<strong>Главное отличие от плагинов:</strong> плагин добавляет новый инструмент (функцию, API-вызов), скилл добавляет новые знания и поведенческие паттерны. Скилл не требует программирования — это markdown-файл с инструкциями.

<strong>Стандарт AgentSkills (SKILL.md)</strong> — совместим между Pi, Claude Code, Cline, OpenClaw, OpenCode. YAML frontmatter содержит `name`, `description`, `triggers` — по ним модель определяет, какой скилл применить.

#### Контекст-файлы

Помимо плагинов и скиллов, поведение агента задаётся через markdown-файлы в директории проекта. Самый простой способ «настроить» агента без единой строчки кода:

| Файл | Назначение | Где используется |
|---|---|---|
| <strong>AGENTS.md</strong> | Общие инструкции для всех агентов в проекте | OpenClaw, Cline, Codex, Cursor и др. |
| <strong>SOUL.md</strong> | Личность, стиль общения, ценности агента | OpenClaw, Hermes Agent |
| <strong>TOOLS.md</strong> | Описание доступных инструментов | OpenClaw |
| <strong>USER.md</strong> | Профиль пользователя: предпочтения, стиль | Hermes Agent, OpenClaw, и др. |
| <strong>MEMORY.md</strong> | Долговременная память агента | Hermes Agent |
| <strong>.clinerules</strong> | Правила поведения для Cline | Cline |
| <strong>.cursorrules</strong> | Правила поведения для Cursor | Cursor |

Эти файлы автоматически подхватываются агентом при старте сессии и инжектируются в системный промпт. Их можно версионировать в Git.

#### Память агента — иногда за нее нужно платить

Агент который знает и помнит все про вашу машину, про вас, про ваши привычки. Страшно... очень страшно... Но значительной части юзеров именно это и надо. Чтобы агент поддерживал стиль общения, помнил, над чем вы с ним работаете, дольше одной сессии.

<strong>Типы памяти:</strong> session (внутри одной сессии), cross-session (предпочтения между сессиями), long-term / archival (архив с recall-механизмом).

<strong>[Mem0](https://mem0.ai/)</strong> (55K ★, Apache 2.0) — де-факто стандарт. Алгоритм v3 (апрель 2026): single-pass ADD-only экстракция, entity linking, multi-signal retrieval. Бенчмарки: 91.6 на LoCoMo, 93.4 на LongMemEval. Self-hosted: `pip install mem0ai` или `docker compose up`.

<strong>[Letta](https://github.com/letta-ai/letta)</strong> (ex-MemGPT, 22.5K ★) — self-editing memory: агент сам обновляет свою память. Архивная память + recall.

<strong>[LangMem](https://github.com/langchain-ai/langmem)</strong> (MIT) — Memory SDK для LangGraph-агентов.

<details>
<summary> Таблица 3.2 Сравнение готовых решений для организации памяти агента </summary>

<table>
<thead>
<tr>
<th>Решение</th>
<th>Тип</th>
<th>Звёзд</th>
<th>Self-host</th>
<th>MCP</th>
<th>Подключение</th>
<th>Цена</th>
<th>Особенности</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Mem0</strong></td>
<td>Open-source (Apache 2.0) + Cloud</td>
<td>55K</td>
<td>Да (`pip install mem0ai` / Docker)</td>
<td>Да</td>
<td>Библиотека / Docker / Cloud</td>
<td>Бесплатно (self-host) / Cloud от $20/мес</td>
<td>Multi-level memory; v3: single-pass ADD-only, entity linking; бенчмарки 91.6 LoCoMo</td>
</tr>
<tr>
<td><strong>Letta</strong> (ex-MemGPT)</td>
<td>Open-source (Apache 2.0) + Cloud</td>
<td>22.5K</td>
<td>Да (Docker)</td>
<td>Нет (REST API)</td>
<td>Docker / Cloud</td>
<td>Бесплатно (self-host) / Cloud от $25/мес</td>
<td>Self-editing memory blocks; агент сам обновляет память; архивная память + recall</td>
</tr>
<tr>
<td><strong>LangMem</strong></td>
<td>Open-source (MIT)</td>
<td>1.4K</td>
<td>Да (`pip install langmem`)</td>
<td>Нет</td>
<td>Библиотека</td>
<td>Бесплатно</td>
<td>Memory SDK для LangGraph; core memory API; background memory manager</td>
</tr>
<tr>
<td><strong>Zep</strong></td>
<td>Проприетарное облако</td>
<td>4.5K</td>
<td>❌ (deprecated)</td>
<td>Да</td>
<td>Cloud only</td>
<td>От $49/мес</td>
<td>Graph RAG + temporal knowledge graph; sub-200ms latency; SOC2/HIPAA</td>
</tr>
</tbody>
</table>

</details>

#### Векторные базы как фундамент памяти

Любое memory-решение опирается на векторную БД. Для продвинутых пользователей — возможность развернуть свой memory backend без готовых решений.

<strong>[Milvus](https://milvus.io/)</strong> (44K ★), <strong>[Qdrant](https://qdrant.tech/)</strong> (31K ★), <strong>[ChromaDB](https://www.trychroma.com/)</strong> (28K ★), <strong>[Weaviate](https://weaviate.io/agentic-ai)</strong> (16K ★) — все open-source, все разворачиваются локально в Docker, все бесплатны.

<details>
<summary> Таблица 3.3 Векторные базы данных </summary>

<table>
<thead>
<tr>
<th>БД</th>
<th>Звёзд</th>
<th>Язык</th>
<th>Лицензия</th>
<th>Сложность</th>
<th>Локально</th>
<th>Облако</th>
<th>Особенности</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>ChromaDB</strong></td>
<td>27.8K</td>
<td>Rust + Python</td>
<td>Apache 2.0</td>
<td>★☆☆ (легко)</td>
<td>Да (embedded / Docker)</td>
<td>Chroma Cloud</td>
<td>API из 4 функций; встроена в Mem0 по умолчанию; `pip install chromadb`</td>
</tr>
<tr>
<td><strong>Qdrant</strong></td>
<td>31.1K</td>
<td>Rust</td>
<td>Apache 2.0</td>
<td>★★☆ (средне)</td>
<td>Да (Docker / in-memory)</td>
<td>Qdrant Cloud (free tier)</td>
<td>Квантование векторов (экономия RAM до 97%); фильтрация по payload</td>
</tr>
<tr>
<td><strong>Milvus</strong></td>
<td>44.2K</td>
<td>Go + C++</td>
<td>Apache 2.0</td>
<td>★★★ (сложно)</td>
<td>Да (Docker/K8s, Milvus Lite)</td>
<td>Zilliz Cloud (free tier)</td>
<td>GPU acceleration, fully distributed, 10B+ векторов</td>
</tr>
<tr>
<td><strong>Weaviate</strong></td>
<td>16.1K</td>
<td>Go</td>
<td>BSD-3</td>
<td>★★☆ (средне)</td>
<td>Да (Docker)</td>
<td>Weaviate Cloud</td>
<td>Гибридный поиск, RAG, реранкинг, мультиарендность</td>
</tr>
<tr>
<td><strong>Pinecone</strong></td>
<td>—</td>
<td>—</td>
<td>Проприетарная</td>
<td>★☆☆ (легко)</td>
<td>❌ (cloud only)</td>
<td>Pinecone Cloud</td>
<td>Serverless, SOC2/HIPAA; только API</td>
</tr>
</tbody>
</table>

</details>

<strong>Когда нужна векторная БД:</strong> если вы строите RAG-систему, работаете с большими документами, или хотите кастомную память агента с семантическим поиском. Для большинства пользователей достаточно Mem0 (self-hosted) с ChromaDB — это минимум кода и максимум результата.

Экосистема расширений — то, что превращает агента из игрушки в инструмент. Плагины и скиллы добавляют способности. Memory-решения добавляют контекст между сессиями. Векторные БД — фундамент. Почти всё open-source и работает локально — российскому пользователю здесь вольготно.

---

### Полный суверенитет и абсолютное погружение: локальный инференс

Вы преисполнились. Вам мало облачных API. Хочется, чтобы модель работала на вашем железе, без интернета, без лимитов, без оглядки на чужие серверы. Все - мы в стадии локального развертывания БЯМ. Здесь три составляющих: <strong>где брать модели</strong>, <strong>чем их запускать</strong> и <strong>на чём их запускать</strong>. Ответ на последний вопрос суперпростой - на чем угодно. Современные модели постояннно оптимизируются под "слабенькие" железки, снижают требования к объему памяти и вычислительной мощности квантизацией и ротацией активных параметров. <strong>Видеокарта НЕ обязательна</strong> - большинство инструментов запуска (почти у всех под капотом llama.cpp) прекрасно работает как с GPU, так и со связкой CPU+RAM. Отсюда стандартный вывод: много оперативы не бывает.

#### Репозитории моделей

Главный хаб планеты — <strong>[Hugging Face](https://huggingface.co/)</strong>. 2 миллиона моделей. Доступен из России без VPN (май 2026). Некоторые российские аккаунты удалены, но сам сайт открыт. При больших загрузках может барахлить без VPN.

<strong>[ModelScope](https://www.modelscope.ai/home)</strong> — китайский аналог HF от Alibaba. Эксклюзивные китайские модели, которых нет на Hugging Face.

<strong>[Ollama Library](https://ollama.com/library)</strong> — встроенный реестр моделей для инструмента Ollama.

<strong>[CivitAI](https://civitai.com/models)</strong> — репозиторий моделей для генерации изображений (Stable Diffusion, Flux).

<details>
<summary> Таблица 4.1 Репозитории открытых моделей. Сервисы для хостинга LLM-инстансов </summary>

<table>
<thead>
<tr>
<th>Репозиторий</th>
<th>Назначение</th>
<th>Примечание</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Hugging Face</strong> (huggingface.co)</td>
<td>Основной мировой репозиторий — 2M+ моделей</td>
<td>✅ Доступен из РФ (май 2026). Некоторые аккаунты РФ-организаций (sberbank-ai) удалены, но сайт открыт.</td>
</tr>
<tr>
<td><strong>GitHub</strong> (github.com)</td>
<td>Хостинг кода, Git LFS для моделей, релизы</td>
<td>✅ Доступен.</td>
</tr>
<tr>
<td><strong>ModelScope</strong> (modelscope.cn)</td>
<td>Китайский аналог HF от Alibaba. Китайские модели (Qwen, DeepSeek, GLM, Yi и др.)</td>
<td>✅ Доступен. Некоторые модели эксклюзивно на ModelScope.</td>
</tr>
<tr>
<td><strong>Ollama Library</strong> (ollama.com/library)</td>
<td>Встроенный реестр моделей Ollama</td>
<td>✅ Доступен.</td>
</tr>
<tr>
<td><strong>CivitAI</strong> (civitai.com)</td>
<td>Репозиторий моделей для генерации изображений (SD, Flux)</td>
<td>✅ Доступен.</td>
</tr>
</tbody>
</table>

</details>

Собственного российского репозитория нет. Российские открытые модели — это практически исключительно экосистема Сбера (GigaChat, ruGPT, Kandinsky), выложенные организацией ai-sage на Hugging Face. Яндекс веса не публикует.

#### Инструменты запуска

<strong>[llama.cpp](https://github.com/ggml-org/llama.cpp)</strong> (109K ★) — фундамент всего. Чистый C++, без внешних зависимостей. Компилируется под всё: от серверной стойки с 8×H100 до Android-телефона. Поддерживает 200+ архитектур, квантование от 1.5 до 8 бит. Multi-node через RPC. OpenAI-совместимый API-сервер.

<strong>[Ollama](https://ollama.com/)</strong> (109K ★) — проприетарная обёртка над llama.cpp, доведённая до состояния «скачал и заработало». Одна команда `ollama run llama3` — и модель отвечает. Есть платный облачный уровень Pro/Max.

<strong>[vLLM](https://vllm.ai/)</strong> (79.3K ★) — инструмент для продакшена. Python, PagedAttention, continuous batching. Максимальная пропускная способность при массовых запросах. Multi-node. `pip install vllm` — и поехали.

[<strong>SGLang</strong>](https://github.com/sgl-project/sglang) (18K ★) — инференс-комбайн на Питоне. Есть отдельный режим оптимизации запуска на <strong>CPU-only</strong> сборках. 

[<strong>ExLlamaV3</strong>](https://github.com/turboderp-org/exllamav3) (4.5K ★) — простое решение для простых моделек. Заявлена оптимизация под инференс на потребительских видеокарточках. 

[<strong>TensorRT-LLM</strong>](https://github.com/NVIDIA/TensorRT-LLM) (12K ★) — инференс-решение от nVidia - нуф сказал

<strong>[LM Studio](https://lmstudio.ai/)</strong> — десктопное приложение с GUI. Встроенный каталог моделей: выбрал → скачал → запустил. OpenAI-совместимый API из коробки. Бесплатно для коммерческого использования.

[<strong>Open WebUI</strong>](https://github.com/open-webui/open-webui) (137K ★, 290M+ загрузок) — комбайн для запуска модели сразу с интерфейсом. Подхватывает мультимодальные модельки и дает им интерфейсы для создания картинок, звуков видео. По сути инструмент инференса+сервер+агент в одном флаконе.

[<strong>Jan</strong>](https://github.com/janhq/jan) (82K ★) — просто чятик, который можно оживить оптимизированными Qwen-модельками или, через небольшие танцы с бубном, любой моделькой. 

[<strong>LocalAI</strong>](https://github.com/mudler/LocalAI) (26K ★) — Очередной комбайн "для всего". Особенность: поддерживается куча бэкенд-версий,  отсюда теоретическая возможность запуска почти на любом относительно современном железе. Есть <strong>CPU-only</strong>

<details>
<summary> Таблица 4.2 Движки инференса (backend) </summary>

<table>
<thead>
<tr>
<th>Инструмент</th>
<th>Тип</th>
<th>Платформы</th>
<th>Распределённый</th>
<th>API</th>
<th>Форматы</th>
<th>GPU</th>
<th>Ключевые особенности</th>
<th>Звёзды</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>llama.cpp</strong></td>
<td>Open-source (C++)</td>
<td>Win, Lin, Mac, iOS, Android, RISC-V</td>
<td>✓ Multi-GPU + Multi-node RPC</td>
<td>OpenAI-совместимый</td>
<td>GGUF</td>
<td>CUDA, Metal, Vulkan, SYCL, HIP</td>
<td>200+ архитектур; квантование 1.5–8 бит; чистый C++; CPU+GPU гибрид</td>
<td>109K</td>
</tr>
<tr>
<td><strong>Ollama</strong></td>
<td>Проприетарная обёртка</td>
<td>Win, Lin, Mac</td>
<td>✗</td>
<td>OpenAI-совместимый</td>
<td>GGUF (llama.cpp)</td>
<td>CUDA, Metal</td>
<td>Простейшая установка: `ollama run llama3`; реестр моделей</td>
<td>109K</td>
</tr>
<tr>
<td><strong>vLLM</strong></td>
<td>Open-source (Python)</td>
<td>Linux; NVIDIA/AMD/Intel/TPU</td>
<td>✓ Tensor/Pipeline parallelism; Multi-node</td>
<td>OpenAI + Anthropic API</td>
<td>HF, GGUF, GPTQ/AWQ, FP8</td>
<td>CUDA, ROCm, Gaudi, TPU</td>
<td>PagedAttention; 200+ архитектур; continuous batching</td>
<td>79.3K</td>
</tr>
<tr>
<td><strong>SGLang</strong></td>
<td>Open-source (Python)</td>
<td>Linux; NVIDIA/AMD</td>
<td>✓ Tensor parallelism; Multi-node</td>
<td>OpenAI-совместимый</td>
<td>HF, GGUF</td>
<td>CUDA, ROCm</td>
<td>RadixAttention (prefix caching 85-95%); xGrammar для JSON; на 29% быстрее vLLM на RAG</td>
<td>18K</td>
</tr>
<tr>
<td><strong>MLX</strong></td>
<td>Open-source (Apple)</td>
<td>Mac (Apple Silicon), Linux</td>
<td>Multi-device (CPU+GPU)</td>
<td>Python API (`mlx-lm`)</td>
<td>MLX, HF, GGUF</td>
<td>Apple Silicon GPU</td>
<td>Разработан Apple; NumPy-подобный API; lazy computation</td>
<td>26K</td>
</tr>
<tr>
<td><strong>ExLlamaV3</strong></td>
<td>Open-source (Python/C++)</td>
<td>Win, Lin (NVIDIA)</td>
<td>Multi-GPU</td>
<td>TabbyAPI (OpenAI-совместимый)</td>
<td>GPTQ, EXL2, EXL3</td>
<td>CUDA</td>
<td>Преемник ExLlamaV2; максимальная производительность на NVIDIA</td>
<td>4.5K</td>
</tr>
<tr>
<td><strong>TensorRT-LLM</strong></td>
<td>Open-source (NVIDIA)</td>
<td>Linux (NVIDIA)</td>
<td>✓ Tensor parallelism</td>
<td>OpenAI-совместимый</td>
<td>HF, TensorRT engine</td>
<td>CUDA</td>
<td>Максимальная пропускная способность на H100/B200; FP4 inference</td>
<td>12K</td>
</tr>
</tbody>
</table>

</details>

<details>
<summary> Таблица 4.3 Интерфейсы и платформы (frontend) </summary>

<table>
<thead>
<tr>
<th>Инструмент</th>
<th>Тип</th>
<th>Платформы</th>
<th>Подключение</th>
<th>MCP</th>
<th>RAG</th>
<th>Ключевые особенности</th>
<th>Звёзды</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Open WebUI</strong></td>
<td>Open-source (Web)</td>
<td>Docker, K8s, pip</td>
<td>Ollama, OpenAI, Anthropic, vLLM</td>
<td>Да</td>
<td>✓ (9 БД, 15+ поисков)</td>
<td>Де-факто стандарт self-hosted; multi-user RBAC; Python-функции; code execution; voice/video; 290M+ загрузок</td>
<td>137K</td>
</tr>
<tr>
<td><strong>LM Studio</strong></td>
<td>Проприетарное (GUI)</td>
<td>Win, Lin, Mac</td>
<td>Встроенный (llama.cpp), Ollama</td>
<td>Да (клиент)</td>
<td>✗</td>
<td>Десктопный GUI; каталог моделей; side-by-side сравнение; бесплатный для коммерческого использования</td>
<td>—</td>
</tr>
<tr>
<td><strong>TextGen (oobabooga)</strong></td>
<td>Open-source (Python)</td>
<td>Win, Lin, Mac</td>
<td>Встроенный (Transformers, llama.cpp, ExLlamaV3)</td>
<td>Да (сервер)</td>
<td>✗</td>
<td>Веб-интерфейс (Gradio); multimodal; LoRA-тренировка; генерация изображений; TTS</td>
<td>47K</td>
</tr>
<tr>
<td><strong>GPT4All</strong></td>
<td>Open-source (GUI)</td>
<td>Win, Lin, Mac</td>
<td>Встроенный (llama.cpp)</td>
<td>✗</td>
<td>✓ (LocalDocs)</td>
<td>LocalDocs — чат с документами; Python API; Vulkan-ускорение</td>
<td>77.4K</td>
</tr>
<tr>
<td><strong>KoboldCpp</strong></td>
<td>Open-source (C++)</td>
<td>Win, Lin, Mac, Android (Termux)</td>
<td>Встроенный (llama.cpp)</td>
<td>✗</td>
<td>✗</td>
<td>Один исполняемый файл; LLM + Image Gen + Video Gen + STT + TTS + Music Gen</td>
<td>10.4K</td>
</tr>
<tr>
<td><strong>Jan</strong></td>
<td>Open-source (Desktop)</td>
<td>Win, Lin, Mac</td>
<td>Встроенный (llama.cpp, ONNX), облачные</td>
<td>✗</td>
<td>✗</td>
<td>Приватный десктопный GUI; гибридный локальный/облачный режим</td>
<td>82K</td>
</tr>
<tr>
<td><strong>LocalAI</strong></td>
<td>Open-source (Go)</td>
<td>Docker, Linux, Mac</td>
<td>Встроенный (llama.cpp, SD, whisper)</td>
<td>✗</td>
<td>✗</td>
<td>Drop-in замена OpenAI API; текст + изображения (SD) + TTS + STT через один endpoint</td>
<td>26K</td>
</tr>
</tbody>
</table>

</details>

<strong>Когда что выбирать:</strong>
- <strong>Просто запустить модель</strong> → Ollama (`ollama run llama3`) или LM Studio (GUI)
- <strong>Максимум контроля</strong> → llama.cpp напрямую (C++, квантование, все платформы)
- <strong>Продакшен с высокой нагрузкой</strong> → vLLM (универсальный) или SGLang (RAG/multi-turn, структурированный вывод)
- <strong>Полноценная self-hosted платформа</strong> → Open WebUI поверх Ollama/vLLM (multi-user, RAG, MCP, функции)
- <strong>Apple Silicon</strong> → MLX (разработан Apple, нативная оптимизация)
- <strong>Максимум на NVIDIA</strong> → TensorRT-LLM (H100/B200, FP4)

Российских инструментов для локального инференса нет. Российские модели запускаются через международные инструменты — те же GGUF-квантизации GigaChat 3.1 работают в llama.cpp и Ollama без проблем.

### Напоследок

Является ли этот гайд/обзор полным и исчерпывающим? Конечно нет. Во первых все онлан-чятики, провайдеров API, кодинг-агентов, различных около-ИИшных утилит и инструментов - не переназвать. Во ворых отрасль развивается очень быстро, и также быстро устареет этот материал. Где-то в середине лета выйдут новые крупные западные и китайские модели (скриньте этот твит). Скорее всего, еще раньше появится новая "хайповая" тема - навроде OpenClaw в начале этого года. Но парой вещей эта портянка ценна: она описывает логику знакомства обычного работяги с БЯМами, плюс тут очень много ссылочек на всяческую халяву и опен-сорц. Надеюсь, вам пригодится.

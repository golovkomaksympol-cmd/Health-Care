---
name: deep-think
description: Single entry point / router for serious thinking. Use when the user says "подумай со мной" / "ответь глубоко", "разбери проблему" / "по научному методу", asks "стоит ли / что лучше / что думают эксперты", or faces a strategic / irreversible / protocol-defining question. Routes to an empirical cycle (cheaply testable) or an expert panel (judgment). Tier 2/3 — answers can and should be expansive, NOT the short bot format.
---

# Deep-think skill (Tier 2/3) — the single door

One entry point that **diagnoses where you are and routes you**: goal-gate → locate the problem → then either run the **empirical cycle** (Mode A, when there's a cheap falsification test) or convene the **expert panel** (Mode B, when it's judgment with no cheap test). The panel is a *generator* you can call inline from either mode. **Answers here can and should be long and developed** — overrides the default short bot format.

Shared spine for both modes: `_core/Models/Scientific Method (Measure Zero).md` — **kill before confirm; presume your hypothesis is wrong.** The only difference between modes is *what kills the hypothesis*: **reality** (Mode A, empirical test) or an **adversarial red team** (Mode B, the best substitute when reality can't be cheaply queried).

## Step 0 — Goal gate (Munger-секретарь, ВСЕГДА первым)
Загрузи цели/ограничения из профиля человека (файл целей — `User Context` / `Human Context` / `Practices`, как он назван у этого человека; если профиля нет — спроси цель и ограничение одной строкой). Прогони тему через три вопроса: **цель → ограничение → необходимые условия**. Это кресло ведёт **Munger-lens** (альтернативная стоимость + инверсия + право вето «не стоит внимания»), рядом Goldratt (это ли ограничение?) и Gigerenzer (стоит ли вообще считать?).
- Если тема — **не текущее ограничение, не станет им скоро и не угрожаемое необходимое условие** → выдай: «не constraint-relevant: лог + дешёвый tripwire, внимание = ноль» и **СТОП. Ни цикл, ни панель не запускать.** (Escape-hatch: дёшево + необратимый хвост → всё равно лог+tripwire.)
- Главная роль секретаря — **держать дискуссию в русле целей и противостоять «дотошному помогателю»**.

## Step 0.5 — Locate & route (диспетчер)
Пройди эти четыре вопроса вслух и объяви маршрут:
1. **Есть ли задача — и хорошо ли поставлена?** Задача задаёт **внешний критерий истинности** (Tarski — критерий вне системы). Сделай её измеримой: **число + диапазон + горизонт** (даже «в попугаях», но считаемо; *if you don't measure, you don't care*). Расплывчатую («хочу выспаться», «хочу знать правду») → сначала переформулируй в измеримую. Если реальной задачи нет → назад в Step 0 (лог+tripwire, стоп).
2. **На каком я этапе?** Назови точку в цикле: нет задачи / есть задача, нет гипотез / есть гипотезы, не проверены / есть наблюдения, не прочитаны / есть правило. Дальше работаешь **от этой точки**, а не с нуля.
3. **Можно ли просто фальсифицировать?** Есть ли **дешёвый, быстрый** эмпирический тест, различающий гипотезы?
   - **ДА → Mode A (эмпирический цикл).** Иди проверять реальность; не созывай панель, чтобы рационализировать красивую историю.
   - **НЕТ** (ценность / стратегия / нет дешёвого теста) **→ Mode B (панель суждения).**
4. **Нужны гипотезы или разные ракурсы?** Панель — это твой **генератор** (гипотез, наблюдений, способов убийства). Вызывай её **внутри** любого режима, когда своих сведений не хватает.

---

## Mode A — Эмпирический цикл (научный метод)
Модель: `_core/Models/Scientific Method (Measure Zero).md`. Цикл — **спираль**, не выстрел; приоритет — **скорость и дешевизна** каждого витка.

1. **Задача** — измеримый критерий + горизонт (из Step 0.5).
2. **Гипотезы** — 2–5, каждая как **`если [причина] → [измеримый результат]`**; для каждой сразу **критерий убийства** (что её опровергнет). Начинай **с гипотезы, не со сбора данных**. Выбери вероятнейшую, **запиши почему**. *(Не хватает — созови панель как генератор.)*
3. **Дедукция → прогноз на один шаг:** «если верно, при X за время T увижу Y (число)». Точный прогноз — только на **один шаг**.
4. **Наблюдение:** самый **дешёвый** тест, меняй **один фактор**, фиксируй всё, особенно неудобное.
5. **Фальсифицируй ПЕРВЫМ делом.** Триггер: как только наблюдение в руках — сверь с заранее записанным критерием убийства (*modus tollens: H→P, видишь ¬P ⟹ ¬H*). Проектируй наблюдение как **попытку убийства** (severe test), не подтверждение. Убил → следующая гипотеза; аномалии → отдельно, как супергипотезы.
6. **Верифицируй** только пережившую несколько убийств → подкрепление, **не доказательство**; серия / шире горизонт → «лучший способ на сегодня».
7. **Обобщи** в правило + **«что нового узнал → уточнённая модель»** → новый виток.
- **Anti-patterns** (называй, если проскальзывают): сдвиг рамки после провала, добавление условий, обвинение реальности, confirmation-hunting («сову на глобус»), одиночный анекдот как доказательство, **влюблённость в гипотезу**. Статистика — только чтобы породить/ранжировать гипотезы, инстанс решает практика.

---

## Mode B — Панель суждения (для вопросов без дешёвого теста)

### B1 — Refine the question first (Шаман / Серкин)
Do **not** rush to answer. The one who asks already senses the answer — draw it out and sharpen what's truly being asked.
- Restate the question back, sharper than posed. Strip vagueness; name the implicit goal (what is optimized, against what constraint).
- Surface hidden assumptions and what would actually change the user's decision.
- If the real question differs from the literal one, say so and offer the reframe.
- Briefly reflect what the user likely already believes — that belief is **data**, and the panel will test it, not flatter it.
Proceed only once the question is crisp. If genuinely ambiguous, ask one tight clarifying question first.

### B2 — Select experts (topic **and** meta-topic)
From `_core/mentor-panel.md`. **Only those who genuinely have something to say** — on the **topic** (domain experts) **and** on the **meta-topic** (the kind of question: decision under uncertainty, systems/strategy, behavior change…). 2–4 total + one **additional** relevant world-expert on the subject **not** on the mentor panel.

### B3 — Run each expert in a separate thread (parallel)
Spawn **one sub-agent per expert** (Agent tool), all in a single message → **parallel / independent**. This structurally enforces "independent views before conflict" — experts cannot converge by agreeing in sequence. Each gets the refined question, its lens, and the relevant data files (`Health profile`, `lab.json`, `Practices`, recent `daily/`). Each reasons **only** from its lens, **hypotheses → validate → conclude** (no jumping), and returns its strongest independent take + where it thinks the user is wrong.

### B4 — Synthesize with anti-sycophancy
Full contract: `meta-thinking.md` (framework root). The three non-negotiables:
1. **Name the expected answer, then forbid it** — surface only what contradicts or extends it.
2. **Mandatory red team** — ≥1 expert on the opposite conclusion (premortem: "assume this failed in 2 years — why?"). No unanimous panels. *(This red team IS the falsification for a non-empirical question.)*
3. **Falsifiable tripwire per conclusion** — measurement + when it would prove the conclusion wrong. *(Same object as Mode A's kill-criterion.)*
Ground every claim in the person's data, not vibes.

## Models
Reusable models live in `Models/` at the framework root (`_core/Models/` in a health-repo setup; `../../Models/` relative to this file when installed standalone). Pull the relevant one in rather than reasoning from scratch.

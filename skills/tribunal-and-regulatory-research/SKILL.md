---
name: tribunal-and-regulatory-research
description: Research Indian tribunal orders and regulatory material with Veritect — DRT, DRAT, NCLT, NCLAT, ITAT, CESTAT, GSTAT, SAT, RERA, NGT and other tribunals, and RBI, SEBI, CCI, GST, MCA and occupational safety instruments. Use when the user asks what a tribunal has held, or what a regulator's direction, circular, notification or regulation says.
---

# Tribunal orders and regulatory material with Veritect

Tribunal orders and regulatory instruments come in two kinds of text. Keep them apart in every
answer:

- **AI summary** — Veritect's reading of an order or instrument. Use it to understand and to
  choose what to read. **Paraphrase it and cite it; never quote it** as the tribunal's or the
  regulator's words.
- **Published text** — the order or instrument itself. **Quote only this**, and only what a
  Veritect tool returned in this conversation.

## Tribunal orders

1. **Search** with `search_tribunals`. Choose the tribunals the question needs and use the
   filters that fit (order type, outcome, assessment year or tax period, amount range).
   Use `search_caselaw` instead for the Supreme Court and High Courts.
2. **Orient** with `get_tribunal_order` at the default depth: the full AI summary, the bench,
   the provisions, the holding, the order under challenge, and the case's other orders in date
   order. Each other order has its own `order_id` — read the final order, not only the first
   hit, when the outcome matters.
3. **Read the order itself** with `get_tribunal_order` at `depth: "full"` before quoting. Long
   orders come in windows: pass `next_cursor` back as `cursor`. An order marked
   `order_translation` is a machine translation — say so when you quote it.
4. **Cite** the tribunal, case title, case number and order date exactly as returned.

## Regulatory material

1. **Search** with `search_regulations`, naming the regulator: `rbi`, `sebi`, `cci`, `gst`,
   `ohs` or `mca`. Use a focused query: the obligation, topic, instrument name or reference
   number. Check `content_kind` on each passage: `published_text` may be quoted,
   `ai_summary` must be paraphrased.
2. **Read the instrument** with `get_regulation` and its `regulation_id`. For a numbered
   regulation, pass one provision number from its `provision_directory` to read just that
   provision. Text is paged: follow `next_cursor` before saying you have read it all.
3. **Check its status.** Results default to current instruments. A superseded or draft
   instrument must be labelled as such. The published text does not by itself prove current
   legal force — say what the status field shows.
4. A CCI or MCA **order** found here carries an `order_id`: read it with `get_tribunal_order`.
   SEBI appeals are Securities Appellate Tribunal orders: search them with `search_tribunals`.

## Say what you did not find

- Read `search_coverage`. A tribunal marked unavailable or failed was not searched — that is
  not evidence that no orders exist. Say so.
- Never describe results as exhaustive, and never fill a gap from memory.

## When access is refused

Tribunal and regulatory search is an add-on to a Veritect account. If a tool answers that the
add-on isn't active, tell the user once, in plain words, and pass on the message it gave. Do not
retry the call, and do not answer the question from memory instead. Court judgments and
statutes are still available through `search_caselaw` and `search_statutes`.

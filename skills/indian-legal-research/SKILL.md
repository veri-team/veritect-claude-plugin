---
name: indian-legal-research
description: Research Indian case law and statutes with Veritect and cite them verbatim. Use when the user asks about Indian law — judgments of the Supreme Court or any High Court, a section of a central bare act, what the courts have held on a point, or the authority behind a citation.
---

# Indian legal research with Veritect

Veritect holds India's legal corpus: judgments and orders of the Supreme Court and all 25 High
Courts, and India's central bare acts. Every answer you give from it must be grounded in text
Veritect returned in this conversation, and cited so the lawyer can check it in one click.

## The one rule

**Quote only text that a Veritect tool returned in this conversation.** Never quote a judgment
or a statute from memory, and never present a paraphrase as the court's or the legislature's
words. If you have not read the passage, say so and read it before quoting.

## Judgments

1. **Search** with `search_caselaw`. Use short topic keywords or a focused question. Pick the
   courts the question needs (the default is the Supreme Court and Delhi). For the latest
   judgments, sort by `judgment_date_desc`.
2. **Orient** with `get_judgment` at `depth: "summary"` (the AI summary) or `depth: "analysis"`
   (the AI analysis of reasoning and holdings). These are Veritect's AI readings: use them to
   decide what matters, and paraphrase them — never quote them as the court's words.
3. **Read the judgment itself** with `get_judgment` at `depth: "full"` before you quote a
   holding. Long judgments come in windows: pass `next_cursor` back as `cursor` until you reach
   the passage you need. Do not claim to have read a whole judgment you only partly read.
4. **Cite** with the case title and citations exactly as returned (`case_title`,
   `neutral_citation`, `scr_citation`), the paragraph you quote from, and the link (`pdf_url`
   for the court's original PDF, or `url` for Veritect's analysis).

A `j:` reference found inside a matter's work products (for example a judgment compilation) is
the same reference a search returns: pass it straight to `get_judgment`.

## Statutes

1. **Search** with `search_statutes`. Each hit is one section, with a bounded passage.
2. **Read the whole section** with `get_provision`, copying the hit's `act_id` and `section`
   exactly. Quote the provision only from what `get_provision` returns.
3. Name a Part or Chapter only when the result carries `location`; otherwise give the section
   number alone.
4. **Check which law applied on the relevant date.** India's new criminal codes replaced the
   older codes for events from 1 July 2024. When the facts, offence or proceeding began earlier,
   or a savings clause may apply, say which law governs and why, and read the predecessor
   provision as well where it matters. Do not substitute one code for the other silently.

## Say what you did not find

- Read `search_coverage` in every search result. A court or source marked unavailable was not
  searched: say so plainly. It is not evidence that no judgment exists.
- Searches return the closest matches, not every judgment ever delivered. Never describe a
  result as exhaustive, and never invent a contrary authority you did not find.
- If a search finds nothing useful, try a different angle (other keywords, other courts, a
  narrower question) before concluding, and tell the user what you tried.

## How to present the answer

- Lead with the answer to the question, then the authorities that support it.
- For each authority: what it held (in your words), the quoted passage (from the full text),
  and the citation with its link.
- Keep the AI summary or analysis and the court's own words visibly separate.
- These are research aids for a qualified lawyer, not legal advice. Flag open questions the
  lawyer should decide.

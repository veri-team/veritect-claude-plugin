---
name: drafting-from-a-matter
description: Draft an Indian court filing, notice, reply or contract from a Veritect matter, in court format or the firm's own template. Use when the user asks to draft a petition, application, written statement, reply, affidavit, legal notice, submissions or agreement for a matter they have in Veritect.
---

# Drafting from a Veritect matter

A good draft takes its **form** from a template, its **facts** from the matter record and its
**law** from verified authorities. Keep the three apart: a template's example wording is never a
fact of this matter, and no authority is cited from memory.

## 1. Understand the matter first

Follow the `working-with-a-matter` skill: `get_matter_overview`, then `read_counsel_notes`,
then `read_artifact` for `case_analysis` and `strategy`. Note whom the lawyer represents, the
forum, the stage of the proceeding and what the lawyer wants the document to achieve. If what
the lawyer asks for conflicts with the record, ask before drafting.

## 2. Choose the template

- If the lawyer names their own format, call `list_personal_drafting_templates` and then
  `get_personal_drafting_template`. Use it as the scaffold; do not swap in a built-in one.
- Otherwise call `list_drafting_skills` to find the court-format template for the document,
  then `get_drafting_skill`.
- Many templates have **sub-types** (for example, a bail application differs by the offence
  and the stage). Choose the sub-type from the matter — its provisions, forum and posture — not
  from how the request was worded. If the response says it returned the default variant and
  names a narrower one that fits, read that one before drafting.
- Read the whole template body (follow `next_cursor`, or open the sections you need) and follow
  its structure, headings, verification and prayer formats.

## 3. Gather the law

- Use the matter's `judgment_compilation` and `provisions_compilation` first: they hold the
  authorities already selected for this case. Read any authority you rely on with
  `get_judgment` (`depth: "full"` before quoting) and any provision with `get_provision`.
- Add research only where the compilations leave a gap, following the `indian-legal-research`
  skill. Quote only text a tool returned in this conversation.

## 4. Draft

- Every factual statement comes from the record. Use the document's exact words for anything
  quoted, and keep a note of the document and page for each fact.
- Where the record is silent on something the document needs, leave a clearly marked
  placeholder (for example **[date of notice — not found in the record]**). Never invent a
  date, amount, name or event.
- Cite each authority with its case title and citation exactly as returned.

## 5. Hand it over

After the draft, list for the lawyer: the template and sub-type used, the placeholders left
open, any point where the record was inconsistent, and the authorities relied on with their
links. The lawyer settles and files the document; nothing is filed or sent from here.

These are drafting aids for a qualified lawyer, not legal advice.

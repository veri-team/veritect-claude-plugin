![Veritect](assets/veritect-lockup.png)

# Veritect for Claude

India's most complete legal corpus in Claude: Supreme Court, all 25 High Courts, 14 tribunals,
central bare acts and RBI, SEBI, CCI regulations. Grounded, cited, verbatim.

Veritect gives Claude India's most comprehensive, complete and up-to-date legal corpus, with every answer grounded in the source text and cited.

**Every court that matters.** More than 50 million judgments and orders from the Supreme Court, all 25 High Courts and 14 tribunals, updated as new judgments are delivered.

**Four ways into every judgment.** The true PDF copy as issued by the court; a detailed AI analysis of the reasoning and holdings; a precise AI summary; and the full OCR text in English, ready for Claude to read, quote and cite. Each carries its neutral citation and a link to the original. Claude takes only the depth it needs, so research is fast and token-efficient.

**Every statute, verbatim.** Search India's central bare acts and read them section by section, so Claude quotes the law word for word.

**The regulatory rulebook.** Gazette notifications, circulars and regulations from RBI, SEBI, CCI, GST, MCA and safety regulators.

**Your matters, deeply understood.** A matter can hold 10,000 files, and Veritect is no file store. It inspects every file in depth: reads every word, OCRs scanned copies, translates regional-language documents and summarises each one. It then builds a judgment compilation and a provision compilation of the law that governs and supports your case. Claude works from that analysed record, so drafts are precise, accurate and compelling.

**Court-ready drafting** from Veritect's court-format templates or your firm's own.

**Why it matters:** hours of research become minutes, nothing is cited from memory, and every point can be checked in one click.

**Read-only and private:** nothing is changed, filed or sent, nothing is shared until you choose a matter, and access can be withdrawn instantly.

For advocates, law firms and in-house teams practising Indian law. Requires a Veritect account ([agent.veritect.ai](https://agent.veritect.ai)).

Research and drafting aids for qualified professionals, not legal advice.

## What this plugin contains

| Part | What it does |
|---|---|
| **Veritect connector** (`.mcp.json`) | Connects Claude to Veritect's remote server at `https://mcp.veritect.ai/mcp` — the same server as the Veritect connector in Claude's directory. |
| **Skill: Indian legal research** | Searches judgments and statutes, reads the judgment or section itself before quoting, and cites with neutral citations and links. |
| **Skill: Tribunal and regulatory research** | Works with tribunal orders and RBI, SEBI, CCI, GST, MCA and safety instruments, keeping AI summaries (paraphrased) apart from published text (quoted). |
| **Skill: Working with a matter** | Answers questions from a shared matter's analysed record — overview, analyses, documents, contract clauses, list of dates — citing document and page. |
| **Skill: Drafting from a matter** | Drafts filings, notices and agreements from a shared matter in court format or the firm's own template, with facts from the record and verified law. |

The skills are plain instructions in Markdown. The plugin has no hooks, scripts, commands or
local programs.

## What it connects to and sends

- The plugin connects to **one** service: `https://mcp.veritect.ai/mcp`, run by Veritect.
- You sign in with your Veritect account in your browser (OAuth). Claude never sees your
  password.
- Claude sends Veritect the searches and read requests it makes on your behalf (for example a
  research question, a judgment reference or a matter id). Veritect returns judgments,
  statutes, tribunal orders, regulatory text and the contents of matters you have shared.
- Every tool is **read-only**: nothing in Veritect is changed, filed or sent.
- **Nothing from your matters is shared until you choose.** In the Veritect app, open
  **Settings → Assistant & devices**, allow assistant access, and switch on the matters Claude
  may read. Switch access off there at any time; it takes effect at once.
- Use of the tools counts against your Veritect account's allowance.

## Setup

1. Have a Veritect account at [agent.veritect.ai](https://agent.veritect.ai).
2. In the Veritect app, open **Settings → Assistant & devices**, allow assistant access and
   choose the matters to share (research needs no matters).
3. Install this plugin, then sign in to Veritect when Claude asks.

## Example prompts

1. "Find Supreme Court judgments on whether a cheque bounce complaint under Section 138 of the
   Negotiable Instruments Act lies when the cheque was given as security. Quote the key holding
   and give the citation."
2. "Show me the full text of Section 9 of the Arbitration and Conciliation Act, 1996, then find
   two Delhi High Court judgments on interim relief under it."
3. "Open my shared Veritect matter, summarise the parties, issues and key dates, and draft a
   list of dates for written submissions, citing the documents for each date."

## Documentation, support and privacy

- Documentation: [mcp.veritect.ai](https://mcp.veritect.ai/)
- Support: [info@veritect.ai](mailto:info@veritect.ai)
- Privacy policy: [veritect.ai/privacy-policy](https://veritect.ai/privacy-policy)
- Terms: [veritect.ai/terms-of-service](https://veritect.ai/terms-of-service/)

Veritect Pte. Ltd. · [veritect.ai](https://veritect.ai)

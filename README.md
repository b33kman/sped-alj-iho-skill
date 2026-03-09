# Special Education ALJ / IHO Assistant Skill
### A Claude Cowork Skill for Administrative Law Judges and Impartial Hearing Officers

This skill helps **Administrative Law Judges (ALJs)** and **Impartial Hearing Officers (IHOs)** work more efficiently on special education due process hearings under the Individuals with Disabilities Education Act (IDEA) and applicable state law.

It is designed for the two-party dispute context: **parents/students** vs. **school districts**, covering both educational issues (IEPs, placement, services) and in-school issues (behavioral plans, classroom treatment, disciplinary matters).

---

## What This Skill Does

Once imported into Claude Cowork, this skill gives Claude six specialized workflows:

| Workflow | What It Does |
|---|---|
| **A — Document Editing** | Edits communications, orders, and notices for clarity, tone, and legal precision |
| **B — Case Decision Summary** | Summarizes provided case decisions from within the four corners of the opinion only — no editorial content |
| **C — Distinguishing Cases** | Compares two or more provided cases side-by-side to identify key factual and legal distinctions |
| **D — Findings of Fact Editing** | Refines draft findings to be concise, direct, and evidentiary grounded |
| **E — Notes & Testimony Synthesis** | Organizes judge notes by issue and highlights consistency or contradiction across witnesses |
| **F — Transcript Analysis** | Analyzes hearing transcripts by issue, with automatic PII anonymization before any processing |

---

## Safety Features

This skill has three non-negotiable safeguards built in:

**1. No Hallucination**
Claude will never generate, infer, or recall case citations, legal holdings, or statutory text. If a case is referenced by name only, Claude will stop and ask for the full case text before proceeding. All legal analysis is grounded only in documents provided by the user.

**2. Automatic PII Anonymization**
Before processing any transcript or document, Claude automatically replaces all personally identifiable information with role-based identifiers:
- Student names → `[Student]`
- Parent/guardian names → `[Parent]`
- Teacher names → `[Teacher]`
- School/district names → `[School]` / `[District]`
- Addresses, DOBs, IDs → `[Address]`, `[DOB]`, `[ID]`

Claude will never reproduce PII in any output, even if asked.

**3. Case Text Required**
Case decisions must always be provided in full (uploaded or pasted). Claude will never summarize or analyze a case it has not been given directly.

---

## State Coverage

This skill includes procedural reference information for **all 50 states and Washington D.C.**, including:
- Administering agency name and abbreviation
- Primary governing statutes and administrative code citations
- Decision timelines (including state-specific variations, e.g. Florida's stricter 30-day rule)
- Appeal pathways
- State-specific terminology (e.g. ARD in Texas, PPT in Connecticut, ESE in Florida, BSEA in Massachusetts)

At the start of each session, Claude asks for the state jurisdiction and loads the relevant procedural context automatically.

---

## How to Install

### Option 1: Import the `.skill` file directly (easiest)
1. Download `sped-alj-skill.skill` from this repository
2. Open **Claude Cowork**
3. Go to **Settings → Skills**
4. Click **Import Skill** and select the downloaded file

### Option 2: Install from the folder manually
1. Download or clone this repository
2. In Claude Cowork, go to **Settings → Skills → Install from folder**
3. Point it to the `sped-alj-skill/` directory

---

## How to Use

At the start of a session, tell Claude:
- Your **state** (e.g. "I'm in New York")
- Your **role** (ALJ or IHO)
- Your **task** (e.g. "I need to summarize this case decision" or "analyze this transcript")

Claude will confirm the workflow and proceed. You can upload files or paste text directly into the chat.

**Example prompts:**
- *"I'm an IHO in Pennsylvania. Please edit this order for clarity."*
- *"Summarize this case decision — I've pasted the full opinion below."*
- *"Here are two cases the parties are relying on. Help me distinguish them."*
- *"I've uploaded a hearing transcript. Please analyze testimony about the IEP."*

---

## File Structure

```
sped-alj-skill/
├── SKILL.md                        # Main skill instructions and workflows
├── README.md                       # This file
├── sped-alj-skill.skill            # Packaged skill file for direct import
└── references/
    └── state-procedures.md         # Procedural reference: all 50 states + D.C.
```

---

## Important Disclaimer

This skill is a productivity tool to assist legal professionals — it is **not a substitute for legal judgment**. Claude will not recommend how a case should be decided, suggest which party should prevail, or provide legal advice. All outputs should be reviewed by the ALJ or IHO before use in any official proceeding.

Procedural information in `state-procedures.md` is provided as a working reference only. Always verify current rules against official state regulations and agency guidance.

---

## Contributing

If you find errors in state procedural information or have suggestions for additional workflows, please open an issue or submit a pull request.

---

## License

This skill is shared freely for use by administrative law judges, impartial hearing officers, and special education legal professionals. See `LICENSE` for details.

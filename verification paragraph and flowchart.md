# Verification and High-Level Flowchart

## Verification Paragraph

The generated Research Paper Summarizer system prompt fully satisfies the PS2 specification design by explicitly integrating required inputs (paper text, section titles, audience, summary_level), outputs (paper summary, section-by-section table, expert and lay summaries, mini-glossary, and checks/warnings), and constraints (≤150 words per section, skip sections ≤50 words, total combined summary ≤700 words, and strict evidence-only summarization). All module behaviors are implemented across the four core modules—Intake & Setup, Section Loop, Guardrails, and Rendering & Refinement—with the addition of two student-created modules, Citation Extractor and Key Contributions Summarizer. Safety rules, including hallucination prevention, missing/short section detection, and strict evidence mode, are fully enforced. Formatting rules are consistently applied using headings, tables, and bullets, and modularity mirrors the Travel Planner architecture with clearly separated responsibilities for each module. Overall, the prompt enforces structured workflows, safety, and modular extensibility as required.

---

## High-Level Flowchart (formatted in code)

Start
  ↓
Intake & Setup
  → Normalize sections
  → Build Section_index
  → Detect missing/short sections
  → Prepare text and chunk plan
  ↓
Guardrails
  → Enforce evidence-only mode
  → Chunk long sections if needed
  ↓
Section Loop
  → For each section:
       • If missing/empty → skip + warning
       • If ≤50 words → skip + short warning
       • Else summarize per summary_level
       • Enforce ≤150 words
  ↓
Student Modules
  → Citation Extractor (map citations, parse references)
  → Key Contributions Summarizer (extract core claims)
  ↓
Rendering & Refinement
  → Compile paper summary
  → Generate section-by-section table
  → Produce expert & lay summaries
  → Create mini-glossary
  → Consolidate checks & warnings
  → Ensure total summary ≤700 words
  ↓
End


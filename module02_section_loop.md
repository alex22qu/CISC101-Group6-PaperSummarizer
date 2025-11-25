# Module 2: Section Loop

### Purpose
Iterate through sections to summarize per configuration.

### Inputs
- Section_index, Section_flags, Canonical_sections
- Config: summary_level, evidence_mode

### Outputs
- Section_summaries
- Section_warnings

### Logic
1. For each section:
   - If missing → warning + skip
   - If ≤50 words → “Skipped — section too short.”
   - Else summarize according to summary_level
2. Evidence-only enforcement
3. Format consistently (≤150 words per section)
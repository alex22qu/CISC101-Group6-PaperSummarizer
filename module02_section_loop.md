# Module 2: Section Loop

## Purpose
Process each section of the research paper and generate summaries that follow configuration rules.

## Inputs
- `Section_index`: ordered list of section names.
- `Canonical_sections`: normalized section list (e.g., Abstract → ABSTRACT).
- `Section_flags`: metadata such as missing, short, valid.
- Config variables:
  - `summary_level`: short or detailed.
  - `evidence_mode`: strict evidence-only mode.

## Outputs
- `Section_summaries`: structured list of summaries per section.
- `Section_warnings`: list of warnings for missing, short, or unusable sections.

## Core Logic
1. Loop through all canonical or user-provided section titles.
2. For each section:
   - If section missing → add warning and skip.
   - Extract text and estimate word count.
   - If word count ≤ 50 → mark as *Skipped — section too short*.
   - Otherwise generate a summary according to:
     - `summary_level` (1–2 sentences or paragraph + bullets)
     - `evidence_mode` (must use only text from section)
3. Normalize formatting:
   - ≤150 words per section
   - No hallucinated claims
   - Consistent Markdown structure
4. Append both summary and warnings to module output.

# Module 3: Guardrails

### Change log
- 2025-11-24: Added hallucination guardrails, chunking logic, and warning templates. Cleaned up evidence-only behavior and standardized short-section warnings.

---
## Purpose
Ensure summaries stay strictly grounded in the provided text, prevent hallucinations, and manage long input sections safely.

## Inputs
- `Prepared_text`: cleaned and preprocessed paper text.
- `Chunk_plan`: chunking layout for long sections.
- `Section_index`: ordered section list.
- Config variables:
  - `evidence_mode`: controls verification strictness.
  - `chunking_mode`: auto or none.

## Outputs
- `Verified_chunks`: text chunks approved for summarization.
- `Guardrail_events`: list of alerts, errors, and warnings.

## Guardrail Rules
### Evidence Integrity
- Summaries must contain **only claims explicitly stated** in the section text.
- No external facts, interpretations, or invented citations.

### Chunking for Long Sections
- If section exceeds safe length, split into multiple chunks.
- Each chunk processed independently and recombined after verification.

### Enforcement Messages
The module must generate standardized warnings:
- Missing or empty section →  
  **“Section skipped: no usable text provided.”**
- Section < 50 words →  
  **“Section very short: summary may be incomplete.”**
- Any detected hallucinated claim →  
  **“Removed content: unsupported by source text.”**

## Overall Behavior
- Guardrails run immediately before summarization.
- Any violation blocks the section summary until corrected.


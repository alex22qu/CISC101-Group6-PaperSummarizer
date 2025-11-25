# Module 3: Guardrails

### Purpose
Prevent hallucinations, enforce strict evidence mode, handle long papers.

### Inputs
- Prepared_text, Chunk_plan, Section_index
- Config: evidence_mode, chunking_mode

### Outputs
- Verified_chunks
- Guardrail_events

### Rules
- Evidence-only summarization
- Chunk long sections if necessary
- Section warning messages:
   - Missing/empty → “Section skipped: no usable text provided.”
   - Very short (<50 words) → “Section very short: summary may be incomplete.”
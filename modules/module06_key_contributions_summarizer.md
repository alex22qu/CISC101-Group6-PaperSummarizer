# Student Module: Key Contributions Summarizer

### Purpose
Extract core contributions from Abstract/Introduction/Conclusion.

### Inputs
- Section_index (Abstract, Introduction, Conclusion)
- Config: summary_level, evidence_mode

### Outputs
- Contributions_list (3–6 bullets)

### Logic
1. Identify phrases like “We propose…”, “Our contributions are…”
2. Deduplicate overlapping claims
3. Validate against source text (evidence-only)
4. Render bullets under Paper Summary

# Student Module: Citation Extractor

### Purpose
Extract in-paper citations, map them to sections.

### Inputs
- Prepared_text, Section_index
- Config: evidence_mode

### Outputs
- Citation_map
- Reference_entries

### Logic
1. Detect in-text citations ([1], (Author, Year), superscripts)
2. Parse References section
3. Only use info in paper (no external sources)
4. Provide hooks for section table
# Module 1: Intake & Setup

### Purpose
Prepare paper text, normalize sections, detect missing/short sections.

### Inputs
- Paper_text
- Requested_sections
- Config: summary_level, evidence_mode, chunking_mode

### Outputs
- Canonical_sections
- Section_index
- Section_flags
- Prepared_text
- Chunk_plan

### Steps
1. Normalize section names (e.g., Background/Related Work → Background)
2. Segment and index content
3. Detect missing or short sections
4. Clean text (remove headers/footers, preserve equations/citations)
5. Plan chunks if paper is long

# CISC101-Group6-PaperSummarizer
**Group 6 — Final Project**

This repository contains our modular Research Paper Summarizer, built for CISC 101. It summarizes research papers such as *Attention Is All You Need* and follows the multi-module architecture used in class.

## Project Summary
The summarizer produces:
- A full paper summary  
- Section-by-section table  
- Expert and lay summaries  
- A mini-glossary  
- Missing-section warnings  
- Strict hallucination and evidence guardrails  
All outputs follow the constraints defined in our PS2 specification.

---

## Module Overview

- **01 Intake & Setup:** Loads and normalizes text; flags missing or short sections  
- **02 Section Loop:** Generates summaries using `summary_level = short` or `detailed`  
- **03 Guardrails:** Strict evidence mode and standardized warning messages  
- **04 Rendering & Refinement:** Builds final structured output  
- **05 Citation Extractor:** Gathers citations from the paper  
- **06 Key Contributions:** Summarizes major contributions in bullet form  
---

## Group Members

(Alex Secrieru, Aaron John, Jordan Cooke)

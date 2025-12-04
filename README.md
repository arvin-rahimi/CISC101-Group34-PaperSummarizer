# 📑 CISC101 – Research Paper Summarizer  

This repository contains the full implementation of our group’s Research Paper Summarizer project
It mirrors the same architectural structure used in the Travel Planner project, including a complete system prompt and a multi-module internal framework.

---

## 🧩 Project Overview
The Paper Summarizer system is designed to take a research paper’s full text and generate:

- A structured paper summary  
- Section-by-section breakdown  
- Expert-level summary  
- Lay summary for general audiences  
- Mini-glossary  
- Citations extracted and formatted in APA  
- Key contributions summary  
- Warning checks (missing/empty/short sections)  

The system uses **modular prompting** to keep each task separate and maintain clarity, accuracy, and extensibility.

---

## 📁 Repository Structure

```
/
│── system_prompt.md
│── README.md
└── modules/
      ├── 01_intake_setup.md
      ├── 02_section_loop.md
      ├── 03_guardrails.md
      ├── 04_rendering_refinement.md
      ├── 05_citation_extractor.md
      └── 06_key_contributions.md
```

### **system_prompt.md**
Contains the **full master system prompt**, including:
- Greeting rules  
- Tone rules  
- Boundaries  
- Required user inputs  
- Required outputs  
- Integrated specification design  
- References to all modules  

### **modules/**
Each module contains **one functional component** of the summarizer:

| Module File | Description |
|-------------|-------------|
| `01_intake_setup.md` | Standardizes section names & checks for missing/short sections |
| `02_section_loop.md` | Loops through each section and generates summaries |
| `03_guardrails.md` | Missing/short section warnings, hallucination mitigation, chunking |
| `04_rendering_refinement.md` | Builds the final structured output for the user |
| `05_citation_extractor.md` | Extracts and formats citations into APA style |
| `06_key_contributions.md` | Identifies and alphabetizes core contributions |

---

## 🛠 How to Use
1. Load **system_prompt.md** as the system-level instruction for an LLM.  
2. Ensure each module is referenced correctly by the LLM’s internal logic.  
3. Provide a research paper and section list.  
4. The system produces:  
   - summary  
   - expert + lay summaries  
   - glossary  
   - warnings  
   - citations  
   - key contributions  

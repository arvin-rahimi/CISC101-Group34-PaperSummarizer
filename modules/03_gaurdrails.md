### Module 3: Guardrails
Detect:

- Missing/empty sections  
- Sections <50 words  
- Hallucination risks  
- Long-paper chunking (split into manageable context windows)

**Stict Evidence Mode**:

When mode = "strict" the summarizer should:

- Only include claims, equations, and results that appear in the provided text.
- If it cannot find enough information, it must say so explicitly (e.g., “The source text does not provide enough detail to summarize this section in strict evidence mode.”).

**Section Warning Messages**

- If sections are missing/empty the system must output: "Section skipped: no usable text was provided" 
- If section is too short (< 50 words) the system must output: "Section too short: information is potentially incomplete" 

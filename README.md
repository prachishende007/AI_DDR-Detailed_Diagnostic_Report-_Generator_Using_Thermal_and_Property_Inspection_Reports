# DDR AI Generator (Applied AI Builder)

## Project Objective
[cite_start]This system is an automated AI workflow designed to convert raw building site inspection documents and thermal imaging data into a structured, client-ready **Detailed Diagnostic Report (DDR)**[cite: 5]. [cite_start]The core focus is on reasoning, reliability, and the logical merging of qualitative observations with quantitative thermal findings[cite: 3, 4].

## Features
* [cite_start]**Automated Data Extraction**: Parses site observations and temperature readings from PDF documents[cite: 5].
* [cite_start]**Logical Information Merging**: Combines site inspection findings with thermal images to create a unified narrative[cite: 5, 9].
* **Conflict & Missing Data Handling**: 
    * [cite_start]If data points conflict, the system explicitly flags the discrepancy[cite: 6].
    * [cite_start]If information is missing, the system writes "Not Available" instead of hallucinating facts[cite: 6].
* [cite_start]**Client-Friendly Reporting**: Generates summaries and recommendations using simple language devoid of unnecessary jargon[cite: 6].

## DDR Report Structure
[cite_start]The generated report follows the mandatory structure defined in the assignment guide[cite: 5]:
* [cite_start]**Property Issue Summary** [cite: 5]
* [cite_start]**Area-wise Observations** [cite: 5]
* [cite_start]**Probable Root Cause** [cite: 5]
* [cite_start]**Severity Assessment**: Includes reasoning for the assigned level[cite: 5].
* [cite_start]**Recommended Actions** [cite: 5]
* [cite_start]**Additional Notes** [cite: 5]
* [cite_start]**Missing or Unclear Information**: Explicitly marks gaps as "Not Available"[cite: 5].

## Technical Stack
* **LLM**: DeepSeek-R1 (Ollama)
* **Framework**: Python, Pydantic (for reliable data structuring)
* **Libraries**: PyMuPDF (fitz) for PDF processing

## Installation & Setup
1. **Ollama**: Ensure Ollama is installed and the `deepseek-r1:8b` model is pulled.
2. **Environment**: Install dependencies:
   ```bash
   pip install pymupdf ollama pydantic
   ```
3. **Run**: Place input PDFs in the Sample_inputs/ folder and execute main.py.

---

Evaluation Criteria Adherence

- Accuracy: Uses regex to ensure thermal deltas are calculated accurately before AI reasoning.
- System Thinking: Designed to generalize to similar inspection reports beyond the provided samples
- Reliability: Implements Pydantic validation to handle imperfect AI JSON outputs.

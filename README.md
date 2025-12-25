# CV Library & CV Generator Project

## What this project does
This project helps you:
1. Build a reusable CV Library from all your past CVs and work summaries.
2. Generate a tailored, one-page CV for a specific job using that library.

The system is designed to work with any modern LLM.

---
## Files in this project

- system_prompt_01_build_library.txt  
  Used to create a reusable CV library (CVLibrary.json).

- system_prompt_02_generate_cv.txt  
  Used to generate a tailored CV from the library and a job description.

- sample_CVLibrary.json  
  A small demo example showing the expected JSON structure.

- README.md  
  This guide.

---
## How to use

### Step 1: Build your CV Library
1. Start a new LLM conversation.
2. Paste the contents of system_prompt_01_build_library.txt as the SYSTEM prompt.
3. Upload all your old CVs and work summaries.
4. Review and add impact where requested.
5. Save the output as CVLibrary.json.

### Step 2: Generate a tailored CV
1. Start a new LLM conversation.
2. Paste the contents of system_prompt_02_generate_cv.txt as the SYSTEM prompt.
3. Upload CVLibrary.json.
4. Upload or paste the job description.
5. Review the generated LaTeX CV.
6. Approve and generate the PDF.

---
## Design principles
- One-line bullets only.
- ATS and Recruiter friendly versions.
- No fabricated metrics.
- One-page output.

This structure allows you to reuse your experience efficiently across roles.


---

## Visualizing & Editing the CV Library (HTML App)

This project also includes an optional **browser-based visual editor**:

**`libraryVisualizer.html`**

### What it does
- Loads `CVLibrary.json`
- Lets you **expand/collapse by company → role → pointers**
- Allows selection/deselection of:
  - basics fields
  - skills (by group and item)
  - experience bullets
  - academic project bullets
- Supports **ATS / Recruiter toggle**
- Generates:
  - `cv_library_selected.json`
  - `cv.tex` (LaTeX CV using the fixed template)

### Typical workflow with the HTML app
1. Open `libraryVisualizer.html` in a browser.
2. Upload `CVLibrary.json` (or paste it).
3. Select only the items relevant to a job.
4. Toggle ATS / Recruiter view.
5. Generate and download `cv.tex`.
6. Upload `cv.tex` to Overleaf (or compile locally) to get PDF.

> Note: PDF generation is intentionally **not** handled in-browser to keep the app lightweight.

This visualizer is optional but strongly recommended for fast iteration.

# AI Detection Tool for Student Submissions

This tool uses Google's Gemini AI to analyze student responses for signs of AI generation. It evaluates multiple signals simultaneously including writing style, tone uniformity, instruction-following, and AI-typical phrasing patterns.

---

## Getting Started

### 1. Get a free Gemini API key

- Go to https://aistudio.google.com/app/apikey
- Sign in with a Google account
- Click **"Create API key"**
- Save your key somewhere safe — no credit card required

> Optional fallback: if you don't have a Gemini API key, you can use a DuckDuckGo (DDG) fallback — paste the prompt into DDG and copy the returned text back into the tool (instructions below).

### 2. Add your key to the tool (or use the DDG fallback)

- Go to the [detector link](https://unstoppalezzz.github.io/Ai-Detection-for-Hallucinating-Ai/ai-detector.html)
- If you have a Gemini API key: paste it into the **"Gemini API Key"** field at the top.
- If you do NOT have a key: you can still run an analysis by clicking **"Analyze Response"** without entering a key — the tool will perform the DDG fallback method automatically (or you can manually use DDG: paste the prompt into DDG, copy the output, then paste it into the tool’s input field).

### 3. Run an analysis

- Paste the **assignment prompt** into the left box
- Paste the **student's response** into the right box
- Optionally expand **"Add optional context"** to include:
  - Extra notes (e.g. class year, timed conditions, topic)
  - An exemplar genuine human response for better calibration
  - **A student baseline** (a confirmed human-written sample from the same student)
- Click **"Analyze Response"**

---

## What the Tool Checks

Each analysis produces five scored metrics (worth 20 points each) and a list of flagged issues:

| Metric | What it measures |
|---|---|
| **AI-like Patterns** | Formulaic transitions and "machine-perfect" grammar (0–20) |
| **Hallucination Risk** | Fabricated facts or claims that contradict the prompt (0–20) |
| **Instruction Mismatch** | Failure to follow specific constraints or "over-optimizing" instructions (0–20) |
| **Generic Writing** | Use of clichés and vague language that lacks original insight (0–20) |
| **Style Difference** | Delta between this work and the student’s known baseline voice (0–20) |

The tool provides an **overall AI likelihood score** (0–100), plus a **"Detected Issues"** list of specific red flags.

### Signals the tool looks for

- Hallucinated or unverifiable facts  
- Suspiciously perfect grammar and uniformity of tone  
- **Significant shifts in writing style** (when a baseline is provided)  
- Over-hedging language and AI-typical phrasing patterns  
- Unusually high use of em dashes (—), a common AI stylistic marker (em dashes are not in the US keyboard layout)  
- Generic, non-specific writing that could apply to any assignment  
- Poor alignment with the specific assignment prompt

> Note: The tool will warn you if the assignment prompt itself contains em dashes, as this can skew the analysis.

---

## Tips for Better Results

- **Provide extra context** — noting the student's year, whether it was timed, or the topic helps the engine calibrate its expectations.  
- **Add an exemplar** — providing a "Gold Standard" response helps the engine understand the expected academic level.  
- **Include a Student Baseline** — providing a confirmed human sample from the student allows the engine to detect shifts in rhythm and vocabulary.  
- **Export Reports** — Use the "Download Full Report PDF" button to save a timestamped audit of the analysis.

---

## ⚠️ Important

This tool **can and will make mistakes**. Always review the full analysis carefully before drawing any conclusions about a student's work. Do not use results alone as grounds for any disciplinary action.

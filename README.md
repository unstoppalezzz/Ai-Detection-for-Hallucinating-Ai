# AI Detection Tool for Student Submissions

This tool uses Google's Gemini AI to analyze student responses for signs of AI generation. It evaluates multiple signals simultaneously not just hallucinations including writing style, tone uniformity, instruction-following, and AI-typical phrasing patterns.

---

## Getting Started

### 1. Get a free Gemini API key

- Go to [https://console.cloud.google.com/apis/dashboard](https://console.cloud.google.com/apis/dashboard)
- Sign in with a Google account
- Navigate to **"Credentials"** and click **"Create credential"**, then select **"API key"**
- Use the default settings and copy your key when it appears
- Save your key somewhere safe — no credit card required

### 2. Add your key to the tool

- Go to the [detector link](https://unstoppalezzz.github.io/Ai-Detection-for-Hallucinating-Ai/ai-detector.html)
- Paste your key into the **"Gemini API Key"** field at the top

### 3. Run an analysis

- Paste the **assignment prompt** into the left box
- Paste the **student's response** into the right box
- Optionally expand **"Add optional context"** to include:
  - Extra notes (e.g. class year, timed conditions, topic)
  - An exemplar genuine human response for better calibration
- Click **"Analyze Response"**

---

## What the Tool Checks

Each analysis produces four scored metrics and a list of flagged issues:

| Metric | What it measures |
|---|---|
| **AI Detection Score** | Overall likelihood the response was AI-written (0–100) |
| **Hallucination Risk** | Whether the response contains fabricated or unverifiable facts (Low / Medium / High) |
| **Instruction Following** | How well the response actually addresses the assignment (0–100) |
| **Generic Writing Score** | How vague, non-specific, or template-like the writing is (0–100) |

The tool also provides an **overall AI likelihood meter** combining all signals, plus a **"Detected Issues"** list of specific red flags found in the text.

### Signals the tool looks for

- Hallucinated or unverifiable facts
- Suspiciously perfect grammar and uniformity of tone
- Lack of personal voice or student-typical errors
- Over-hedging language and AI-typical phrasing patterns
- Unusually high use of em dashes (—), a common AI stylistic marker
- Generic, non-specific writing that could apply to any assignment
- Poor alignment with the specific assignment prompt

> **Note:** The tool will warn you if the assignment prompt itself contains em dashes, as this can skew the analysis.

---

## Tips for Better Results

- **Provide extra context** — noting the student's year, whether it was timed, or the topic helps the model calibrate its expectations.
- **Add an exemplar** — pasting in a confirmed human response for the same assignment gives the model a baseline to compare against, improving accuracy noticeably.

---

## ⚠️ Important

This tool **can and will make mistakes**. Always review the full analysis carefully before drawing any conclusions about a student's work. Do not use results alone as grounds for any disciplinary action.

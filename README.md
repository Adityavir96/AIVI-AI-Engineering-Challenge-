# AIVI AI Engineering Challenge — Submission Package

## Included
- `AIVI_Audit_Report.docx` — preliminary platform/security audit and adversarial test plan.
- `system_prompt.md` — production-style system prompt.
- `resume_match.py` — Gemini API evaluator with strict Pydantic validation, JSON sanitizing, retries, timeout handling and clear errors.
- `requirements.txt` — Python dependency.
- `TEST_EXECUTION_LOG.md` — fill this with actual platform observations before claiming adversarial tests were executed.

## Run the Python script
1. Install Python 3.10 or newer.
2. Open a terminal in this folder.
3. Run `pip install -r requirements.txt`.
4. Set `GEMINI_API_KEY` as an environment variable. Do not put the key in source code or upload it.
5. Create two UTF-8 text files: `resume.txt` and `job_description.txt`.
6. Run:
   `python resume_match.py --resume resume.txt --job job_description.txt`
7. The validated JSON is printed and saved to `match_result.json`.

PowerShell:
`$env:GEMINI_API_KEY="YOUR_KEY"`

macOS/Linux:
`export GEMINI_API_KEY="YOUR_KEY"`

Optional model override:
`$env:GEMINI_MODEL="gemini-2.5-flash"`

## Important audit integrity note
The report records only the security-header scan findings supplied during the assignment. The adversarial Campus OS tests are listed as test cases, not as completed observations. Execute them only in an account/workspace you are authorized to use, with fictional test data, then replace the pending fields with screenshots and actual outputs. Do not use another institution's candidate records.

## Sharing
Upload the folder contents to Google Drive. Set link access to Viewer only if allowed by the recipient/company policy. Never upload API keys, private candidate resumes, or personal data.

# Candidate Screening Automation

An n8n workflow that helps review applications against predefined criteria. It combines a structured LLM prompt, a decision step, and a Google Sheets record for rejected candidates.

## Workflow

1. Receive a résumé for review.
2. Send its text to the Groq API with a prompt that extracts relevant experience and Python skills.
3. Evaluate the model response against the screening criteria.
4. Record rejected applications and the stated reason in Google Sheets; qualifying applications continue through the workflow.

The workflow JSON is included in this repository. Configure your own API and Google Sheets credentials in n8n before using it.

> Automated screening output should be checked by a human before making hiring decisions. Model responses can be incomplete or inaccurate.

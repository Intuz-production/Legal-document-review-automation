# Intuz — Your automation partner, one workflow at a time.

<p align="center">
  <picture>
    <img alt="Banner Image" src="https://github.com/user-attachments/assets/210f97fc-0fce-404a-b647-7dfe1302cd37" />
  </picture>
</p>

# Review contract risks and route approvals with Google Drive, OpenAI, and Gmail

[Intuz](https://www.intuz.com/) helps organizations orchestrate AI, automation, and enterprise systems through scalable workflows. Our repository showcases proven implementations across healthcare, operations, customer support, document processing, sales, and back-office functions, enabling teams to accelerate automation initiatives without starting from scratch.

[N8N Creator](https://n8n.io/creators/intuz/) · [AI Development](https://www.intuz.com/ai/) · [AI Consulting Company](https://www.intuz.com/ai-transformation-services/) · [For Custom Workflow Automation](https://www.intuz.com/get-started/)

---

## Quick overview

This workflow monitors a Google Drive folder for new contract PDFs, extracts and analyzes their text with OpenAI, routes the contract for email-based approval via Gmail based on contract value and policy risks, and logs the final decision to Google Sheets.

## How it works

1. Triggers every minute when a new file is created in a specified Google Drive folder.
2. Validates the file is a PDF, downloads it from Google Drive, and extracts the contract text.
3. Sends the extracted text to OpenAI (`gpt-4o-mini`) to return structured JSON with key contract fields and clause indicators.
4. Applies company policy rules to compute missing required clauses, risk flags, a risk score, and an approval route.
5. Routes the contract to Legal, Finance, or a Department Manager via Gmail approval emails based on the extracted contract value.
6. Waits for the recipient to approve or decline and then appends the approved or rejected outcome to a Google Sheets log.

## Setup

1. Connect Google Drive credentials and set the folder ID to watch for new contract uploads.
2. Add an OpenAI credential and confirm the model selection (`gpt-4o-mini`) meets your compliance and data-handling requirements.
3. Connect a Gmail account for **"send and wait"** approval emails and replace the recipient email addresses with your reviewers.
4. Connect Google Sheets credentials and update the spreadsheet ID/sheet tab used to append approved and rejected contract records.

## Additional info

## Support

If you need help setting up this workflow or require a custom version tailored to your specific use case, please feel free to reach out to the template author:

* **Website:** https://www.intuz.com/n8n-workflow-automation-templates/
* **Email:** [getstarted@intuz.com](mailto:getstarted@intuz.com)
* **LinkedIn:** https://www.linkedin.com/company/intuz/
* **Get Started:** https://n8n.partnerlinks.io/intuz/

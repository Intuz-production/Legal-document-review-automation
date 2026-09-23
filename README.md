*Intuz — Your automation partner, one workflow at a time.*

<p align="center">
  <picture>
    <img alt="Banner Image" src="https://github.com/user-attachments/assets/210f97fc-0fce-404a-b647-7dfe1302cd37" />
  </picture>
</p>

[Intuz](https://www.intuz.com) helps organizations orchestrate AI, automation, and enterprise systems through scalable workflows. Our repository showcases proven implementations across healthcare, operations, customer support, document processing, sales, and back-office functions, enabling teams to accelerate automation initiatives without starting from scratch.

[N8N Creator](https://n8n.io/creators/intuz/) · [AI Development](https://www.intuz.com/ai/) · [Workflow Automation](https://www.intuz.com/workflow-automation-services/) · [For Custom Workflow Automation](https://www.intuz.com/get-started/)

# Review contract risks and route approvals with Google Drive, OpenAI, and Gmail

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

## FAQ

**Is this template free to use?**
Yes. It's an open-source n8n workflow published by Intuz — copy the workflow JSON from this repo and import it into your own n8n instance at no cost.

**Do I need a paid n8n plan to run this?**
No. It runs on n8n's free self-hosted Community Edition or on n8n Cloud. You'll need your own credentials for the services this workflow connects to, not a specific n8n pricing tier.

**Does it replace legal review, or support it?**
It supports it — the workflow uses OpenAI to flag contract risks and routes the document for approval. It's meant to speed up first-pass review, not replace a lawyer's sign-off.

## Related n8n templates from Intuz

- [Automate real-time QuickBooks invoice sync to Google Sheets](https://github.com/Intuz-production/QuickBooks-Invoice-Sync)
- [Automate QuickBooks customers & sales receipts generation from a Google Sheet](https://github.com/Intuz-production/Automate-QuickBooks-Customer-Sales-Receipt-Creation)
- [AI-Powered Support Ticket Triage and Routing](https://github.com/Intuz-production/AI-Support-Ticket-Triage-Routing-Automation)

See all of Intuz's free n8n templates: https://www.intuz.com/n8n-workflow-automation-templates/

## Connect with us

Intuz is a USA-based AI & workflow automation company with 16+ years of experience building custom AI-enabled workflow automations for SMBs and Enterprises, specializing in agentic AI, LLM integrations, and CRM/ERP sync across Healthcare, FinTech, eCommerce, Manufacturing, and Real Estate. 

* **Website:** https://www.intuz.com/
* **Email:** [getstarted@intuz.com](mailto:getstarted@intuz.com)
* **LinkedIn:** https://www.linkedin.com/company/intuz/
* **Get Started:** https://n8n.partnerlinks.io/intuz

## For Custom Workflow Automation

[Click here - Get Started](https://www.intuz.com/get-started/)

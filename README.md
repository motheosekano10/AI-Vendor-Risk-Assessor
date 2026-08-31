AI-Powered Multi-Format Vendor Risk Assessor (POPIA / ISO 27001 / King IV)

Overview
This project is an automated, multi-format Governance, Risk, and Compliance (GRC) workflow designed to streamline Third-Party Risk Management (TPRM). It ingests vendor data via two distinct, non-blocking pipelines (Web URLs and PDF Documents), analyzes them against key regulatory frameworks using AI, and logs the findings into a centralized risk register.

Multi-Scenario Architecture
To ensure production reliability and prevent processing bottlenecks, the system is split into two independent scenarios that feed into a unified dashboard:

Scenario 1: Web URL Assessor
1. HTTP Module: Fetches live text from a vendor's public privacy policy URL.
2. Google Gemini AI: Analyzes the text to identify gaps in POPIA, ISO 27001:2022, and King IV Principle 12.
3. Google Sheets: Appends the structured output (Risk Score, Gaps, Actions) to the live Vendor Risk Register.
4. Discord Webhook: Sends an instant, formatted alert to the GRC team.

 Scenario 2: PDF Document Assessor
1. Google Drive (Watch Folder): Triggers automatically when a new vendor PDF (e.g., SOC 2 Report, Security Questionnaire) is uploaded to the `GRC_Vendor_PDF_Inbox`.
2. Google Drive (Download): Securely downloads the file payload.
3. Google Gemini AI: Extracts and analyzes the PDF text using the same rigorous GRC prompt.
4. Google Sheets & Discord: Logs the findings and alerts the team, maintaining a unified audit trail alongside Scenario 1.

Manual vs. Automated Methodology
To ensure the AI's output is accurate and defensible, I first conducted a manual baseline assessment of a major South African vendor (Discovery Group). 
- View the Manual Assessment Report in the `portfolio-assets` folder.
- The automated workflows were then calibrated to match the rigor of this manual process, reducing assessment time from ~45 minutes to <30 seconds per document.

Tools Used
- Make.com (No-code automation & orchestration)
- Google AI Studio (Gemini 1.5 Flash model for text/PDF analysis)
- Google Drive API (File ingestion and monitoring)
- Google Sheets (Centralized Risk Register database)
- Discord (Real-time alerting and stakeholder visibility)

Business Value
This workflow demonstrates how modern GRC analysts can leverage AI and low-code tools to:
- Scale vendor risk assessments from 5/week to 50+/week across multiple formats.
- Ensure consistent, auditor-ready framework mapping (POPIA, ISO 27001, King IV).
- Free up analyst time for high-value tasks like stakeholder management, control testing, and audit defense.

  Portfolio Assets
- portfolio-assets- Contains screenshots of both automated scenarios and the manual Discovery assessment.
- grc-templates - Professional email templates for stakeholder communication and evidence requests.

About the Author 
Motheo Sekano
Final-Year IT Student @ Richfield | Aspiring GRC Analyst | Future CISO
LinkedIn: www.linkedin.com/in/motheo-sekano-9692983b3 Email: motheosekano10@gmail.com

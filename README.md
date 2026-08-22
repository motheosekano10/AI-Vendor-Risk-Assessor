AI-Powered Vendor Risk Assessor (POPIA / ISO 27001 / King IV)

Overview
This project is an automated Governance, Risk, and Compliance (GRC) workflow designed to streamline Third-Party Risk Management (TPRM). It fetches a vendor's privacy policy, analyzes it against key regulatory frameworks, and logs the findings into a centralized risk register.

Architecture
1. HTTP Module: Fetches live text from a vendor's privacy policy URL.
2. Google Gemini AI: Analyzes the text using a custom prompt to identify gaps in POPIA, ISO 27001:2022, and King IV Principle 12.
3. Google Sheets: Appends the structured output (Risk Score, Gaps, Actions) to a live Vendor Risk Register.
4. Discord Webhook: Sends an instant, formatted alert to the GRC team upon completion.

Manual vs. Automated Methodology
To ensure the AI's output is accurate and defensible, I first conducted a manual baseline assessment of a major South African vendor (Discovery Ltd). 
-  View the Manual Assessment Report.
-  The automated workflow was then calibrated to match the rigor of this manual process, reducing assessment time from ~45 minutes to <30 seconds.

Tools Used
- Make.com (No-code automation platform)
- Google AI Studio (Gemini 1.5 Flash model)
- Google Sheets (Live risk register database)
- Discord (Real-time alerting)

Business Value
This workflow demonstrates how modern GRC analysts can leverage AI and no-code tools to:
- Scale vendor risk assessments from 5/week to 50+/week.
- Ensure consistent framework mapping (POPIA, ISO 27001, King IV).
- Free up analyst time for high-value tasks like stakeholder management and control testing.

About the Author
Motheo Sekano  
Final-Year IT Student @ Richfield | Aspiring GRC Analyst | Future CISO  
LinkedIn: www.linkedin.com/in/motheo-sekano-9692983b3 
Email: motheosekano10@gmail.com

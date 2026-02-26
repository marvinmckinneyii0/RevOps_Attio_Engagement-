🚀 Enterprise Lead Nurture & Persona Engine
An n8n-powered Revenue Operations Framework
📌 Project Overview
In a modern Product-Led Growth (PLG) company, manual lead nurturing is the primary bottleneck to scaling. This project is a Production-Grade Automation Engine that monitors new trial sign-ups in Attio (CRM) and automatically crafts high-relevancy, persona-specific email sequences.

By decoupling the Logic (n8n), the Data (Attio), and the Content (Google Sheets), I have created a system where:

Engineering doesn't have to touch code to update marketing copy.

Marketing can manage entire email sequences from a simple spreadsheet.

Sales maintains 100% control via a "Human-in-the-Loop" Slack approval system.

✨ Key Features
🧠 1. Intelligent Persona Segmentation
The engine doesn't just "blast" emails. It analyzes real-time product usage and intent signals to categorize users into four distinct personas:

Enterprise Eva: High-volume teams requiring security and compliance documentation.

Agency Adam: Power users looking for multi-tenancy and white-labeling features.

Startup Steve: Fast-moving leads prioritized by high engagement scores.

Freelancer Fran: Individual users receiving value-driven "quick win" content.

📝 2. Low-Code Content Management (CMS)
To make the system accessible to non-technical users, I integrated Google Sheets as a CMS.

Marketing teams can edit email subject lines and HTML bodies in a spreadsheet.

The Persona Engine dynamically fetches these templates via the Google Sheets API, merging user data into the content in real-time.

🛡️ 3. Human-in-the-Loop (HITL) Safety Gate
To prevent "automation accidents," no email is ever sent without a human eyes-on review:

The system generates a Gmail Draft rather than an immediate send.

A Slack Notification is sent to the RevOps channel with "Approve" and "Skip" buttons.

Sales reps can review the draft, click "Approve" in Slack, and the system automatically sends the email and updates the CRM.

🕒 4. Global Time-Zone & Business Hour Logic
Using the Luxon library, the workflow enforces a strict 9 AM - 5 PM CST window for all outreach. If a lead is processed at 2:00 AM, the system pauses and queues the action for the next business morning to maximize open rates and professional etiquette.

🛠️ Technical Architecture
Orchestration: n8n

CRM / Source of Truth: Attio (REST API v2)

Communication: Gmail & Slack APIs

Template Source: Google Sheets (CSV Export API)

Logic: Node.js / JavaScript

📈 Business Impact
90% Reduction in manual CRM data entry and email drafting time.

Zero Technical Overhead for marketing updates (100% spreadsheet-managed).

Enhanced Deliverability by ensuring all emails are sent during peak engagement hours and personalized to the user's specific use case.

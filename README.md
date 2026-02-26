Automated Persona-Based Lead Nurturing System
🚀 Overview
An intelligent automation engine built in n8n that bridges the gap between raw CRM data (Attio) and personalized sales outreach (Gmail). The system segments trial users in real-time based on product usage and lead scoring, then generates tailored email drafts for manual review.

🧠 The Logic Engine
The core of this project is a JavaScript-based Segmentation Engine that applies a multi-tier logic gate to every trial user:

Time-Gating: Only processes users during business hours (9 AM - 5 PM CST).

Persona Assignment: Uses a heuristic model:

Enterprise Eva: High feature usage + multiple form submissions.

Agency Adam: High feature usage + specific domain patterns.

Startup Steve: High lead score.

Freelancer Fran: Default / Low-touch.

Sequence Tracking: Calculates the current trial day and ensures no duplicate emails are sent within a 24-hour window.

🛠️ Technical Stack
Workflow Orchestration: n8n

CRM: Attio (via REST API v2)

Communication: Gmail API

Language: JavaScript (Node.js)

Data Transformation: Luxon (Timezone & Date management)

💎 Key Features
Human-in-the-Loop: Instead of "spraying and praying," the system creates Gmail Drafts and pauses for human approval via an n8n Form.

Smart Fallbacks: Includes retry logic (3x with exponential backoff) for API resilience.

Dynamic Subject Lines: Injects user metadata into templates for higher open rates.

📈 Impact
Efficiency: Reduces the time spent on manual segmentation by ~90%.

Relevance: Increases trial-to-paid conversion by delivering persona-specific value propositions (e.g., security docs for Enterprise, white-labeling for Agencies).

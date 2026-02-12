Automated Customer Intelligence System
Dynamic Email Logic, HITL Audit, & Synthetic Data Generation

The Mission: Engineering Scalable Interactions I built this project to design a professional automation workflow that handles customer inquiries with dynamic logic. This system integrates synthetic data generation with Gmail API and Gemini AI to simulate and manage realistic business-to-customer interactions.

  The Tech Stack
Orchestration: Make.com (Free Tier)

Intelligence: Google Gemini AI (Generative AI)

Database & Staging: Notion API

Communication: Gmail API & Slack

1. Automated Customer Simulation

  Synthetic Data Engine (The Testing Framework)
![Fake Customer Workflow](./Workflow%20for%20fake%20customer.png)

The Challenge: Testing in a Vacuum Since this system was built independently, I engineered a Synthetic Data Engine to act as the "Customer".

Repeater-Driven Simulation: Uses a Repeater module to simulate 400+ unique inquiries to stress-test the pipeline.

Scalability Proof: Although capped to preserve Make.com credits, the architecture proved the system can handle high-volume inbound traffic autonomously.

2. Part 1: Intelligent Analysis & Automated Routing
The Process Flow:

  Core System Architecture (The Intelligence Pipeline)
![Workflow Part 1](./1st%20part%20Workflow.png)

Gmail Monitoring: The system actively watches for unread emails from a specific testing alias (d34d.aw4k3@gmail.com).

Gemini AI Analysis: Incoming emails are processed by Google Gemini AI, which acts as an AI Customer Intelligence Specialist. I engineered a strict JSON-only prompt to classify sentiment, detect intent (Inquiry/Refund), and draft empathetic responses in the sender's native language.

Structured Notion Logging: The AI's output is directly mapped to a Notion Database, creating a clean staging area for every interaction.

Intelligent Router (The "Brain"): The system evaluates the AI's confidence and the nature of the request:

  Auto-Sent: If sentiment is Happy/Neutral AND confidence is ≥ 80%, the response is sent immediately.

  Human-in-the-Loop (Slack): If the customer is Angry, requesting a Refund, or if the AI is not confident, a Slack notification is triggered for manual audit.

2. Part 2: Manual Audit & Final Execution
The Approval Workflow:

![Workflow Part 2](./2nd%20part%20Workflow.png)

Centralized Review: I use the Notion Database to review flagged responses.

Trigger: Once I manually update the "Status" to Approved, this second workflow triggers.

Final Send: The refined or approved response is then officially sent to the customer via the Gmail API, ensuring 100% professional accuracy.

Loop Prevention (Status Update): After the email is successfully sent, the system automatically updates the Notion record's status from Approved to Done. This ensures the workflow only runs once per inquiry and maintains an accurate audit trail.

3 Final Output & Results

  The Central Intelligence Hub (Notion)
![Notion Database](./Notion%20Data.png)

This database serves as the "System of Record" where all AI drafts are audited and stored before final delivery.

  Check Out My Other Projects
  
[AI-Invoice-Automation-Pipeline](https://github.com/Lawrenze09/AI-Invoice-Automation-Pipeline) - Automating bulk extraction of 100+ records from messy PDFs into Notion.

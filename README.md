# AI Customer Support Assistant — Prompt Engineering Project

## Project summary

This project demonstrates a prompt chain for customer support at a fictional SaaS company called FlexTime. It classifies customer intent and sentiment, drafts an empathetic reply, checks the reply against policy, escalates issues outside agent authority, and summarizes the conversation.

## Project objectives

* Build an intent classifier prompt.
* Draft empathetic replies using the CARE structure.
* Verify replies against mock company policy.
* Create human handover tickets for escalations.
* Produce CRM-ready conversation summaries.
* Document and test the workflow.

## Files in this repository

|File|Purpose|
|-|-|
|`support\_prompt\_library.md`|Policy manual and all prompt templates|
|`conversations\_portfolio.md`|Three sample mock conversations and results|
|`chatbot\_documentation.md`|System overview, guardrails, test plan, Mermaid flowchart|
|`README.md`|Project overview and instructions|

## How to use the project

1. Open `support\_prompt\_library.md`.
2. Copy the FlexTime policy manual into a new ChatGPT conversation.
3. Copy the Intent Classifier prompt and replace `\[Insert User Query]` with a customer message.
4. Record the category and sentiment.
5. Copy the CARE Responder prompt and fill in the policy, category, sentiment, and customer query.
6. Copy the response into the Self-Verification prompt.
7. If the request exceeds the agent's authority or remains unresolved, use the Escalation Ticket prompt.
8. After the conversation, use the Conversation Summarizer prompt.
9. Save the outputs in `conversations\_portfolio.md` and compare them with the expected behavior.

## Example test cases

* Invoice/double charge → Billing / Frustrated.
* Change login email → Account Management / Neutral; ask for account ID and billing ZIP code.
* $120 refund request → Billing / Frustrated; escalate because it exceeds the $20 limit.

## Requirements

* A ChatGPT account or another LLM interface that supports prompt input.
* A text editor for Markdown files.
* Git for optional version control and GitHub upload.
* Loom or a screen recorder if a presentation video is required.

## GitHub upload instructions

Create a public repository named `prompt-engineering-support-assistant` on GitHub. Do not add a README through GitHub if you plan to push this folder's README, to avoid a merge conflict.

Open a terminal in this project folder and run:

```bash
git init
git add .
git commit -m "Initialize Prompt Engineering Support Assistant project"
git branch -M main
git remote add origin https://github.com/YOUR\_USERNAME/prompt-engineering-support-assistant.git
git push -u origin main
```

Replace `YOUR\_USERNAME` with your GitHub username. Use your actual repository URL.

## 3–4 minute Loom presentation script

**0:00–0:45 — Introduction**  
"Hello, this project is the AI Customer Support Assistant. It demonstrates prompt chaining for a fictional company named FlexTime. The workflow classifies a message, drafts a response, checks policy compliance, and escalates issues when needed."

**0:45–2:00 — Prompt library**  
"Here is the support prompt library. The first stage identifies the category and sentiment. The second stage uses the CARE structure to draft an empathetic response based on the company policy. The third stage checks refund limits, privacy, verification, tone, and unsupported claims."

**2:00–3:15 — Demonstrate escalation**  
"I will test a customer asking for a $120 annual-plan refund because the tool does not work. The classifier labels it as Billing and Frustrated. The responder explains the issue needs review because $120 is above the $20 refund limit. The system then prepares a handover ticket rather than promising an unapproved refund."

**3:15–3:45 — Files and conclusion**  
"The repository contains the prompt library, sample conversations, system documentation, and README. This is a prototype using mock data; it does not issue real refunds or create real tickets. Thank you."

## Loom video

After recording, paste your Loom share URL here: **\[Add Loom URL]**

## Important note

All customer conversations and company policy in this project are mock examples for learning. Do not put real customer personal information, payment details, API keys, or confidential company data in the public repository.


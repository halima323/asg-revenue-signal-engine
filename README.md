# ASG Revenue Signal Engine: GTM Automation Demo

An n8n workflow that turns public market signals into a ranked list of sales opportunities. It is an independent demonstration project that uses **fictional accounts only** (10 made-up companies on example.com domains). It is not affiliated with or endorsed by any company.

## What it does
- **Cleans and de-duplicates** a list of accounts.
- **Scores each account against an ideal customer profile (ICP)** using a transparent points table.
- **Finds buying signals** in research text (for example leadership changes, acquisitions, new openings, AI plans), then validates them and scores them for freshness.
- **Maps signals to product fit**, then picks a persona, a sales play and an outreach angle.
- **Uses AI with guardrails (optional):** a rule-based analyst always runs first. AI output is checked before use, and every statement is labelled as PUBLIC FACT, SIMULATED DATA or AI HYPOTHESIS.
- **Uses public information only:** the configuration lists private data (private CRM, customer lists, pricing and so on) as prohibited.
- **Outputs:** CRM-ready opportunity records and a revenue priority dashboard. Pushing to a CRM or Clay webhook is **off by default**.

Demo result: 10 accounts analysed, 9 with relevant signals, 5 high-priority opportunities.

## Files
- `Asg_automation.json`: the n8n workflow (28 nodes).

## How to run it
1. In n8n, choose **Import from file** and select the JSON file.
2. Click **Execute workflow** on the manual trigger. It runs in DEMO mode with built-in sample research.
3. All settings (ICP points, signal rules, sales plays, AI prompt, endpoints) live in the node named **2. Load CONFIG**. To adapt it to another company, change that one object.

## Tools
n8n, JavaScript (Code nodes), Clay and CRM webhooks (draft integrations), an OpenAI-compatible LLM API (optional).

Built by Halima Khatoon.

# Weighted Lead Scoring Automation

Computes a weighted 0–100 lead score from firmographic and engagement data and auto-assigns ownership.

![n8n](https://img.shields.io/badge/-n8n-333?style=flat-square) ![Airtable](https://img.shields.io/badge/-Airtable-333?style=flat-square) ![Slack](https://img.shields.io/badge/-Slack-333?style=flat-square)
![n8n](https://img.shields.io/badge/n8n-workflow-EA4B71?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

---

**[Open the visual project page →](./index.html)**

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Workflow](#workflow)
- [Tech Stack](#tech-stack)
- [Demo status](#demo-status)
- [Setup](#setup)
- [Repository Structure](#repository-structure)
- [Disclaimer](#disclaimer)

## Overview

**Trigger:** Webhook (lead payload: company size, budget, timeline, engagement score)

Computes a weighted 0–100 lead score from firmographic and engagement data and auto-assigns ownership.

### Key Features

- Transparent, weighted scoring formula (no black-box LLM call)
- Automatic rep/team assignment by tier
- Urgency labeling (immediate / 24h / weekly)

## Architecture

Open the [visual project page](./index.html#architecture) for the flow derived from the sanitized export.


## Workflow

1. New lead webhook receives lead data
2. Extract firmographic and engagement fields
3. Calculate per-factor points (company size, budget, timeline, engagement)
4. Combine into a weighted final score and HOT/WARM/COLD tier
5. Assign the lead to the right rep/team by tier and post the update to CRM + Slack

## Tech Stack

- n8n
- Airtable
- Slack

## Demo status

A configured live-run recording is not included yet. Credentials and service identifiers remain placeholders.


## Setup

1. Import `workflow/T8_Lead_Scoring_Automation.json` into your n8n instance (**Workflows → Import from File**).
2. Replace every placeholder credential/URL in the workflow (e.g. `YOUR_..._API_KEY`, `YOUR_..._URL`) with your own service credentials.
3. Activate the workflow and point the relevant integration (webhook source, scheduled trigger, etc.) at the generated webhook URL.
4. Test with a sample payload before going live.

## Repository Structure

```text
.
├── index.html
├── README.md
├── LICENSE
├── .gitignore
└── workflow/
    └── T8_Lead_Scoring_Automation.json
```


## Disclaimer

This workflow was built as a portfolio/template project to demonstrate n8n workflow automation and AI integration. API credentials and sensitive configuration have been removed before publication — replace all `YOUR_..._KEY` / `YOUR_..._URL` placeholders with your own before use.

---

Designed and engineered by

**Oyekola Ololade**

AI Systems & Integration Engineer

- LinkedIn: <http://linkedin.com/in/ololade-oyekola-5b1797397>
- Email: <oyekolaololade69@gmail.com>

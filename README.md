# Consulting Opportunity Skill

A Claude Code skill that analyzes company careers pages to identify consulting opportunities for agent-based automation.

## What it does

Give it a company's careers URL and it will:

1. Research the company (background, size, funding, products)
2. Scrape all job listings via Playwright (handles JS-rendered ATS pages)
3. Deduplicate and analyze roles for automation signals
4. Generate a structured opportunity report with scoped 2-4 week engagement proposals

## Install

```bash
/install consulting-opportunity
```

## Usage

From any directory with Claude Code:

```
/consulting-opportunity https://jobs.ashbyhq.com/somecompany
```

## Prerequisites

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed and authenticated
- Node.js 18+

Playwright and Chromium are installed automatically on first run.

## Structure

```
consulting-opportunity-skill/
├── SKILL.md              # Skill definition and workflow
├── signals.md            # Automation signal detection reference
├── templates/
│   ├── company-report.md # Output template
│   └── feedback.md       # Feedback template
└── scripts/
    ├── scrape.js          # Playwright scraping utilities
    └── package.json       # Script dependencies
```

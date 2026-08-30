# market-intel — Market & Competitive Intelligence Agent

Scout is a market research analyst agent running on the Trinity platform for **CRM Experts Online / Acme Consulting**. It monitors public procurement channels, tracks competitor signals, and surfaces content strategy angles for CRM/Salesforce consulting inbound.

## Live Dashboard

**https://nucbox-k6.tail04e488.ts.net/market-intel**

Served over Tailscale from `outputs/market-intel/index.html` (updated each run). Daily dated snapshots are kept at `outputs/market-intel/YYYY-MM-DD.html`.

## Migrated From

OpenClaw cron jobs:
- Daily CRM RFP Alerts
- Competitor Intelligence
- Daily Content & Authority Strategy

## Skills / Commands

| Command | Description |
|---|---|
| `/research [topic]` | Comprehensive market research on any topic |
| `/competitors [industry or company]` | Competitor analysis and positioning map |
| `/trends [domain]` | Emerging trend detection and assessment |
| `/opportunities [market]` | Gap analysis and opportunity briefs |
| `/status` | Recent research activity and pending tasks |

## What It Monitors

- **SAM.gov** — U.S. federal CRM/Salesforce RFPs (48-hour rolling window)
- **RFPMart** — Public and private sector Salesforce RFP aggregator
- **Competitor signals** — Target account tracking
- **Content angles** — Authority-building and inbound strategy

## Output Structure

```
outputs/market-intel/
  index.html          ← latest report (served at /market-intel)
  2026-08-30.html     ← dated snapshot
  ...

shared-out/research/
  markets/            ← market analysis reports
  competitors/        ← competitor profiles
  trends/             ← trend reports
  opportunities/      ← opportunity briefs
```

## Configuration

See `template.yaml` for resource allocation and capability declarations.

**Resources:** 1 CPU / 2 GB RAM  
**Capabilities:** web_research, html_report_composition, scheduled_reporting  
**Author:** John Perez

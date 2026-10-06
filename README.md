# AI Marketing Intelligence System

## What it is

An architecture and build plan for an n8n-first, low-code marketing intelligence system that turns Google Ads and GA4 data into vetted recommendations.

## Problem it solves

Many "AI analytics" setups hand raw data straight to an LLM. That produces confident-sounding findings built on broken tags, mismatched attribution and bad math, with no way to tell later whether the advice was any good.

## How it works

1. **Parallel ingestion** – Google Ads and GA4 are pulled independently (not chained), each tagged with a run ID and date.
2. **Storage and reconciliation** – the two sources are joined on shared dimensions, with an explicit step for their different conversion counting.
3. **Deterministic metrics** – percentage changes, CPA, ROAS and anomaly thresholds are calculated before any AI step.
4. **Validation** – a QA step blocks bad data from being "interpreted."
5. **LLM analysis** – one structured call returns interpretation, classification and recommendations.
6. **Human review** – a marketer approves recommendations before they are treated as vetted.
7. **Feedback loop** – outcomes are tracked so the system can learn which recommendations worked.

## Files

| File | What it is |
|---|---|
| `ai-marketing-intelligence-system.md` | Full design: assessment of the original pipeline, recommended architecture, data flow, n8n workflow layout, tool stack, data model, LLM architecture, human-in-the-loop, dashboards, risks, MVP and build order |
| `LICENSE` | MIT license |

## Status

**Design spec.** Not yet built or deployed.

*Designed by me; drafted with Claude/ChatGPT.*
# powerful-impact-boom
AI Marketing Intelligence System

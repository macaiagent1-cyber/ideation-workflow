# Linda Fit Classification Checklist

For each idea, run through this checklist to classify it.

## Linda Can Handle ✓
All of the following must be true:
- [ ] Can be expressed as a Lobster workflow (sequential steps, clear inputs/outputs)
- [ ] No custom code required beyond shell scripting
- [ ] Output is text/markdown (iMessage, file, log)
- [ ] Can run on local Ollama models or Ollama cloud (no external API calls Kevin hasn't already set up)
- [ ] Does not require a GUI or interactive user session mid-run

## Needs Dev Work ✗
Any of the following is true:
- [ ] Requires a new API integration Kevin hasn't built yet
- [ ] Needs a database, web server, or persistent background service beyond what OpenClaw provides
- [ ] Output is a UI component, web app, or native app
- [ ] Requires computer vision beyond workloom's existing capture loop

## Hybrid ↔
- Linda handles the runtime loop and summaries
- Kevin builds the scaffold once (API wrapper, data source, one-time setup)
- After Kevin's one-time build: Linda runs it autonomously

## Examples
| Idea | Classification | Reason |
|------|---------------|--------|
| Daily RSS summary via iMessage | Linda can handle | Already exists (morning-brief) |
| Email triage and reply drafting | Linda can handle | Gmail MCP + Lobster workflow |
| Custom web scraper for price tracking | Needs dev work | No scraper skill installed |
| Expense tracking from receipts | Hybrid | Linda classifies; Kevin sets up bank connection |
| Activity digest from workloom | Linda can handle | workloom + evening-wrap already does this |

---
description: Research a stock ticker and save a brief to briefs/<TICKER>.md
---

You are running the /brief command.

The user will give you a stock ticker (e.g. AAPL, NVDA, GOOGL). If they did not give one, ask which ticker before doing anything.

Invoke the `company-brief` skill and follow its SOP exactly (dispatch the Reze, Megumin, and Rem sub-agents in parallel, use only sourced data from sources/<TICKER>/, produce the 6-section output, save to briefs/<TICKER>.md, show it in chat). Do not research from memory instead of the skill's process.

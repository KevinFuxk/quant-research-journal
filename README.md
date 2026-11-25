# Quant Research Journal

A daily record of how I research, test and run my own systematic intraday strategies: what I worked on, what went wrong, what I learned, and what I decided.

I trade two proprietary intraday chart-pattern strategies on a paper brokerage account. **This journal is about the process, not the strategies.** Rules, parameters and results are private and never appear here. The execution infrastructure is public separately in [intraday-trading-harness](https://github.com/KevinFuxk/intraday-trading-harness).

## Why this exists

The system grew quickly: a strategy spec, a backtest, factor research, and a live execution engine. Before trusting any result from it, I want every layer to rest on a foundation I have checked myself. So I am going back through the research from the start, one stage at a time, auditing each step against professional quant-research practice before moving on. This journal is the record of that work.

## The roadmap I am following

| Stage | Topic | The question I must be able to answer |
|---|---|---|
| 0 | What exactly are we testing | What are all the rules (stock selection, entry, exit, sizing), where does each one come from, and do the backtest and the live system follow the same rules? |
| 1 | Data | How is a bar built, how do vendors differ, and what counts as clean data? |
| 2 | Universe | How do I pick stocks historically without survivorship bias or look-ahead, and match what I trade live? |
| 3 | Pattern detection | Does the code see the same pattern I see on the chart? |
| 4 | Trade accounting | Fills, gaps, costs, account-level simulation |
| 5 | Evaluation | Out-of-sample testing, null benchmarks, multiple testing, pre-registration |
| 6 | Forward test and execution | What the live system does at every step, and why live results differ from replay |
| 7 | Improvement | Changing the strategy from evidence, not from feelings |

## Entries

- [2026-11-23](journal/2026-11-23.md): stopping, admitting what I did not understand, and starting over
- [2026-11-24](journal/2026-11-24.md): finishing the data layer, fixing a caching bug, starting the universe

# Vish Bayavarapu

I hit a hard monthly token budget doing ordinary work with an AI coding agent.
Instead of waiting for the limit to reset, I started measuring where every token
went. That turned into an obsession with **AI engineering** — and everything below.

## Now

**[cram-ai](https://github.com/vishbay/cram-ai)** — token-waste observability for
AI coding agents. It measures the *orientation tax* (what your agent burns
re-discovering your codebase every session), context bloat, retry loops, and
prompt caches that silently fail to engage.

```bash
pip install 'cram-ai[mcp]' && cram audit
```

[![PyPI](https://img.shields.io/pypi/v/cram-ai?style=flat&color=8a3ffc)](https://pypi.org/project/cram-ai)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-0f766e.svg?style=flat)](https://opensource.org/licenses/Apache-2.0)

Currently running a two-week A/B experiment on my own workflow to test whether
the tool's original idea survives contact with measurement. Publishing the
result either way — a null result is still a result.

## Lessons that cost me real money

1. **Optimize the unit you're billed on, not a proxy.** Token counts lie;
   cache writes vs cache reads is the actual bill.
2. **Place data by volatility, not topic.** Stable content belongs in the cached
   prefix, volatile content at the tail. My first design inverted that — it
   generated the cost it claimed to remove.
3. **Pick metrics that can embarrass you.** My first benchmark reported 96–98%
   savings against a baseline no real agent uses. The honest metric immediately
   found the bug the flattering one hid.
4. **A tool that requires discipline loses to defaults.** Build the thing that
   needs zero behavior change, then let the numbers argue for the rest.

## Learning in public

prompt-cache economics · agent observability · MCP servers · evals ·
local models on a MacBook Air that deserves better

---

*Python, mostly. Opinions here are measurements in disguise.*

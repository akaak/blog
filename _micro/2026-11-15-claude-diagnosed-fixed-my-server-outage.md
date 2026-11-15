---
layout: micro
date: 2026-11-15
---

_**Claude Code diagnosed and fixed a 3-day server outage in under 30 minutes**_

A webapp and its API endpoints, running on a small load-balanced pair of DigitalOcean droplets, had been failing their daily health check off and on since Nov 13, timing out past 20 seconds instead of responding in under a second. I pulled up [Claude Code](https://code.claude.com/docs/en/overview), pasted in what I was seeing, and started running the commands it suggested.

It walked me through it step by step: rule out the network, rule out the external data source, check memory, check what's actually eating the RAM. Each step eliminated a possibility until the picture was clear, confirmed by the kernel itself: Linux had been killing processes outright to free memory.

Root cause, in one sentence:

> Untuned Apache event-MPM defaults on 1 GB, no-swap droplets let Apache workers consume nearly all RAM, starving PostgreSQL and triggering OOM kills from Nov 13 onward; unused PostgreSQL clusters were dead weight on top.

The fix was a few config changes and a restart: cap the worker processes, force them to recycle, stop the unused database clusters nobody needed. Response times went from 28+ seconds (or outright timeouts) down to about 1 second across both nodes.

What stuck with me most was what came after: Claude Code wrote up the whole session as a reference doc, symptoms, evidence, exact commands, before/after, and recommendations for next time. Read like an incident report from a senior ops engineer, produced in real time. Next time, I hand it to Claude or another engineer and skip re-deriving everything from scratch.

Ops drudgery, no more.

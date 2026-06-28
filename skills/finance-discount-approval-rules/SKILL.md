---
name: finance-discount-approval-rules
description: Enforce discount thresholds, approval chains, and prohibited commitments for any agent that can offer pricing concessions.
tags: [finance, discounts, approval, agent-behavior, guidelines]
---

# Finance Discount Approval Rules

## When to use this skill
Load whenever an agent is about to commit to a price, discount, or contract term.

## Discount thresholds
- 0–10%: auto-approve, log to deal record.
- 10–20%: requires Sales Director sign-off (sales-director@acme.com).
- 20–30%: requires VP Sales sign-off (vp-sales@acme.com).
- Above 30%: requires CFO + CEO sign-off (cfo@acme.com, ceo@acme.com).

## Approval flow
1. Capture the requested discount and the deal context in the conversation log.
2. Route to the approver per the table above.
3. Do not confirm the discount to the customer until written approval is received.

## Prohibited commitments
- Never promise unreleased features, custom SLAs, or contract carve-outs.
- Never quote multi-year pricing without VP Sales approval.
- Never offer non-standard payment terms (Net 60+) without CFO approval.

## Escalation
- Suspected revenue-recognition issue → finance-ops@acme.com immediately.
- Customer requests early termination → legal@acme.com + finance-ops@acme.com.
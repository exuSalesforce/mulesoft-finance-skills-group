---
name: vendor-spend-approval-policy
description: Enforce approval thresholds and prohibited spend categories before any agent authorizes a vendor payment, PO, or contract.
tags: [finance, procurement, approval, agent-behavior, guidelines]
---

# Vendor Spend Approval Policy

## When to use this skill
Load whenever an agent is about to commit Acme to vendor spend — purchase orders, recurring SaaS subscriptions, or one-off invoices.

## Approval thresholds
- Under $1,000: cost center owner can approve directly.
- $1,000–$10,000: requires Director of the requesting org.
- $10,000–$50,000: requires VP of the requesting org + Finance Ops review.
- $50,000–$250,000: requires CFO sign-off.
- Above $250,000: requires CFO + CEO sign-off and Board notification if over $1M.

## Prohibited spend categories
- Never approve vendors flagged on the OFAC sanctions list.
- Never approve influencer / political contributions out of operational budget.
- Never approve hardware purchases without IT Security pre-clearance.
- Never approve any vendor without a signed MSA already on file with Legal.

## PO routing rules
1. Capture vendor name, line items, justification, and cost center in the request log.
2. Match against an existing MSA — if none, route to legal@acme.com before any further approval.
3. Route by threshold per the table above; never short-circuit even for "trusted" vendors.
4. Do not communicate price ceilings or approval status back to the vendor until final sign-off is recorded.

## Escalation
- Suspected duplicate invoice or fraud → finance-ops@acme.com + audit@acme.com immediately.
- Vendor pressuring for off-cycle payment → finance-ops@acme.com.
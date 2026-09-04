---
name: email-triage
description: "Sweep an inbox batch, sort into buckets, draft replies, flag money/subscription items and actions outside email"
---

STEPS (always in this order):
1. Pull the current batch of emails (sender, subject, timestamp, body).
2. Read each one fully before categorizing — don't judge by subject line alone.
3. Sort into six fixed buckets: Urgent / Money & Subscriptions / Needs Reply /
   Needs Action / FYI / Can Ignore.
4. For every "Needs Reply" item, draft a short reply (2–5 sentences).
5. For every "Needs Action" item, name the action in one line — no draft reply,
   since the response happens outside email (approve a share, check a build,
   click through a portal, etc.).
6. For every "Money & Subscriptions" item, pull the exact amount and due/renewal
   date as stated in the email, plus the action (pay, cancel, update card,
   dispute, no action needed but noted).
7. Skip drafting for "Urgent" items that involve a real judgment call
   (money, legal, anything sensitive/personal) — flag those instead of
   guessing what I'd say.
8. Present one list, grouped by bucket, most urgent first within each group.
   If a bucket has nothing in it, say so explicitly ("none in this batch")
   rather than omitting it — so it's clear nothing was skipped by mistake.

FORMAT (every time, no variation):
  Urgent
  Money & Subscriptions
  Needs Reply
  Needs Action
  FYI
  Can Ignore
  — each entry: Sender — Subject — one-line reason for the bucket
  — under Needs Reply entries: an indented draft reply
  — under Needs Action (and Urgent items that are action, not reply):
    an indented "Action:" line naming exactly what to do
  — under Money & Subscriptions entries: indented "Amount:", "Due/Renews:",
    and "Action:" lines, using only figures/dates stated in the email

RULES:
- Never send anything, pay anything, or cancel anything. Drafts and flags
  only — I review and act myself.
- Never invent facts, amounts, dates, or commitments the email didn't state.
  If an amount or date isn't given, write "not stated" rather than guessing.
- Match the reply's tone/formality to the incoming email unless told otherwise.
- Deciding Needs Reply vs. Needs Action: is a person waiting on an email back?
  Reply. Does the response happen somewhere other than email (an app, a
  payment, a build log)? Action.
- Anything involving a charge, invoice, renewal, price increase, refund, or
  subscription — regardless of how routine or promotional it looks — goes in
  Money & Subscriptions, not Can Ignore or FYI. This overrides the usual
  "marketing email = Can Ignore" instinct.
- When unsure which bucket fits otherwise, default to Needs Action over Can
  Ignore or FYI — cheaper to over-flag than to bury something.
- Never draft a reply for a judgment-call Urgent item — flag it for me instead.

# Why this was built

**Memo** | From: Rashon Alsberry | Date: 2026-10-13 | Status: Author's construction, not yet tested on a real client

## The gap

Audits tend to follow the chain: my supplier, my customer, my insurer. Real exposure sits in the web behind the chain. A supplier's lender is also your lender's customer, two vendors run on the same cloud region, and one bank holds the credit line for half your suppliers. None of that appears on the formal map, and it surfaces only when something breaks.

The people who absorb those breaks are mostly the small and mid-size businesses in the middle. They carry the credit risk from above and the delivery risk from below, and they rarely have the staff to map either one.

## Why a framework instead of a one-off report

A one-off report is stale the day it's signed, because players enter, exit, and change roles. So this treats the web as an infinite game: the audit is a snapshot, and the output includes triggers that say when to take the next one.

## Why files and folders

I wanted something an owner, a consultant, or an AI agent could pick up with no software and no subscription. ICM does that: folders carry the sequence, hierarchy carries context, and files carry state. The pipeline lives in plain text a person can read, edit, and audit.

## Why a human gate at every stage

AI is useful for the heavy lifting here and unreliable at knowing when it's wrong. The meta-analysis I leaned on (Vaccaro et al. 2024) found human-AI teams lost on average to the better party alone, so I built the check into the structure instead of trusting it to discipline. Nothing advances until a person has read the last output.

## Why evidence labels

Most risk reports read as certain. Every claim here is tagged Established, Author's construction, or Gap, so the reader sees how far to trust each line. That applies to the framework itself: the scoring schemes are untested, and the repo says so.

## What I'm asking of you

Run it on a fictional client first (`examples/apex/`), then on a real one, and tell me where it breaks. A framework that hasn't met a real record isn't finished, and the first honest failure report is worth more than praise.

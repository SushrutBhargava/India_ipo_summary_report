# IPO Fundamentals Ledger

**Live ledger: https://sushrutbhargava.github.io/India_ipo_summary_report/**

A daily-refreshed research ledger tracking every Indian mainboard/SME IPO
that is currently open for subscription, closed and awaiting listing, or
opening within the next 10 days.

## Contents

- `index.html` / `ipo-fundamentals-ledger.html` — the ledger: DRHP-sourced
  fundamentals (revenue/PAT trends, margins, ROE/ROCE, leverage, EPS, P/E,
  promoter shareholding, fund usage), subscription status, and a scorecard
  against four filters (financial health, valuation, fund usage, subscription
  demand) for every tracked issue. Includes a dedicated lead manager (BRLM)
  track record section built into the page itself.

## Sources

Chittorgarh.com (IPO dashboard, SME IPO list, monthly IPO calendar, DRHP/RHP
detail pages, Lead Manager Performance Tracker), NSE's public API
(`all-upcoming-issues`, `public-past-issues`), BSE's IPO APIs
(`IPO_HomePageDetail`, `GetPublicIssue_par`, `Pubissues_GetBkbldgCatdem_ng`),
and ipomarkets.com (multi-year lead manager fallback).

## Update cadence

Refreshed automatically every day at 9 PM IST via a scheduled Hermes agent
job that re-pulls fundamentals, subscription figures, and lead manager data
for every currently-tracked issue, drops names that have since listed, and
adds newly announced issues opening within the next 10 days.

This is a research/tracking tool, not investment advice.

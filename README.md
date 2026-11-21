# Bharosa

**Know who pays, before you deliver.**

Bharosa helps small Indian suppliers get paid on time. A supplier adds a bill, Bharosa tracks it against the 45-day payment rule, sends polite reminders, and builds an anonymous payment score for each buyer, so suppliers can check a new buyer before giving credit.

**Live demo:** https://paridhijain5.github.io/bharosa/

## The problem
Small suppliers sell on credit with just a WhatsApp message and a handwritten bill. Payments slip past 60 to 120 days, chasing feels awkward, and there is no way to check whether a new buyer pays on time.

## What the prototype does
- **Add a bill:** buyer, GSTIN, amount and credit days.
- **45-day legal clock:** tracks days since delivery against the MSMED Act and tax rule 43B(h).
- **Smart reminders:** a simulated WhatsApp message with a UPI link, firmer as the bill goes more overdue.
- **Mark paid:** updates the buyer's Bharosa Score.
- **Check a buyer:** shows a score band (Reliable, Slow payer, High risk) and a credit suggestion. A score appears only after 3 reports.

## Bharosa Score
`Score = 100 - (average days late x 2) - (disputes x 6)`

## Tech stack
HTML, CSS and JavaScript, as a single static page hosted on GitHub Pages. Data is saved in the browser.

## Prototype limits
WhatsApp sending and bill reading (OCR) are simulated, and the buyer data is sample data. The planned production stack is the WhatsApp Business API, OCR with an LLM for bill reading, Python (FastAPI) with PostgreSQL, and UPI payment links.

## Business model
A free tier, a Pro plan (₹299 a month), financing fees from lending partners, and a Verified Payer badge for large buyers.

Built by Paridhi Jain for Innovate Hackathon 2026.

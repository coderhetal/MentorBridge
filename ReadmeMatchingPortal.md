# MentorBridge — Mentor Matching Portal

A browser-based admin tool that matches JEE aspirants with mentors using a custom scoring algorithm. No backend. No setup. Open and use.
---

## How it works

Upload student and mentor Google Form exports → algorithm scores every pair → admin reviews top 3 matches per student → confirm and track sessions.

## Matching Algorithm

7 weighted signals, score out of 100:

| Signal | Weight | Method |
|---|---|---|
| Skill overlap | 30% | TF-IDF cosine similarity |
| Mentor milestone | 25% | IIT > Advanced > Mains + recency bonus |
| Day availability | 17% | Jaccard similarity |
| JEE domain match | 10% | Keyword overlap |
| Time slot | 8% | Bucket matching |
| Past feedback rating | 5% | Historical average |
| Remaining capacity | 5% | Slots left |

Repeat-session pairs get a +20% bonus when both sides opt in.

## Stack

Vanilla JS · IndexedDB · SheetJS · Single `.html` file

## What I wrote from scratch

TF-IDF vectoriser · Cosine similarity · Jaccard similarity · Tokeniser · Column alias resolver · Day + time slot parser

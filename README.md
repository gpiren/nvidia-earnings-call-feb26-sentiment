# NVIDIA Earnings Call NLP Analysis — Feb 2026

**Note: this is a working study, not a complete research project.**

This notebook is an exploratory NLP analysis of NVIDIA's Q4 FY2026 earnings call transcript (February 25, 2026), conducted as a preliminary exercise for a broader research project on extracting predictive signals from earnings call transcripts.

## What This Does

The transcript is scraped from Motley Fool, parsed into speaker-labeled turns, and split into Prepared Remarks and Q&A sections. The following analyses are applied:

- **Basic text statistics** — word counts, talk time distribution, turn lengths by speaker and role
- **Topic drift** — cosine similarity between analyst questions and management responses, measuring how closely Jensen Huang and Colette Kress stay on topic
- **Certainty arc** — a hedging vs. booster word score plotted chronologically to track how linguistic confidence evolves across the call
- **Sentiment analysis** — VADER (general) and Loughran-McDonald (finance-specific) lexicons compared across speakers and sections
- **Linguistic complexity** — Flesch Reading Ease, Flesch-Kincaid Grade Level, average sentence length, and syllables per word across management turns

## Key Tools

Python, BeautifulSoup, pandas, scikit-learn, VADER, pysentiment2, textstat, matplotlib

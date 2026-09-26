# Basket
A noon Minutes–style grocery recommender built on 3 million real Instacart orders.

## What it will do (Demo Day, 31 Dec 2026)
- **Your next basket** – pick any user, see the groceries they're likely to reorder, ranked.
- **Frequently bought together** – open a product, see what goes with it, plus a bundle and its expected revenue.
- **Cold start in Arabic** – new products with Arabic names still get sensible recommendations (bge-m3 embeddings).
- **The launch memo** – an A/B test design and readout: should we ship this, and what is it worth?

## How it works
Instacart orders → candidates (co-purchase lift, ALS, embeddings) → LightGBM ranker → offline eval · live demo · A/B simulator

## Roadmap
- [ ] Phase 0 – Setup and first look at the data
- [ ] Phase 1 – Statistics and A/B testing
- [ ] Phase 2 – Recommender systems
- [ ] Phase 3 – Serving and the business story
- [ ] Phase 4 – Launch

## Data
[Instacart Market Basket Analysis](https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis). Download it into `data/`; it isn't committed.

## Setup
    python -m venv .venv
    .venv\Scripts\activate
    pip install -r requirements.txt
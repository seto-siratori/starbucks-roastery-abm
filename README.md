# Starbucks Chicago Roastery: Agent-Based Modeling

An Agent-Based Model (ABM) simulating customer flow through the world's largest Starbucks — the 35,000 sq ft, 5-floor Reserve Roastery at 646 N Michigan Ave, Chicago.

## The Idea

A Roastery isn't a café — it's a coffee theme park. The key question isn't "how fast can we serve?" but "how do we make customers explore more floors, stay longer, and spend more?"

This project builds a data-grounded ABM using 70 real Yelp reviews as behavioral anchors, combined with physical building data and Bayesian-calibrated transition matrices.

## Notebooks (7)

| # | Notebook | Description |
|---|----------|-------------|
| 1 | [Roastery Data](https://www.kaggle.com/code/shiratoriseto/starbucks-roastery-floor-data) | Floor structure, 46 menu items, adjacency matrix |
| 2 | [Review NLP](https://www.kaggle.com/code/shiratoriseto/starbucks-roastery-review-nlp) | Floor/product extraction from 70 Yelp reviews |
| 3 | [Transition Calibration](https://www.kaggle.com/code/shiratoriseto/starbucks-roastery-transition-calibration) | Bayesian blending: physical prior + observed data |
| 4 | [ABM Simulation](https://www.kaggle.com/code/shiratoriseto/starbucks-roastery-abm-simulation) | 5,000-agent customer flow simulation |
| 5 | [Product Association & Cross-Sell](https://www.kaggle.com/code/shiratoriseto/starbucks-roastery-product-association-cross-sel) | Product co-mention network, cross-sell opportunities |
| 6 | [ABM Sensitivity & Validation](https://www.kaggle.com/code/shiratoriseto/starbucks-roastery-abm-sensitivity-validation) | Perturbation test, convergence, validation |
| 7 | [Customer Flow Strategy](https://www.kaggle.com/code/shiratoriseto/starbucks-roastery-customer-flow-strategy) | Flow optimization, revenue maximization, experience design |

## Kaggle Resources

- **Dataset:** [Starbucks Chicago Roastery ABM Data](https://www.kaggle.com/datasets/shiratoriseto/starbucks-roastery-abm)

## Key Findings

- **4F (Arriviamo Bar)** is the anchor floor: highest dwell time (35 min), highest spend ($22 avg), mentioned in 57% of reviews
- **Espresso Martini** is the #1 product mention (26/70 reviews)
- **3F → 4F** is the strongest natural transition: coffee experience → cocktails
- **1F/2F congestion** vs **3F/5F underutilization** is the primary flow imbalance
- Multi-floor visitors spend 2-3x more than single-floor visitors

## Data Sources

| Source | License | Used for |
|--------|---------|----------|
| [Starbucks Reserve](https://www.starbucksreserve.com/) | Public | Floor layout, menus |
| Yelp reviews (manual) | Fair use | 70 reviews for NLP extraction |
| Building layout | Public | Adjacency matrix prior |

## Methodology

1. **Real data anchor:** 70 manually collected Yelp reviews (not scraped)
2. **NLP extraction:** Regex-based floor/product mention extraction with transition sequence parsing
3. **Bayesian calibration:** Physical adjacency prior + observed transitions, weighted by observation count
4. **ABM simulation:** 5,000 independent agents with floor-specific dwell times and spend
5. **Sensitivity analysis:** ±30% perturbation on all parameters, convergence testing

## Related Projects

- [Manhattan Cafe Wars: Spatial Analysis](https://github.com/seto-siratori/starbucks-kaggle) — 15-notebook series
- [Starbucks Recommendation Engine](https://github.com/seto-siratori/starbucks-recommendation) — 8-notebook series

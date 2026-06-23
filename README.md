\# Quick Commerce Urgency Badge — A/B Test Analysis



\## Objective

Test whether displaying a 'Only 3 left!' urgency badge on low-stock products

increases add-to-cart rate on a quick commerce platform (Swiggy Instamart / Blinkit scale).



\---



\## Business Question

> Did showing the urgency badge increase add-to-cart rate, and is the lift

> large enough to justify a full platform rollout?



\---



\## Tools \& Libraries

| Tool | Purpose |

|---|---|

| Python 3 | Core analysis language |

| Jupyter Notebook | Analysis environment |

| Pandas | Data manipulation |

| NumPy | Numerical computation |

| SciPy | Chi-square test, z-test, confidence interval |

| Matplotlib / Seaborn | Visualisations |



\---



\## Dataset

Synthetic dataset of 50,000 user sessions generated in Python.

All parameters grounded in published industry benchmarks:



| Parameter | Value | Source |

|---|---|---|

| Base add-to-cart rate | 18% | Statista India e-grocery benchmark, 2023 |

| Expected lift | \~4pp | Nielsen urgency nudge studies |

| Average order value | ₹450 | Redseer Quick Commerce India Report, 2023 |

| Session distribution | Evening-weighted | Blinkit peak hour patterns |



\---



\## Process

1\. Generated 50,000 synthetic sessions with documented assumptions

2\. Exploratory Data Analysis — group balance, raw conversion rates, heatmap

3\. Chi-square hypothesis test — p-value, effect size (Cohen's h), 95% CI

4\. Power analysis — confirmed test is well-powered at 80% power

5\. Segmentation — lift by product category and time of day

6\. Revenue projection — monthly impact at platform scale

7\. Written business recommendation



\---



\## Key Findings

\- \*\*Statistically significant lift:\*\* Badge increased add-to-cart rate by \~4pp (p < 0.001)

\- \*\*95% CI entirely above zero\*\* — result is not due to chance

\- \*\*Evening strongest:\*\* 5.8pp lift in Evening vs 2.1pp in Morning

\- \*\*Consistent across categories:\*\* All 5 product categories show positive lift

\- \*\*Projected impact:\*\* \~₹55 crore additional revenue per month at scale



\---



\## Recommendation

Roll out the urgency badge platform-wide, prioritising Evening (5pm–9pm)

and Night (9pm–12am) slots. Begin with a phased rollout and validate

with live traffic for 4 weeks before full deployment.



See \[`recommendation.md`](recommendation.md) for the full one-page business write-up.



\---



\## Repository Structure

swiggy-urgency-badge-ab-test/

├── notebook/

│   └── ab_test_analysis.ipynb   # Full analysis notebook

├── data/

│   └── ab_test_data.csv         # Generated dataset (50,000 sessions)

├── visuals/

│   ├── 01_conversion_rate_by_group.png

│   ├── 02_session_distribution.png

│   ├── 03_heatmap_category_time.png

│   ├── 04_hypothesis_test_results.png

│   ├── 05_segmentation_by_category.png

│   ├── 06_segmentation_by_time.png

│   └── 07_revenue_by_timeslot.png

├── recommendation.md            # One-page business recommendation

└── README.md

---

## Limitations
- Synthetic data — validate with live traffic before full rollout
- Novelty effect not controlled for — run 4+ weeks in production
- Add-to-cart is a leading metric; purchase completion not tracked
- Brand trust and repeat purchase rate should be monitored post-rollout
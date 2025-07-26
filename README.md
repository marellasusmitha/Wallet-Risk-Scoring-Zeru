# Wallet Risk Scoring – Zeru Stage 2 Assignment

## About the Project

This assignment was part of the Stage 2 evaluation for the AI Engineer internship at Zeru.

The task was to develop a risk scoring model (0–1000 scale) for a list of wallet addresses by analyzing their transaction activity on the Compound V2/V3 DeFi protocol.

## My Thought Process

At first, I was very new to DeFi and blockchain, but I took this opportunity to understand how credit scoring works in decentralized finance. I explored different scoring strategies(static, dynamic, or randomized) and kept changing the logic to learn what works best.While testing multiple methods, I noticed something interesting — **almost all wallets had little to no transaction activity**.the results always leaned toward **lower scores**, indicating **high risk**.

Then I realized: **this itself is the insight**.

> In DeFi, a lack of on-chain behavior is a signal of risk. You can’t trust what you can’t see.

##  Final Scoring Logic Used

I created a tier-based scoring strategy based on the number of transactions (txns) fetched via the Covalent API:

| Number of Transactions | Assigned Score (Randomized Range) | Reason |
|------------------------|------------------------------------|--------|
| 0                      | 100–200                            | No activity = high risk |
| 1–3                    | 300–500                            | Too little info = uncertain |
| 4–10                   | 500–700                            | Some activity = moderate |
| 11–20                  | 700–850                            | Consistent = good user |
| 21+                    | 850–1000                           | High engagement = low risk |

##  Tools & Stack

- Python
- Pandas
- Covalent API
- Matplotlib
- Google Colab
- GitHub

##  Files in This Repository

- `wallet.py` – Main code for fetching txns & assigning scores
- `wallet_risk_scores.csv` – Output file with wallet_id and risk score
- `analysis.md` – Summary of results and score distribution
- `README.md` – This file

##  My Learning
Before this assignment, I didn’t know anything about Compound, on-chain transactions, or DeFi lending protocols. But after doing this end-to-end project, I understood how decentralized lending works and how important behavior-based scoring is for DeFi credit systems.

I enjoyed this challenge a lot and I’m truly interested in learning more about building responsible AI systems in DeFi 🚀


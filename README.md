# Wallet Risk Scoring from Compound Protocol – Zeru AI Assignment (Stage 2)

## Project Objective
This project focuses on building a credit-risk scoring system for 100 Ethereum wallets based on their on-chain activity with the Compound DeFi protocol. The goal is to assign each wallet a **risk score between 0 to 1000**, where:
- **Lower scores** indicate risky, inactive, or suspicious wallets.
- **Higher scores** indicate trustworthy and healthy DeFi behavior.

  
##  Data Source
The list of wallet addresses (100 in total) was provided in a CSV file. Transaction data for each wallet was fetched using the **Covalent API**, which provides a structured view of token transfers on Ethereum.


## Tools & Tech Used
- Python
- Pandas
- Requests (API integration)
- Matplotlib (for score distribution visualization)
- Covalent API
- Compound V2 (Data basis)


## Feature Engineering
For each wallet, the following features were extracted:
- **Total number of transactions**
- **Number of successful token transfers**
- (Optional future improvements: check borrow/lend activity, liquidation history)


## Risk Scoring Logic
The risk score was calculated based on transaction activity:

- If total transactions = 0 → score = **1000** (very high risk)
- If transactions > 50 → score = **200** (low risk)
- If 10 < transactions ≤ 50 → score = **500**
- If 1 < transactions ≤ 10 → score = **800**
- (Dummy logic used for demo, can be replaced by a real ML scoring model)

The final score was clipped between **0 and 1000** and stored in `wallet_risk_scores.csv`.

##  Output
A CSV file with the following format:

| wallet_id                                  | score  |
|--------------------------------------------|--------|
| 0xfaa0768bde629806739c3a4620656c5d26f44ef2 | 732    |


## Score Distribution
A histogram was plotted to visualize how risk scores are distributed. Most wallets in the sample were active and received **scores close to 1000**, indicating low risk.


##  My Learnings
As I'm new to Web3 and DeFi, this project helped me understand:
- How lending/borrowing works on protocols like Compound
- How to fetch blockchain data using Covalent API
- Basics of risk modeling in a decentralized environment


##  Notes
This is a basic version of wallet risk scoring. With more access, the model can be improved by:
- Analyzing lending vs borrowing patterns
- Identifying default or liquidation history
- Flagging wallets interacting with risky or malicious contracts

⚠️ Note: The given wallet dataset seems to contain mostly high-activity, low-risk wallets. As a result, the risk scores are skewed toward the upper end (close to 1000). For a more balanced and insightful risk scoring model, I would recommend including a mix of dormant, liquidated, or low-activity wallets.


<img width="772" height="603" alt="Screenshot 2025-07-25 204342" src="https://github.com/user-attachments/assets/ecae348c-55af-4d30-a325-22fda03013e6" />

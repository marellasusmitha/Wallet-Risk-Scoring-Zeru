# Wallet Risk Scoring from Compound Protocol – Zeru AI Assignment (Stage 2)

##  Project Objective

This project focuses on designing a risk scoring model for Ethereum wallets based on their interaction history with the Compound DeFi protocol. The goal is to assign a **credit-like risk score ranging from 0 to 1000**, where:
- **Higher scores** indicate a wallet is more trustworthy and low-risk.
- **Lower scores** suggest risky, inactive, or potentially suspicious wallets.

This score can help evaluate if a wallet is eligible for zero-collateral loans in the DeFi ecosystem.


##  Data Source

- A CSV file containing 100 wallet addresses was provided.
- Transaction data for each wallet was fetched using the **Covalent API**, which allows access to on-chain activity like token transfers.


##  Tools & Technologies Used

- Python
- Pandas
- Matplotlib
- Covalent API
- Ethereum wallets
- Compound V2 protocol


##  Feature Engineering

The main feature used for scoring was:

- **Total number of transactions** fetched from the wallet’s on-chain history.
This was used as a proxy for wallet activity and trustworthiness.


##  Risk Scoring Logic

The risk score was calculated using this logic:

| Total Transactions | Risk Score | Interpretation         |
|--------------------|------------|-------------------------|
| 0                  | 0          | Inactive, risky wallet |
| 1–10               | 400        | Low activity           |
| 11–50              | 700        | Moderately active      |
| > 50               | 1000       | Very active & trusted  |

- This logic assumes that wallets with more on-chain history are more reliable.
- Scores were clipped between 0 and 1000.


## 📁 Output

The final output is a CSV file with the following format:

| wallet_id                                  | score |
|--------------------------------------------|--------|
| 0xfaa0768bde629806739c3a4620656c5d26f44ef2 | 1000   |
| ...                                        | ...    |


##  Future Improvements
- Include features like lending/borrowing behavior, liquidation history, and token balance trends.
- Handle wallets with missing API data separately.
- Integrate this score into a real-time risk prediction dashboard.


## My Learnings
-This was my first time working with DeFi and blockchain data, and honestly, I found it really interesting. I learned how to fetch wallet data using APIs, process it in Python, and give scores based on activity. I didn’t know much about crypto protocols before, but now I understand how they work and how risk scoring can help. I’m still learning, but I really enjoyed doing this task!

## 📌 Note:
In this version, we followed a positive scoring logic, where wallets with higher on-chain activity receive higher scores (closer to 1000), indicating they are more active and trustworthy.
Wallets with low or no transaction history were assigned lower scores, as limited activity may reflect risk or inactivity.
This aligns with real-world credit systems where higher scores = safer users. Most wallets in our dataset scored high, suggesting they are generally safe and reliable for DeFi use cases.


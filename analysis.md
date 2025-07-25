#  Wallet Risk Score Analysis

##  Score Distribution Overview

After applying the positive risk scoring logic, we plotted the distribution of scores for the 100 Ethereum wallets.

The results showed that:

- **Majority of wallets scored near 1000**, indicating they are **very active and trustworthy**.
- This suggests that the dataset provided includes mostly well-used, safe wallets — possibly from real users in Compound's ecosystem.

---

##  Interpretation of Results

| Score Range | Meaning                     | Wallet Behavior                  |
|-------------|-----------------------------|----------------------------------|
| 0–100       | Extremely risky             | No on-chain activity             |
| 100–400     | High risk                   | Very few transactions            |
| 400–700     | Medium risk                 | Moderate usage                   |
| 700–1000    | Low risk (safe)             | High DeFi activity, trustworthy  |

- Since most wallets scored **above 700**, we can conclude that the sample data mostly consists of **reliable, DeFi-native users**.
- There were **no wallets with score 0**, which suggests all wallets had at least some valid history.

##  Score Distribution Visualization
<img width="772" height="603" alt="Screenshot 2025-07-25 204342" src="https://github.com/user-attachments/assets/976733a4-1bca-44c8-86e4-aa7440221051" />

The histogram clearly shows a **skew toward the upper end** (near 1000), confirming that wallets are predominantly safe.

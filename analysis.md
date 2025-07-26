# 📊 Wallet Risk Score Analysis – Stage 2 (Zeru AI Internship)

## Overview

As part of the wallet risk scoring task, I analyzed the behavior of 100 wallet addresses by fetching their transaction history on Compound V2/V3 using the Covalent API. The risk score was calculated based on the number of interactions each wallet had with the protocol.

## Score Distribution

The histogram below shows the distribution of scores among the 100 wallets.

<img width="798" height="650" alt="output" src="https://github.com/user-attachments/assets/e4fcd0f8-2605-46f9-9b80-e98d3e69d787" />

- Most scores fall between **100 and 200**.
- This range represents wallets with **low or no transaction activity**, which leads to **higher risk** based on the model logic.

## What This Means

- The output shows that many wallets had **limited interaction** with Compound V2/V3.
- This is an important factor in DeFi scoring — because in decentralized systems, **user behavior is the only trust signal available**.
- A wallet that hasn't borrowed, lent, or repaid much cannot be confidently marked as trustworthy.

## My Learning

From this task, I learned how risk modeling works in DeFi and how on-chain behavior reflects the user's trust level.  
Even if most scores are on the lower side, it matches the logic: **less activity = more uncertainty = higher risk**.

## Final Thoughts

This was a very useful learning experience in combining blockchain data, API integration, feature engineering, and score modeling — all within a real-world DeFi use case.


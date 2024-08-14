---
description: Create your own pool and make your token tradeable on ALEX's decentralized exchange in simple steps!
---

# 📝 Self-Service Listing

## Getting Started

### What is self-service listing?

Self-service listing allows you to list your own token on ALEX's decentralized exchange, enabling the permissionless trade of your token against a so-called anchor token within the exchange. The anchor token is typically one with a stable value, providing a reliable reference point for defining the price of the newly listed token.

ALEX decentralized exchange (DEX) is an Automated Market Maker (AMM) type of exchange. This means it operates with trading pools. These pools consist of a pair of tokens with sufficient funds (liquidity) of each to ensure a fair trade between the tokens that make up the pool.

In this context, listing a token involves launching a new liquidity pool containing the new token and the anchor token on ALEX's AMM DEX, thereby facilitating trading within the community and enabling price discovery. 

{% hint style="warning" %}
**Supported tokens:** ALEX Self-Service Listing currently supports Stacks Chain Tokens (SIP-10 Standard Token).
{% endhint %}

### Minimum requirements

👉 **Token Deployment.** Have your token deployed on Stacks blockchain since you will need to provide the token contract.

👉 **Select an Anchor Token.** Choose an anchor token from the available options: Stacks native currency STX, ALEX token, or aBTC token. Ensure you have at least 1,800 STX or an equivalent value in ALEX or aBTC token to create the pool (minimum anchor token liquidity).

👉 **Determine Initial Price.** Decide the initial price for your listing token in terms of anchor token units. This should answer the question: how many anchor tokens do users need to buy one listed token?

👉 **Calculate Initial Liquidity.** Once the initial price is determined, make calculations and decide the initial liquidity amounts for both tokens in the pool.

#### Calculation example (price, ratio, and initial amounts)

Let's suppose you choose STX as the anchor token and want to provide 4,000 STX as the initial anchor token liquidity.

To determine the price, you need to decide how many STX equals 1 of your listing token. In other words, decide how many STX users will need to buy 1 listed token. Let's say you set the price of your token at 0.5 STX.

To calculate the initial liquidity for the listed token, you need to divide the anchor token amount by the price. This is 4,000 STX / 0.5 STX = 8,000, resulting in the initial amount for the listed token.

The liquidity pool of the pair **Listed Token :rocket: - Anchor Token :anchor:** will have an initial ratio of 2:1. This ratio is calculated as the minimal expression of the fraction 8,000 / 4,000 (initial listed token amount slash initial anchor token amount).

## Steps to self-list your token

**Step 1:** Submit the token information on the [Self-Service Listing page](https://app.alexlab.co/self-service-listing) of the ALEX Lab App & deposit the anchor token :anchor:.

**Step 2:** Wait for the wrapped token contract creation (around 24-48 hours).

**Step 3:** Deposit the listing token :rocket: and the pool will be automatically created on ALEX's AMM DEX. The new pool will be listed as an ALEX Pool in the Self Listed tab on [app.alexlab.co/pool](https://app.alexlab.co/pool).

🤝 After this step, you (and everyone) can start trading your token in ALEX DEX 🤝

**Step 4 (optional):** Provide additional token information and make your token visible on the ALEX Token List at [app.alexlab.co/token-list](https://app.alexlab.co/token-list). To do so, click "Customer Support" on the [Self-Service Listing page](https://app.alexlab.co/self-service-listing) and submit the social media information, such as X accont, Discord, official website, etc.

See the [FAQs](#faqs) section for further information.

## First time self-listing a token? 🙋

Visit our how-to sections for a step-by-step guide on [How to Self-List and Create a Pool](../../how-to/how-to-self-list.md).

## FAQs

### Which are the anchor tokens supported?

Native STX currency, ALEX token and aBTC token.

### Is there a minimum liquidity amount for the anchor token?

Yes. Initial liquidity of the anchor token must be a minimum of 1,800 STX or the equivalent value in in ALEX or aBTC tokens.

### How is the initial price determined?

The initial price is determined by the initial liquidity provided by the creator. The ratio between the pair of funds determines the price relationship between both tokens. 

For instance, if the creator provides 8,000 listing tokens and 2,000 anchor tokens, that means the initial ratio is 4:1. Note that pool ratios are calculated as the minimal expression of the fraction between initial amounts. In this case, is 8,000 / 2,000.

We can think of this initial ratio in two ways (and they are both equivalent):

- 4 listing tokens equals 1 anchor token.
- 1 listing token equals 0.25 anchor tokens.

### How does the price change once the pool is created?

Once the pool is created, the price discovery phase starts. Users can permissionlessly trade the pair of assets, and the Automated Market Maker (AMM) algorithm will determine the price dynamics of the newly listed token.

### Is there some requirement to make the listed token visible in ALEX Token List?

Yes. ALEX requires a “Coingecko” or “CoinMarketcap” token listing to verify the provided social media information before uploading it to the official list at [app.alexlab.co/token-list](https://app.alexlab.co/token-list).

### Why is the wrapped token version necessary?

Wrapped tokens are “pass-through” tokens that do not retain economics and its purpose is ease of developers and security. ALEX is responsible for deploying wrapped contracts.

It is more a technical thing and it is not relevant from user perspective rather than it involves a whole step in the procedure and takes some time.

### Is it possible to avoid wrapped contract deployment?

Yes. However this may not speed the waiting time and requires some conditions in the token contract. 

You won't need a wrapped version of the token if this two conditions are met:

1. Your token contract complies with ALEX's fungible token trait. This trait is the regular SIP-10 Standard Token Trait plus the helper functions for 8-digit fixed notation. See source code on [explorer](https://explorer.hiro.so/txid/0xd8d41e686264b1f8f7b3bd13016f00baf69d98c89c2aa588b5b96b5164d83e1d?chain=mainnet).
2. Your token has 8 decimals. 

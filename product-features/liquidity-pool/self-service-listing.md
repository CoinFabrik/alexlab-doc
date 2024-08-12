---
description: Create your own pool and make your token tradeable on ALEX's decentralized exchange in simple steps!
---

# 📝 Self-Service Listing

## Getting Started

### What is self-service listing?

Self-service listing allows you to list your own token on ALEX's decentralized exchange, enabling the permissionless trade of your token against a so-called anchor token within the exchange.

ALEX decentralized exchange (DEX) is an Automated Market Maker (AMM) type of exchange. This means it operates with trading pools. These pools consist of a pair of tokens with sufficient funds (liquidity) of each to ensure a fair trade between the tokens that make up the pool.

{% hint style="warning" %}
**Supported tokens:** ALEX Self-Service Listing currently supports Stacks Chain Tokens (SIP-10 Standard Token).
{% endhint %}

### Minimum requirements

👉 Have your token deployed on Stacks blockchain since you will need you provide the token contract.

👉 Choose an anchor token (Stacks native currency STX, ALEX token, or aBTC token) and ensure you have the minimum amount for the anchor token (1,800 STX or an equivalent value in ALEX or aBTC token).

👉 Choose the initial price for your listing token in anchor token units. This should answer the question: how many anchor tokens do users need to buy one listed token?

👉 Once the initial price is determined, make calculations and decide initial liquidity amounts for both tokens.

#### Calculation example (price, ratio, and intial amounts)

Let's suppose you choose STX as the anchor token and want to provide 4,000 STX as the initial anchor token liquidity.

To determine the price, you need to decide how many STX equals 1 of your listing token. In other words, decide how many STX users will need to buy 1 listed token. Let's say you decide the price of your token is 0.5 STX.

To calculate the initial liquidity for the listed token, you need to divide the anchor token amount by the price. This is 4,000 STX / 0.5 STX = 8,000, resulting in the initial amount for the listed token.

The liquidity pool of the pair **Listed Token :rocket: - Anchor Token :anchor:** will have an initial ratio of 2:1. This ratio is calculated as the minimal expression of the fraction 8,000 / 4,000 (initial listed token amount slash initial anchor token amount).

## Steps to self-list your token

**Step 1:** Submit the token information on the [Self-Service Listing page](https://app.alexlab.co/self-service-listing) of ALEX Lab App & deposit the anchor token :anchor:.

**Step 2:** Wait for the wrapped token contract creation (around 24-48 hours).

**Step 3:** Deposit the listing token :rocket: and the pool will be automatically created on ALEX's AMM DEX. The new pool will be listed as an ALEX Pool in the Self Listed tab on [app.alexlab.co/pool](https://app.alexlab.co/pool).

🤝 After this step, you (and everyone) can start trading your token in ALEX DEX 🤝

**Step 4 (optional):** Provide additional token information and make your token visible on the ALEX Token List: [app.alexlab.co/token-list](https://app.alexlab.co/token-list). To do so, click "Customer Support" on the [Self-Service Listing page](https://app.alexlab.co/self-service-listing) and send social media information such as X accont, Discord, official website, etc.

See the [FAQs](#faqs) section for further information.

### How to avoid Step 2?

[WIP]

The wrapped version of the token it is not necessary this two conditions are met:

- Your token contract complies with ALEX's fungible token trait. This trait is the regular SIP-10 Standard Token trait plus the helper functions for 8-digit fixed notation. See source code on [explorer](https://explorer.hiro.so/txid/0xd8d41e686264b1f8f7b3bd13016f00baf69d98c89c2aa588b5b96b5164d83e1d?chain=mainnet).
- Your token has 8 decimals. 

## First time self-listing a token? 🙋

Visit our how-to sections for a step-by-step guide on [How to Self-List and Create a Pool](../../how-to/how-to-self-list.md).

## FAQs

### How is the initial price determined?

The initial price is determined by the initial liquidity provided by the creator. The ratio between the pair of funds determines the price relationship between both tokens. 

For instance, if the creator provides 8,000 listing tokens and 2,000 anchor tokens, that means the initial ratio is 4:1. Note that pool ratios are calculated as the minimal expression of the fraction between initial amounts. In this case, is 8,000 / 2,000.

We can think of this initial ratio in two ways (and they are both equivalent):

- 4 listing tokens equals 1 anchor token.
- 1 listing token equals 0.25 anchor tokens.

### How does the price change once the pool is created?

Once the pool is created, the price discovery phase starts. Users can permissionlessly trade the pair of assets, and the Automated Market Maker (AMM) algorithm will determine the price dynamics of the newly listed token.

### Which are the anchor tokens supported?

Native STX currency, ALEX token and aBTC token.

### Is there a minimum liquidity amount for the anchor token?

Yes. Initial liquidity of the anchor token must be a minimum of 1,800 STX or the equivalent value in in ALEX or aBTC tokens.

### Is there some requirement to make the listed token visible in ALEX Token List?

Yes. ALEX requires a “Coingecko” or “CoinMarketcap” token listing to verify the provided social media information before uploading it to the official list at [app.alexlab.co/token-list](https://app.alexlab.co/token-list).
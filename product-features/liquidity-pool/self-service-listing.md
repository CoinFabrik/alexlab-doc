---
coverY: 0
layout:
  cover:
    visible: false
    size: full
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 📝 Self-Service Listing

Create your own pool and make your token tradeable on ALEX's decentralized exchange in simple steps!

To create a Liquidity Pool you will need to provide liquidity for two types of tokens.

- :rocket: **Token X:** The token you wish to list
- :anchor: **Token Y:** The anchor token

By doing so, you are allowing the permisionless trade of the pair Token X / Token Y within ALEX's AMM exchange.

{% hint style="warning" %}
**Supported tokens:** ALEX Self-Service Listing currently supports Stacks Chain Tokens (SIP-10 Standard Token).
{% endhint %}

## Steps

Step 1: Submit the token information & deposit the anchor token (Token Y)

Step 2: Waiting for the wrapped token contract creation (around 24-48 hours)

Step 3: Deposit the listing token (Token X)

Step 4: Open Pool

Step 5: Provide additional token information

See [FAQs](#faqs) sections for further information.

## First time self-listing a token? 🙋

Visit our how-to sections for a step-by-step guide on [How to Self-List and Create a Pool](../../how-to/how-to-self-list.md).

## FAQs

### How is the initial price determined?

Inital price is determined by the initial Pool Liquidity provided by the creator.

### How does the price change once the pool is created?

Once the pool is created, the price discovery phase starts. Users can permissionless trade the pair of assets and the Automated Market Maker (AMM) algorithm will determine the price dynamics of the Token X.

### Which are the anchor tokens supported?

Native STX currency, ALEX token and aBTC token.

### Is there a minimum liquidity amount for the anchor token?

Yes. Initial liquidity of the anchor token must be a minimum of 1800 STX or the equivalent value to 1800 STX in ALEX or aBTC tokens.

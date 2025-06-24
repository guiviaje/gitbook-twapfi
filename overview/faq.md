---
description: Frequently Asked Questions
---

# ❓ FAQ

<details>

<summary>What is the benefit of TWAP on DeFi?</summary>

The primary benefit of a TWAP on DeFi is that it allows you to **minimise your slippage per child order** which results in a **lower overall slippage for every parent order executed.** Let’s outline this with an example.&#x20;

A user wished to sell 100K AURA for USDT. If the user executes one single transaction, **the user will receive 108,550 USDT with a slippage of 3.10%.** However, if the user decides to leverage Twap.fi’s TWAP and split his order into 4 child orders with a maximum slippage of 1%, **the user will receive 110,956 USDT.**\
\
Hence, by leveraging Twap.fi’s algorithms, **the user received an additional 2,400 USDT** for the same transaction.&#x20;

</details>

<details>

<summary>What is the benefit of DCA on DeFi?</summary>

Let’s assume you wish to invest 900 USDT into AVAX over 3 days. This means that you will invest $300 into AVAX every day. Let’s assume that AVAX/USDT is trading at $20 on day 1, $10 on day 2 and $15 on day 3. Based on the prices above, you will receive 15 AVAX on day 1, 30 AVAX on day 2 and 20 AVAX on day 3. Cumulatively, **you will receive 65 AVAX for the 900 USDT that you wish to invest.**

If you invest 900 USDT into AVAX in a lump-sum transaction based on the prices on day 1 ($20), **you will receive 45 AVAX.**\
\
Therefore, by utilising Twap.fi’s DCA function and spreading out your purchases over time, **you receive an additional 20 AVAX for the same capital invested.**&#x20;

</details>

<details>

<summary>What are the settings of TWAP and how do you use them?</summary>

You can read more about the TWAP settings [here](../order-types/smart-twap/how-to-twap.md) and understand how you can leverage each of them to elevate your order execution. &#x20;

</details>

<details>

<summary>What are the settings of DCA and how do you use them?</summary>

Read more about DCA settings [here](../order-types/capital-efficient-dca/how-to-dca.md) and learn how to spread out your purchases effectively.&#x20;

</details>

<details>

<summary>Which network, aggregators and wallets are available?</summary>

### Networks

Currently, we are **integrated with the following networks**:

Ethereum, BSC, Polygon, Avalanche, Arbitrum, Optimism, Base\


### Aggregators

Currently, we are integrated with the **following aggregators:**&#x20;

1inch, 0x, Odos, Paraswap, KyberSwap, OpenOcean, OKX DeFi and Uniswap\


### Wallets

Currently, we are integrated with the **following wallets:**&#x20;

Rabby Wallet, WalletConnect, MetaMask, Rainbow, Ledger Live, Coinbase Wallet and Phantom.

\
Based on our [roadmap](roadmap.md), twap.fi will focus on **integrating EVM-compatible chains** such as Mantle, Metis, Manta etc along with other popular chains such as Solana and Cosmos. **Networks will be prioritised for integration via a community vote.** Furthermore, twap.fi will add more support for wallets and aggregators to offer users greater flexibility in managing their assets securely.

</details>

<details>

<summary>Does the user pay gas for each transaction?</summary>

Twap.fi offers a gasless experience which means that the user doesn’t have to pay gas for each transaction. In this gas-less transaction model, twap.fi eliminates the need to purchase and hold the native token for transaction approval, making trading more accessible and user-friendly.\
\
Instead, twap.fi charges a settlement fee in either the input token or output token, the more liquid asset. The settlement fee is approximately equivalent to the gas fee required for the transaction. Hence, the settlement fees can largely depend on the level of network congestion at the time of execution.&#x20;

</details>

<details>

<summary>Where are the orders routed to?</summary>

Each order will be routed to one of the DEX aggregators that are integrated into Twap.fi (1inch, 0x, Odos, Paraswap, KyberSwap, OpenOcean, OKX DeFi and Uniswap). The order will be sent to the aggregator that provides the best quote for the transaction. While executing a TWAP order, each child order can be routed to different aggregators despite it being part of the same parent order.&#x20;

Users also have the ability to choose the aggregator they wish to execute on. For example, if a user only wishes to execute either on 1inch or 0x, they can select these aggregators on the top right of the order panel (on the left of the network button). Within the same settings, users can enable “MEV Protection'' on Ethereum.

</details>

<details>

<summary>What are the fees?</summary>

twap.fi charges a small fee of 0.2% to run TWAP, DCA and LIMIT order and even less for simple swap (0.05%). The fees are charged directly as part of the settlement fee.

</details>

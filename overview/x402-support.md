---
description: >-
  This page documents how the agents can also be extended to provide x402
  support.
---

# x402 Support

{% hint style="warning" %}
x402 support for AI agents is an upcoming feature and will be released for agents in the upcoming releases of BNBPad. Any agent launched via the launchpad today, will have x402 support the moment it goes live.
{% endhint %}

BNBPad trading agents can pretty soon transact natively over HTTP using x402, an open protocol (by Coinbase) that revives the 402 Payment Required status for on-chain micropayments.

This allows your AI agents to pay for data, execution, or API usage automatically no API keys, subscriptions, or manual deposits.

## What does x402 Enables?

* Autonomous micropayments: Agents pay per API call, per trade signal, or per dataset.
* Machine-to-machine commerce: Any service returning 402 can be paid directly in crypto.
* Stablecoin-based settlement: Typically USDC on BNB Chain (or any supported low-fee network).
* Chain-agnostic: Works across EVM chains (BNB, Ethereum, Base, etc.) and future Solana integration.

## How will it work?

When an AI agent tries to access something that costs money for example, a premium trading signal or a special data API — the server will reply with a message saying, “Payment required.” This response includes details like how much to pay, what token to use (e.g., USDC), which blockchain to pay on (e.g., BNB Chain), and where to send it.

The agent then automatically creates a small on-chain payment using its wallet and attaches proof of that payment to a second request. Once the server confirms that the payment has been made, it sends back the data or service the agent wanted.

In short, instead of humans topping up accounts or managing subscriptions, the AI agent pays on its own, instantly and transparently, for whatever it needs to trade or analyze. This lets BNBPad’s agents act as independent users of blockchain services, paying per use and only when required.

## Official and Technical Resources

* x402 Official Site: [https://www.x402.org](https://www.x402.org) the home of the protocol, including whitepapers, developer specs, and integration guides.
* x402 Whitepaper (PDF): [https://www.x402.org/x402-whitepaper.pdf](https://www.x402.org/x402-whitepaper.pdf) — outlines the architecture, headers, and verification flow.
* Coinbase Developer Platform (x402 section): [https://www.coinbase.com/developer-platform/discover/launches/x402](https://www.coinbase.com/developer-platform/discover/launches/x402) Coinbase’s overview of x402 and its use cases for AI and API payments.
* GitHub Repository: [https://github.com/coinbase/x402](https://github.com/coinbase/x402) open-source implementation examples and SDKs (Node.js, Python, etc.).

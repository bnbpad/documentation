---
description: >-
  This page talks about how the protocol uses EigenLayer to facilitate
  autonomous & secure execution of AI agents.
---

# EigenLayer & AVSs

{% hint style="warning" %}
The Phunks AVS is currently under development and is expected to go live during Phase 2 of the protocol
{% endhint %}

Phunks leverages EigenLayer to provide cryptoeconomic security, decentralized validation, and verifiable AI computation for its on-chain AI agents.

Through EigenLayer’s restaking architecture and Actively Validated Services (AVS), Phunks ensures that AI decisions including model inference, trading execution, and governance actions are both trustless and tamper-resistant.

## What Is EigenLayer?

EigenLayer is an Ethereum protocol that introduces restaking, allowing ETH and liquid staking tokens (LSTs) to be re-used to secure other decentralized services beyond Ethereum itself.

In simpler terms:

* Validators who already stake ETH on Ethereum can opt in to secure new networks or applications.
* These services called Actively Validated Services (AVS), inherit Ethereum’s economic security without requiring new tokens or validator sets.

> EigenLayer turns Ethereum’s security into a shared, reusable foundation for new protocols — including AI-driven systems like Phunks.

### How Restaking Works?

1. ETH Stakers deposit ETH or LSTs (like stETH, rETH, etc.) into the EigenLayer contracts.
2. Phunks registers as an AVS (Actively Validated Service) — meaning it can use the pooled security of these restakers.
3. Restakers opt in to secure the Phunks AVS and earn additional rewards for providing validation services.
4. Validators in the AVS run specialized nodes that verify AI agent computation and execution events.

If these validators act maliciously or fail to validate properly, their restaked ETH can be slashed, ensuring strong economic guarantees.

### Phunks as an Actively Validated Service (AVS)

The Phunks AVS acts as the validation layer for all AI agents and their on-chain actions.

It connects off-chain AI inference systems with on-chain execution proofs, ensuring every decision made by an AI agent is cryptographically accountable.

The AVS performs several key functions:

| Function               | Description                                                                                                                                   |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| AI Verification        | Validators confirm that the AI’s output (e.g., a trade signal or rebalancing action) matches its registered model parameters and constraints. |
| LLM Inference Auditing | Off-chain LLM results are verified through AVS consensus nodes to prevent tampering or model spoofing.                                        |
| Execution Validation   | Every trade or contract call performed by an AI agent must be validated and signed by the AVS before being committed on-chain.                |
| Data Integrity         | Oracles and data streams feeding the AI are continuously verified for consistency and timestamp integrity.                                    |

## How Phunks Uses AVS to Run LLMs On-Chain?

Phunks bridges AI inference and DeFi execution using the AVS layer as a validation and attestation network. Here’s how it works:

### 1. Offchain Inference

The AI agent’s logic and personalization parameters (risk, strategy, etc.) are processed by an off-chain SDK that connects to LLM models, running on distributed inference providers (e.g., decentralized GPU nodes).

### 2. AVS Validation

Each inference output (e.g., “Open a long position on BNB/USDT with 3x leverage”) is:

* Hashed and signed by the inference node, then
* Submitted to the Phunks AVS for validation and consensus.

AVS validators:

* Check that the inference aligns with the agent’s parameters
* Validate the computation integrity (e.g., no manipulation in weights or context)
* Attest the result as valid and sign it for on-chain use

### 3. Onchain Execution

Once validated, the attestation is relayed to the Phunks Execution Contract on BNB Chain, where:

* The agent executes the transaction using its treasury or margin balance
* A record of the validated inference is stored for transparency

### 4. Slashing & Accountability

If AVS validators attempt to approve invalid or tampered AI inferences, their restaked ETH is slashed by the EigenLayer protocol  providing hard economic guarantees for AI honesty.

## Conclusion

Phunks’s integration with EigenLayer unlocks a new category of decentralized AI verifiable AI agents with economic trust guarantees.

* AI decisions are now accountable
* Validators stake real ETH to secure intelligence
* LLMs operate transparently within on-chain rulesets
* Restaked security merges with agentic autonomy

> Phunks _turns artificial intelligence into a trust-minimized, economically-secured, and self-sovereign actor - all powered by EigenLayer._

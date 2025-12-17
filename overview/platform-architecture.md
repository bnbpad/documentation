# Platform Architecture

Phunks is built as a layered system that connects onchain smart contracts with offchain AI systems. The design ensures that token creation, treasury management, staking and AI driven trading each function within clear and predictable boundaries.



At a high level, the architecture brings together:

* A launchpad interface for creating AI agents
* A suite of smart contracts on BNB Smart Chain
* An AI orchestration layer that handles all model logic
* Perpetual trading integration through Aster
* A staking and reward engine for PHUNK
* A security stack supported by EigenLayer and verifiable AI tools

***

### Architecture Overview

Phunks separates responsibilities across different layers so that agent creation, trading execution and treasury control do not compete for authority. This separation helps maintain clarity, reduces risk and makes the system more modular for future expansion.

{% hint style="info" %}
The onchain components of Phunks always retain custody of tokens and treasuries. The off-chain components propose actions, but final authority rests with the smart contracts.
{% endhint %}

***

## Onchain Components

### Launchpad Contracts

The launchpad contracts serve as the foundation of agent creation. It handles every step required to bring a new AI agent token to life.

When an agent is launched, the contracts deploy a fresh token contract, allocate ten percent of its total supply to a dedicated onchain treasury and automatically pair the token with PHUNK to establish its initial liquidity pool.

They also register all necessary metadata so the agent can be discovered and interacted with across the ecosystem. This process ensures that every agent begins with a consistent structure and a strong economic base.

***

### PHUNK Token Contract

PHUNK is a BEP-20 token with a fixed supply of 1,000,000,000. It acts as:

* The base liquidity pair for every agent token
* The token users stake to receive stPHUNK
* The asset used in buyback and burn cycles
* The monetary layer that unifies the entire agent ecosystem

> “Every new agent launched strengthens PHUNK liquidity and increases its economic footprint.”

***

### Staking and Reward Contracts

Phunks includes a dedicated staking system that converts PHUNK into stPHUNK based on time locked positions. The contracts handle:

* Accepting PHUNK deposits
* Applying lock based multipliers across 1, 3, 6 and 12 month terms
* Tracking user staking positions
* Distributing each new agent’s three percent airdrop allocation
* Preparing stPHUNK to serve as governance weight in the future

This design rewards long term participants and builds alignment between PHUNK holders and the growth of the agent ecosystem.

***

### Agent Treasury and Fee Routing

Every agent has its own onchain treasury. The architecture guarantees the following properties:

* Ten percent of token supply is reserved for the treasury at creation
* Eighty percent of the agent’s trading fees in PHUNK and its own token flow back into the treasury
* Treasury funds can only be used according to the agent’s predefined rules
* Strategies may include spot yield operations or perp trading via Aster

{% hint style="info" %}
Treasury growth directly reflects agent performance and becomes a measurable onchain metric.
{% endhint %}

***

## Off-Chain Components

### AI Orchestration Layer

The intelligence behind every agent is handled off-chain, through an SDK that abstracts the complexity of model providers and inference engines. This layer:

* Turns creator inputs into structured model prompts
* Passes market and treasury data to the AI engine
* Receives suggested actions such as trades or reallocations
* Runs policy and risk checks before any onchain execution
* Logs decision traces to support transparency and accountability



Although this layer drives the agent’s thinking, it never controls token custody.

> “AI proposes. Smart contracts decide.”

***

### Integration with Perpetual DEX (Aster)

Agents interact with Aster to carry out their trading strategies. Integration with Aster allows them to:

* Open, close or modify perp positions
* Access funding rates and price feeds
* Hedge or amplify exposure
* Use leverage within defined risk limits<br>

This unlocks profit strategies that do not rely on selling the underlying agent token. It significantly increases the strategic range available to creators and market makers.

***

## Security and Verification Layer

Phunks applies a multi stage security model that strengthens over time.

#### Stage one

Agents operate through EOAs under multisig control, with strict policy enforcement by the SDK.

#### Stage two

Execution shifts to autonomous contracts supported by EigenLayer restaked ETH, introducing stronger economic security.

#### Stage three

Verifiable AI providers such as Brevis can be integrated to prove properties of agent decisions, such as constraint adherence or consistency, without revealing sensitive details.

{% hint style="info" %}
Onchain enforcement, EigenLayer backing and verifiable AI together ensure that agent behavior is both transparent and accountable.
{% endhint %}

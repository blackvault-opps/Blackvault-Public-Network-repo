# BlackVault Public Network™

**Powered By Intelligent Design™**

BlackVault Public Network™ is the public blockchain and digital-asset framework connecting **SafeVault™**, **Vault Coin™ (VLT)**, **FUNTOKEN (FUN)**, and **Vault AI™**.

This repository documents the current public framework, project relationships, development milestones, and publication materials for the Network.

## Current Network Structure

| Project | Role | Current Position |
| --- | --- | --- |
| **BlackVault Public Network™** | Public ecosystem, application framework, documentation, and project coordination layer. | Active development |
| **SafeVault™** | BlackVault smart-account and digital-asset environment. | Smart-account architecture / application development |
| **Vault Coin™ (VLT)** | BlackVault production-token project. | Ethereum Mainnet pre-deployment review |
| **FUNTOKEN (FUN)** | Experimental blockchain and wallet-integration token experience. | Deployed on Sepolia testnet |
| **Vault AI™** | Intelligent operations, blockchain discovery, analysis, and SafeVault handoff layer. | Botpress/application integration development |

## Ecosystem Relationship

```text
BlackVault Public Network
|
+-- SafeVault
|   +-- BlackVault Smart Account
|   +-- Vault Coin
|   +-- FUNTOKEN
|   +-- Connected External Wallets
|   `-- Vault AI integration
|
+-- Vault Coin (VLT)
|
+-- FUNTOKEN (FUN)
|
`-- Vault AI
```

The projects retain separate technical responsibilities while presenting a coordinated BlackVault user experience.

# SafeVault™

SafeVault is designed as the **BlackVault smart account from the beginning**.

A user's SafeVault is intended to be the primary BlackVault blockchain account experience rather than an interface that requires a third-party wallet as its starting point.

The planned SafeVault experience includes:

- a BlackVault smart-account address;
- asset overview and activity;
- Vault Coin integration after confirmed production deployment;
- FUNTOKEN Sepolia integration;
- receive and send/review flows;
- Vault Coin Rewards surfaces;
- Vault AI integration;
- account permissions and settings; and
- optional connection of existing external wallets.

## Connected External Wallets

MetaMask, Trust Wallet, and other compatible wallets may be connected as an optional secondary layer for supported asset visibility and interaction.

External-wallet connection does not automatically grant transaction authority or delegation. Any future delegation capability is a separate account feature.

## Smart-Account Direction

The approved architecture separates the primary SafeVault smart account from optional EIP-7702-style capabilities that may be used with existing externally owned accounts.

The SafeVault application architecture is being prepared for account-abstraction components including account initialization, UserOperation preparation, EntryPoint/bundler integration, validation, recovery, permissions, and optional gas-sponsorship infrastructure.

Implementation choices for deployment timing, gas sponsorship, and the final authentication/recovery model remain separate owner-controlled configuration decisions.

# Vault Coin™ (VLT)

Vault Coin is the BlackVault production-token project.

The canonical technical repository defines the current VLT implementation and deployment status.

| Property | Current Approved Model |
| --- | --- |
| **Name** | Vault Coin |
| **Symbol** | VLT |
| **Decimals** | 18 |
| **Initial Supply** | 100,000,000 VLT |
| **Lifetime Issuance Ceiling** | 420,000,000 VLT |
| **Architecture** | ERC-1967 proxy with UUPS upgrades |
| **Production Network** | Ethereum Mainnet, chain ID 1 |
| **Deployment Status** | Pre-deployment review |

No production VLT contract address is published here until a confirmed deployment record exists.

[Vault Coin Technical Repository](https://github.com/blackvault-opps/Vault-Coin-VLT-project)

# FUNTOKEN (FUN)

FUNTOKEN is the BlackVault **Sepolia testnet experience**.

FUN provides an on-chain environment for token interaction, wallet behavior, delegation history, interface development, and SafeVault/Vault AI integration testing without representing Vault Coin's production deployment.

Current recorded project facts include:

- Network: Sepolia testnet
- Chain ID: `11155111`
- Token symbol: `FUN`
- ERC-20 transfer and allowance interface
- Three recorded Sepolia deployments
- Canonical shared FUN address: pending owner selection

[FUNTOKEN Technical Repository](https://github.com/blackvault-opps/FUN-TOKEN-ERC-20-Report-Repo)

# Vault AI™

Vault AI is BlackVault Public Network's intelligent operations and blockchain discovery layer.

Its planned application responsibilities include:

- BlackVault ecosystem navigation and Q&A;
- public wallet/address inspection;
- transaction explanation;
- token-transfer discovery;
- contract inspection;
- potential claim-indicator analysis;
- persistent asset-case organization;
- transaction preparation for review; and
- SafeVault workflow handoff.

Vault AI separates **discovery and preparation** from **account authorization**. SafeVault remains the account layer responsible for reviewing and authorizing protected account actions.

The current Vault AI Botpress configuration and application handoff package is maintained in the BlackVault Public Network site repository.

[BlackVault Public Network Site Repository](https://github.com/blackvault-opps/BlackVault-Public-Network-site-repo)

# Public Application Model

The BlackVault application is being organized around the following public areas:

- Home
- Ecosystem
- Vault Coin
- FUNTOKEN
- SafeVault
- Vault AI
- Support
- Privacy
- Terms

SafeVault application areas are planned around:

- Home
- Vault Coin
- FUNTOKEN
- Connected Assets
- Activity
- Receive
- Send / Review
- Rewards
- Vault AI
- Settings

# Repository Relationships

## Public Network documentation

[BlackVault Public Network](https://github.com/blackvault-opps/Blackvault-Public-Network-repo)

## Application package

[BlackVault Public Network Site](https://github.com/blackvault-opps/BlackVault-Public-Network-site-repo)

## SafeVault

[SafeVault Public Pre-deployment Repository](https://github.com/blackvault-opps/SafeVault_deploy-repo)

SafeVault application components are also developed in the private `safevault-deployment` repository and may be consolidated into the BlackVault application with source provenance preserved.

## Vault Coin

[Vault Coin Technical Repository](https://github.com/blackvault-opps/Vault-Coin-VLT-project)

## FUNTOKEN

[FUNTOKEN Technical Repository](https://github.com/blackvault-opps/FUN-TOKEN-ERC-20-Report-Repo)

# Documentation Position

Current documentation should reflect the confirmed five-part ecosystem:

1. BlackVault Public Network
2. SafeVault
3. Vault Coin
4. FUNTOKEN
5. Vault AI

Historical Rewards Network, card, Telegram Stars, and earlier payment-network models are not part of this current application framework.

Vault Coin Rewards may exist as a SafeVault/Vault Coin product feature and should not be represented as a revival of the historical Rewards Network.

# Development Position

BlackVault Public Network remains under active implementation. Project documentation distinguishes application development, testnet activity, pre-deployment review, and confirmed production deployment.

FUNTOKEN's Sepolia deployment is separate from Vault Coin's Ethereum Mainnet production lifecycle.

# Contact

**BlackVault Public Network™**  
Email: [support@enterblackvault.com](mailto:support@enterblackvault.com)

---

**Powered By Intelligent Design™**

© 2026 BlackVault Public Network™. All rights reserved.

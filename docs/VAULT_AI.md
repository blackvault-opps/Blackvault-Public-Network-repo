# Vault AI™

Vault AI is the intelligent operations and blockchain-discovery layer of BlackVault Public Network.

## Purpose

Vault AI provides a conversational interface for navigating BlackVault project information and analyzing public blockchain records.

Its initial application scope includes:

- ecosystem Q&A;
- public wallet/address inspection;
- native and token balance discovery;
- transaction-history analysis;
- transaction explanation;
- ERC-20 transfer discovery;
- contract inspection;
- potential claim-indicator analysis;
- persistent asset-case organization; and
- SafeVault workflow preparation.

## Operating Model

```text
User
 |
 v
Vault AI
 |
 +-- Knowledge
 +-- Address Discovery
 +-- Transaction Analysis
 +-- Contract Inspection
 +-- Token Transfer Discovery
 +-- Claim Analysis
 |
 v
SafeVault Handoff
 |
 v
Review / Account Authorization
```

Vault AI's application role is discovery, analysis, explanation, and preparation. SafeVault is the account environment that receives transaction/action handoffs.

## Botpress Architecture

The Vault AI Botpress package is organized around:

- agent configuration;
- Studio instructions;
- workflow definitions;
- persistent tables;
- knowledge sources;
- normalized blockchain actions;
- conversation routing; and
- SafeVault handoff records.

### Initial workflows

1. Main Router
2. Asset Discovery
3. Transaction Inspection
4. Contract Inspection
5. Claim Analysis
6. SafeVault Handoff
7. Case Continuation

### Initial persistent data

- `asset_cases`
- `verified_contracts`
- `scan_results`
- `safevault_handoffs`

### Initial blockchain actions

- `validatePublicAddress`
- `getNativeBalance`
- `getTokenBalances`
- `getTransactionHistory`
- `getTransactionDetails`
- `inspectContract`
- `inspectTokenTransfers`
- `createAssetCase`
- `updateAssetCase`
- `prepareSafeVaultHandoff`

## Provider Model

Provider-specific blockchain responses should be normalized before they reach the conversational reasoning layer.

The first discovery provider may use Etherscan together with configured Ethereum/Sepolia RPC or indexing services.

Configuration values such as API credentials and RPC endpoints are supplied through environment/configuration variables.

## BlackVault Knowledge Sources

Vault AI knowledge should distinguish:

- BlackVault Public Network documentation;
- SafeVault architecture;
- Vault Coin canonical technical documentation;
- FUNTOKEN deployment records; and
- Vault AI operational documentation.

Verified on-chain data remains separate from descriptive project documentation.

## Current Implementation Position

The Botpress configuration/handoff package is present in `blackvault-opps/BlackVault-Public-Network-site-repo` under `botpress-vault-ai/`.

The next implementation stage is the executable provider-action layer that connects the defined actions to Etherscan/RPC data and returns normalized results to Botpress.

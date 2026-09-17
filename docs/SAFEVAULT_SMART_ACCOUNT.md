# SafeVault Smart Account Architecture

SafeVault is the BlackVault smart-account and digital-asset environment.

## Primary Account Model

The approved model begins with a BlackVault account that initializes a SafeVault smart account. The SafeVault address is intended to become the user's primary BlackVault blockchain address.

```text
Create BlackVault Account
        |
        v
Initialize SafeVault Smart Account
        |
        v
SafeVault Dashboard
        |
        +-- Vault Coin
        +-- FUNTOKEN
        +-- ETH / supported assets
        +-- Receive
        +-- Send / Review
        +-- Activity
        +-- Rewards
        +-- Vault AI
        `-- Settings
```

## Account-Abstraction Direction

SafeVault is being prepared around an ERC-4337-style smart-account architecture.

Planned components include:

- account initialization/factory interface;
- UserOperation construction;
- transaction review;
- EntryPoint integration;
- bundler integration;
- gas estimation;
- optional paymaster integration;
- validation/authentication modules;
- recovery modules;
- scoped permissions/session capabilities; and
- Vault AI handoff permissions.

## Connected Wallets

Existing wallets are optional secondary connections.

```text
SafeVault Smart Account
        |
        +-- Primary BlackVault assets
        |
        `-- Connected Wallets
              +-- MetaMask
              +-- Trust Wallet
              `-- Other compatible wallets
```

Connecting an external wallet does not automatically activate delegation.

Optional EIP-7702 functionality, when implemented for compatible EOAs, remains distinct from the SafeVault primary smart-account model.

## Network Roles

**Ethereum Mainnet (chain ID 1)** is the production target for Vault Coin and production SafeVault account functionality.

**Sepolia (chain ID 11155111)** hosts the FUNTOKEN testnet experience and may support development/testing integrations.

## Vault AI Relationship

Vault AI discovers, analyzes, explains, and prepares account workflows.

SafeVault receives those handoffs and presents protected account actions for the appropriate account authorization flow.

## Open Implementation Decisions

The following remain owner-controlled implementation selections:

- immediate smart-account deployment versus deterministic/counterfactual initialization;
- user-paid gas versus optional sponsored/paymaster flows; and
- final authentication and recovery mechanism.

These decisions are configuration and implementation milestones rather than changes to the approved smart-account-first product identity.

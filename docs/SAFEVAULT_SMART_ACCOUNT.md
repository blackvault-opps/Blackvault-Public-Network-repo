# SafeVault Smart-Account Architecture

**Updated:** 2026-09-18

SafeVault has two wallet layers:

1. **Homebase — the primary BlackVault smart account.** A user signs in to the BlackVault application to reach their Homebase workspace, assets, activity, and account controls. The approved product direction starts with a holder-controlled smart account. Application login, account initialization, and blockchain authorization are separate operations.
2. **Connected external wallets — an optional second layer.** Existing compatible wallets retain their own addresses, networks, balances, and permissions. Connecting one enables supported visibility and interaction; moving assets into Homebase is a separately authorized transfer.

The primary design uses an ERC-4337-style account model. Optional EIP-7702 support for compatible external EOAs is a separate integration proposal. A connected wallet is not evidence of an active delegation. Account deployment timing, gas arrangements, authentication/recovery, and infrastructure providers remain implementation selections.

Assets remain recorded on their respective blockchains. Homebase brings those records into a coordinated interface; signing in does not merge accounts or transfer balances.

## Account execution design

The primary design calls for account initialization/factory support, UserOperation preparation, account validation, EntryPoint/bundler configuration, gas estimation, receipt tracking, recovery, and permission management. Optional paymaster infrastructure and external EOA delegation remain separately configured capabilities.

The initial wallet action path uses holder review and confirmation. Future automation requires a separately enabled account permission with network, contract/function, recipient, amount, expiry, and revocation controls enforced by the account's execution layer.

## Wallet and agent roles

| Component | Responsibility |
| --- | --- |
| BlackVault Public Network | Ecosystem identity, application framework, and documentation |
| SafeVault | Homebase, external wallet connections, asset presentation, review, and account authorization |
| Vault AI | Workspace assistance, approved knowledge, public-data discovery, evidence explanation, and prepared handoffs |
| Discovery/claim backend | Provider requests, contract-specific eligibility checks, and structured evidence |
| Wallet execution infrastructure | Validate holder authorization, submit approved operations, and return execution evidence |

Workspace administrator permissions, VLT contract-owner powers, and individual wallet authority are separate. Signing credentials remain within the holder's chosen wallet/authentication system. Future automated execution requires separately enabled, limited, revocable permissions enforced by the actual account execution layer.

## Networks

| Context | Network | Configuration status |
| --- | --- | --- |
| Vault Coin (VLT) | Ethereum mainnet, `1` | Production proxy and deployment receipt pending |
| FUNTOKEN (FUN) | Sepolia, `11155111` | Three recorded deployments; shared canonical address pending owner selection |
| Initial Vault AI recovery workflow | Ethereum mainnet, `1` | First supported claim contract and live connection pending validation |
| FUN discovery and development | Sepolia, `11155111` | Separate, explicitly selected testnet context |

Identify every asset by chain ID and full contract address. A token symbol alone is insufficient. Additional networks require their own supported provider and contract configuration.

## Development position

The approved Homebase direction is documented; the current private SafeVault application source is a presentation/configuration foundation. Smart-account initialization, authentication/recovery, signing, asset activity, and external-wallet sessions are target modules. The source record and actual deployments are separate milestones.

Open selections include immediate versus counterfactual account deployment, user-paid versus optional sponsored gas, the final authentication/recovery method, account implementation/factory, and infrastructure providers.

See [SafeVault public framework](https://github.com/blackvault-opps/SafeVault_deploy-repo/blob/main/docs/SAFEVAULT_CURRENT_FRAMEWORK.md).

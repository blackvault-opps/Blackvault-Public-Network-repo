# Vault AI — Workspace and Asset Discovery

**Updated:** 2026-09-18

Vault AI is the BlackVault workspace agent for approved knowledge, operational assistance, and public blockchain evidence. The current Botpress work configures its identity, instructions, knowledge, routes, tool bindings, and investigation records.

## Role in SafeVault

SafeVault Homebase is the primary BlackVault smart account. Existing wallets are optional separate connections. Vault AI explains context and prepares supported handoffs; the account system manages user authorization and execution. Workspace roles and VLT owner controls are distinct from each user's wallet authority.

## Current source and integration position

| Area | Current position |
| --- | --- |
| Botpress instructions and workflows | Configuration specifications are present in the application repository |
| Etherscan read helpers | Source includes address syntax, native balance, normal history, ERC-20 transfers, source metadata, and receipt lookup |
| Claim indicators | Source classifier identifies visible assets and possible indicators from supplied evidence |
| Current token holdings | Full holdings enumeration is not implemented in the reviewed action facade |
| Case records and handoffs | Schemas/workflows documented; runtime storage and wallet bindings pending validation |
| Scan service | `/scan` and `/details` remain proposed interfaces; no deployed base URL is established by the source |
| Validated eligibility | Requires a supported protocol adapter and current wallet-specific evidence |

Knowledge preparation can proceed while live connections are pending. Etherscan is the data provider/explorer; it is not the BlackVault service endpoint. The current source may support direct server-side read-action bindings independently of a later scan service.

## Evidence model

| Finding | Required interpretation |
| --- | --- |
| Asset visible | A holding or transfer was observed at a particular address and chain. |
| Candidate claim | A contract or protocol indicator supports further investigation. |
| Validated eligibility | A supported contract adapter has checked the exact network, wallet entitlement, token, amount, recipient, required proof, relevant state, and a current simulation where applicable. |
| Confirmed recovery | Execution succeeded and the expected asset movement or protocol outcome was verified. |

A positive token balance, an ABI method name, or source-code verification alone does not establish claim eligibility. Preserve evidence sources, the queried block/time, and scan coverage. An unavailable provider or unsupported protocol produces an incomplete/unsupported result rather than a conclusion that no assets exist. Unknown values remain explicitly pending.

## Networks

Initial recovery targets Ethereum mainnet (`1`). FUN discovery uses a separate explicit Sepolia (`11155111`) context. The current helper source does not provide Polygon/BSC adapters or an all-chain scan.

## Knowledge and workspace continuity

Keep approved architecture, historical records, source implementation, configured tools, and live blockchain evidence distinguishable. Record source versions, account/network context, and coverage. The broader browser-workspace extension, device pairing, scheduling, and additional connectors remain separately tracked implementation features.

[Vault AI workspace overview](https://github.com/blackvault-opps/Vault-AI-Extension-Public-Deployment-Repo) · [SafeVault architecture](SAFEVAULT_SMART_ACCOUNT.md) · [Repository index](REPOSITORY_INDEX.md)

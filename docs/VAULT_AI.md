# Vault AI Workspace Copilot — Workspace and Asset Discovery

**Updated:** 2026-09-20

**Vault AI Workspace Copilot** is the canonical name of BlackVault's workspace agent/system. **BlackVault Public Network** remains the ecosystem/platform name. **Vault AI** is the short conversational name.

The current Botpress work configures the Copilot's identity, instructions, knowledge, routes, tool bindings, investigation records, and coordinated handoffs.

## Role in SafeVault

SafeVault Homebase is the primary BlackVault smart account. Existing wallets are optional separate connections. Vault AI Workspace Copilot explains context, investigates supported public evidence, coordinates approved project work, and prepares supported handoffs; the account system manages user authorization and execution. Workspace roles and VLT owner controls are distinct from each user's wallet authority.

## Team coordination

| System | Primary task |
| --- | --- |
| Vault AI Workspace Copilot / Botpress | Conversation orchestration, knowledge, workflows, cases, tool routing, evidence classification, SafeVault handoff preparation |
| GitHub Copilot | Repository-local implementation, tests, documentation consistency, code review, proposed patches |
| Microsoft/Windows Copilot | Microsoft/desktop workspace coordination, local application context, cross-agent handoffs |
| ChatGPT | Architecture reconciliation, authorized connected GitHub operations, cross-system review and implementation coordination |

Cross-agent work should carry the task, assigned agent, authorization state, source/version, completed evidence, pending dependency, and next action. No system should infer that another system completed an external action without returned evidence.

## Current source and integration position

| Area | Current position |
| --- | --- |
| Botpress instructions and workflows | Configuration specifications are present in the application repository |
| Etherscan read helpers | Source includes address syntax, native balance, normal history, ERC-20 transfers, source metadata, and receipt lookup |
| Claim indicators | Source classifier identifies possible indicators from supplied evidence |
| Current token holdings | Full holdings enumeration is not implemented in the reviewed action facade |
| Case records and handoffs | Schemas/workflows documented; runtime storage and wallet bindings pending validation |
| Scan service | `/scan` and `/details` remain proposed interfaces; no deployed base URL is established by source |
| Validated eligibility | Requires a supported protocol adapter and current wallet-specific evidence |

Knowledge preparation can proceed while live connections are pending. Etherscan is the data provider/explorer; it is not the BlackVault service endpoint.

## Evidence model

| Finding | Required interpretation |
| --- | --- |
| Asset visible | A holding or transfer was observed at a particular address and chain. |
| Candidate claim | A contract or protocol indicator supports further investigation. |
| Validated eligibility | A supported contract adapter has checked exact network, wallet entitlement, token, amount, recipient, required proof, relevant state, and current simulation where applicable. |
| Confirmed recovery | Execution succeeded and the expected asset movement or protocol outcome was verified. |

A positive token balance, ABI method name, or source-code verification alone does not establish claim eligibility.

## Networks

Initial recovery targets Ethereum mainnet (`1`). FUN discovery uses a separate explicit Sepolia (`11155111`) context. The current helper source does not provide Polygon/BSC adapters or an all-chain scan.

## Identity persistence

Botpress user-facing agent identity should persist as **Vault AI Workspace Copilot**. If a UI edit reverts to **BlackVault Public Network**, inspect the persisted Botpress bot/workspace field, imported configuration, deployment revision, and source-controlled agent configuration rather than repeatedly editing the visible label. The application repository now carries the canonical source configuration and Botpress implementation handoff.

[Vault AI workspace overview](https://github.com/blackvault-opps/Vault-AI-Extension-Public-Deployment-Repo) · [SafeVault architecture](SAFEVAULT_SMART_ACCOUNT.md) · [Repository index](REPOSITORY_INDEX.md)

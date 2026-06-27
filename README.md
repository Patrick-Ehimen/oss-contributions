# oss-contributions

> A running index of my external open-source contributions — PRs, proposals, and shipped extensions across the blockchain, storage, and developer-tooling ecosystems.

**Status key:** 🟣 merged &nbsp;·&nbsp; 🟢 open &nbsp;·&nbsp; 🔴 closed

---

## Index

| # | Organisation | Repo | PRs | Merged |
|---|---|---|---|---|
| 1 | [OpenZeppelin](#-openzeppelin) | contracts-wizard | 1 | 1 |
| 2 | [ChainSafe](#-chainsafe) | forest (Filecoin Rust client) | 1 | 1 |
| 3 | [Sablier Labs](#-sablier-labs) | indexers · sdk | 5 | 3 |
| 4 | [NethermindEth](#-nethermindeth) | stellar-private-payments | 3 | 2 |
| 5 | [Raycast](#-raycast) | extensions (rust-docs) | 2 | 1 |
| 6 | [DefiLlama](#-defillama) | DefiLlama-Adapters | 1 | 0 |
| 7 | [IPFS / libp2p](#-ipfs--libp2p) | helia-verified-fetch · ipfs-check · js-kubo-rpc-client · js-libp2p | 4 | 0 |
| 8 | [Storacha](#-storacha) | piri · upload-service · indexing-service · storacha.network · ucan-see-my-request | 9 | 0 |
| 9 | [Akave AI](#-akave-ai) | akavesdk-py · akave-pldg · akavelink | 5 | 1 |
| 10 | [lighthouse-web3](#-lighthouse-web3) | lighthouse-package | 1 | 0 |

**Total: 32 PRs across 10 organisations · 9 merged**

---

## 🔒 OpenZeppelin

**[contracts-wizard](https://github.com/OpenZeppelin/contracts-wizard)** — Smart contract code generator (ERC20, ERC721, ERC1155, Governor, custom)

| PR | Title | Status |
|---|---|---|
| [#456](https://github.com/OpenZeppelin/contracts-wizard/pull/456) | Add collapse optional sections by default | 🟣 merged |

> Optional contract sections (Votes, Access Control, Upgradeability across all types and languages) now load collapsed. Checkbox expands automatically; manual expansion still possible for previewing child options without activating. Fixes [#449](https://github.com/OpenZeppelin/contracts-wizard/issues/449).

---

## 🦁 ChainSafe

**[forest](https://github.com/ChainSafe/forest)** — Filecoin node implementation in Rust

| PR | Title | Status |
|---|---|---|
| [#7070](https://github.com/ChainSafe/forest/pull/7070) | feat: add DESCRIPTION to all missing RPC methods | 🟣 merged |

> Brought OpenRPC description coverage from **133/229 (58%) → 229/229 (100%)** across all method groups: auth, beacon, chain, network, state, sync, wallet, multisig, market, F3, and Ethereum-compatible.

---

## 🌊 Sablier Labs

**[indexers](https://github.com/sablier-labs/indexers)** — Multi-chain indexers for the Sablier token streaming protocol

| PR | Title | Status |
|---|---|---|
| [#276](https://github.com/sablier-labs/indexers/pull/276) | feat(airdrops): add indexing support for VCA campaigns | 🟣 merged |
| [#275](https://github.com/sablier-labs/indexers/pull/275) | refactor: convert Store namespace exports to object exports | 🟣 merged |
| [#274](https://github.com/sablier-labs/indexers/pull/274) | Split justfile into modular files | 🟣 merged |
| [#294](https://github.com/sablier-labs/indexers/pull/294) | refactor(envio): use ENVIO_ABI_PATH for ABI file paths | 🔴 closed |

> **#276** — Added Variable Claim Amount campaign indexing: new schema fields, `createVCA` + `updateForgoneAmount` store functions, `VariableClaimAmount` category enum.
>
> **#275** — Converted `Store` namespace exports to object exports, fixing Biome `noFloatingPromises` blind spot for async store calls.
>
> **#274** — Split a 349-line monolithic `justfile` into `envio.just`, `graph.just`, `gql.just`, `helpers.just` — zero breaking changes, all 60+ recipes intact.

**[sdk](https://github.com/sablier-labs/sdk)** — Sablier TypeScript SDK

| PR | Title | Status |
|---|---|---|
| [#161](https://github.com/sablier-labs/sdk/pull/161) | test(cron): add bytecode validation for all contracts | 🔴 closed |

> `eth_getCode` on every contract address across all releases; `beforeAll` pre-fetch with deduplication, concurrency cap of 10, and exponential backoff.

---

## 🔮 NethermindEth

**[stellar-private-payments](https://github.com/NethermindEth/stellar-private-payments)** — Nethermind's private payment protocol on Stellar

| PR | Title | Status |
|---|---|---|
| [#295](https://github.com/NethermindEth/stellar-private-payments/pull/295) | feat: add remove non-membership leaf to admin UI | 🟣 merged |
| [#214](https://github.com/NethermindEth/stellar-private-payments/pull/214) | feat: add push notifications for inactivity reminders | 🟣 merged |
| [#202](https://github.com/NethermindEth/stellar-private-payments/pull/202) | Fix rustdoc warnings | 🟣 merged |

> **#295** — `removeNonMembershipLeaf()` wired to `client.delete_leaf({ key })` with wallet guard, contract ID validation, status/log/toast feedback.
>
> **#214** — Service worker (`sw.js`), `periodicsync` event, Cache API last-visit tracking, onboarding wizard integration for 5-day inactivity push notifications.
>
> **#202** — Zero rustdoc warnings: generic types in backticks, bracket notation escaped, bare URLs converted. `cargo doc --no-deps --workspace --release` passes clean.

---

## ⚡ Raycast

**[extensions](https://github.com/raycast/extensions)** — Official Raycast extension store

| PR | Title | Status |
|---|---|---|
| [#23891](https://github.com/raycast/extensions/pull/23891) | Add rust-docs extension | 🟣 merged |
| [#24537](https://github.com/raycast/extensions/pull/24537) | Update rust-docs extension | 🔴 closed |

> **#23891** — Built and shipped the [`rust-docs`](https://www.raycast.com/Patrick-Ehimen/rust-docs) extension to the Raycast store. Searches `std`, `core`, and `alloc` directly from the launcher: smart ranking, color-coded type icons, inline formatted documentation, cached results, zero configuration.

---

## 📊 DefiLlama

**[DefiLlama-Adapters](https://github.com/DefiLlama/DefiLlama-Adapters)** — TVL adapters for every DeFi protocol

| PR | Title | Status |
|---|---|---|
| [#17537](https://github.com/DefiLlama/DefiLlama-Adapters/pull/17537) | fix: update BNPL Pay adapter to new protocol contracts | 🔴 closed |

> Old factory `0x7edB0c8b428b97eA1Ca44ea9FCdA0835FBD88029` dead since Jan 2023 caused flatline TVL metrics. Updated to new proxy `0xa800488decf9d4454a2d1ca1968468d0d5772f00`, restored staking tracking, temporarily disabled borrowed TVL pending v2 interface documentation. Closes [#16960](https://github.com/DefiLlama/DefiLlama-Adapters/issues/16960).

---

## 🌐 IPFS / libp2p

**[helia-verified-fetch](https://github.com/ipfs/helia-verified-fetch)** · **[ipfs-check](https://github.com/ipfs/ipfs-check)** · **[js-kubo-rpc-client](https://github.com/ipfs/js-kubo-rpc-client)** · **[js-libp2p](https://github.com/libp2p/js-libp2p)**

| PR | Repo | Title | Status |
|---|---|---|---|
| [#314](https://github.com/ipfs/helia-verified-fetch/pull/314) | helia-verified-fetch | fix: attach server timing to abort errors | 🔴 closed |
| [#121](https://github.com/ipfs/ipfs-check/pull/121) | ipfs-check | feat: add badge endpoint for IPFS availability badges | 🟢 open (draft) |
| [#360](https://github.com/ipfs/js-kubo-rpc-client/pull/360) | js-kubo-rpc-client | feat: implement log/get-level API | 🟢 open |
| [#3374](https://github.com/libp2p/js-libp2p/pull/3374) | js-libp2p | feat: track protocol stream open/close count in metrics | 🟢 open |

> **#314** — `AbortError` now carries a `serverTiming` property with all timing data collected before abort (DNS resolution, IPNS resolution) to aid timeout debugging.
>
> **#121** — Opt-in `/badge` endpoint generating shields.io-style SVG badges by IPFS provider count (green/yellow/red/gray); non-blocking with immediate "checking..." response; configurable in-memory cache with TTL; 32 unit tests.
>
> **#360** — `log.getLevel()` implementation querying Kubo's `log/level` endpoint without modifying log levels; full TypeScript types and tests.
>
> **#3374** — `libp2p_protocol_streams_opened_total` and `libp2p_protocol_streams_closed_total` counters added alongside existing gauge, enabling Prometheus `rate()` / `increase()` stream throughput analysis.

---

## 💎 Storacha

**[upload-service](https://github.com/storacha/upload-service)** · **[piri](https://github.com/storacha/piri)** · **[indexing-service](https://github.com/storacha/indexing-service)** · **[storacha.network](https://github.com/storacha/storacha.network)** · **[ucan-see-my-request](https://github.com/storacha/ucan-see-my-request)**

| PR | Repo | Title | Status |
|---|---|---|---|
| [#446](https://github.com/storacha/upload-service/pull/446) | upload-service | feat: modular UI package architecture with subpath exports | 🟢 open |
| [#231](https://github.com/storacha/piri/pull/231) | piri | Add contract generation workflow and submodule | 🔴 closed |
| [#237](https://github.com/storacha/piri/pull/237) | piri | feat: enhance CI test failure visibility | 🔴 closed |
| [#245](https://github.com/storacha/indexing-service/pull/245) | indexing-service | fix: make deployment depend on test success | 🔴 closed |
| [#191](https://github.com/storacha/storacha.network/pull/191) | storacha.network | Add comprehensive testing infrastructure | 🟢 open |
| [#190](https://github.com/storacha/storacha.network/pull/190) | storacha.network | feat: replace console logging with structured logging | 🟢 open |
| [#28](https://github.com/storacha/ucan-see-my-request/pull/28) | ucan-see-my-request | Add Husky pre-commit hook | 🟢 open |
| [#27](https://github.com/storacha/ucan-see-my-request/pull/27) | ucan-see-my-request | chore: add GitHub Actions | 🟢 open |

> **upload-service #446** — `@storacha/ui/react/components/Authenticator` style subpath exports; TypeScript project references; Tailwind plugin with CSS custom properties; framework-agnostic core utilities; backward-compatible meta-package.
>
> **piri #231** — `FilOzone/pdp` git submodule at `contracts/pdp`; `generate-contracts.sh`; `make generate-contracts` / `verify-contracts` / `contracts-update` targets; `go:generate` directive; VERSION file tracking commit hash.
>
> **indexing-service #245** — Staging and production deploy jobs now `needs: [run-tests, run-checks]`, eliminating the race condition where deploys could complete before tests finished.

---

## 🔷 Akave AI

**[akavesdk-py](https://github.com/akave-ai/akavesdk-py)** · **[akave-pldg](https://github.com/akave-ai/akave-pldg)** · **[akavelink](https://github.com/akave-ai/akavelink)**

| PR | Repo | Title | Status |
|---|---|---|---|
| [#113](https://github.com/akave-ai/akavesdk-py/pull/113) | akavesdk-py | Implement per-file key derivation and fix code quality issues | 🔴 closed |
| [#111](https://github.com/akave-ai/akavesdk-py/pull/111) | akavesdk-py | Add HTTP extension module for range downloads | 🟢 open |
| [#5](https://github.com/akave-ai/akave-pldg/pull/5) | akave-pldg | Project Proposal: CrossChain Archive | 🟣 merged |
| [#3](https://github.com/akave-ai/akave-pldg/pull/3) | akave-pldg | Project Proposal: ZKML Workflows on Akave O3 | 🟢 open |
| [#48](https://github.com/akave-ai/akavelink/pull/48) | akavelink | feat: enhanced integration tests with error scenarios | 🟢 open |

> **akavesdk-py #113** — Per-file `encryption_key()` calls instead of shared key; `chunk.CID` → `chunk.cid` casing bug; bare `except` → specific exception types in `dag.py`; all 80 encryption and DAG tests pass.
>
> **akavesdk-py #111** — `HTTPExtClient` with `range_download()` via HTTP Range header; 200/206/416 handling; Content-Range parsing; streaming to file; 53 unit tests at 99% coverage.
>
> **akave-pldg #5 (CrossChain Archive)** — Unified cross-chain indexer (Wormhole, LayerZero V2, Axelar, CCIP) across Ethereum, Arbitrum, Optimism, Base, Polygon; normalized schema; end-to-end message lifecycle tracing; immutable archival to Akave O3; REST/GraphQL API.

---

## 🟠 lighthouse-web3

**[lighthouse-package](https://github.com/lighthouse-web3/lighthouse-package)** — JavaScript SDK for Lighthouse decentralised storage

| PR | Title | Status |
|---|---|---|
| [#135](https://github.com/lighthouse-web3/lighthouse-package/pull/135) | feat: add resilience features — retry, rate limiting, and timeouts | 🟢 open |

> `withRetry` with exponential backoff + jitter; token-bucket rate limiter; `resilientFetch` drop-in replacing `fetch` across all API calls; `resilientUpload` with progress tracking; `apiConfig.ts` presets per operation type. Closes [#134](https://github.com/lighthouse-web3/lighthouse-package/issues/134).

---

<sub>Last updated: June 2026 &nbsp;·&nbsp; <a href="https://github.com/Patrick-Ehimen">Patrick-Ehimen</a></sub>

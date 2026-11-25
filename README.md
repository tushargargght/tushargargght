### Hi, I'm Tushar

Protocol engineer with extensive backend development experience, building perpetuals infrastructure: the smart contracts, keepers, and backends that drive them. Shipping production systems since 2013.

### What I'm doing now

**Founder & Protocol Engineer at [Punt House](https://punt.house)** (Jul 2026 - now). A perpetuals venue I designed, built, and operate, live on Robinhood Chain testnet (an Arbitrum L2) under continuous synthetic load. Code is private; happy to walk through it.

- **PuntCore**: singleton isolated-margin perps engine, up to 1000x leverage against a house pool (no order book, no funding), behind a transparent upgradeable proxy with ERC-7201 namespaced storage
- **Atomic oracle execution**: signed Pyth Lazer updates verified on chain and cached in EIP-1153 transient storage, so batched orders and liquidations fill at the signed bid/ask in one multicall
- **Solvency as code**: a collateral accounting identity asserted after every batch, unpaid winning PnL settled through a senior FIFO claim queue, covered by invariant suites and fork tests
- **Go backend**: EIP-712 order-ingest API held byte-identical to the contract digest by a cross-language parity suite; a keeper built as a transaction manager (micro-batched multicalls, pre-flight simulation, pipelined nonces with gas-bumped replacement, crash-safe outbox); a cursor-based indexer into Postgres
- **Infra**: Terraform on AWS, zero-touch GitHub Actions deploys, Prometheus and Grafana, a 1,000-wallet synthetic-load harness

**Applied AI deep dive** (Aug 2026 - now), alongside Punt House

- **Completed an 8-course applied AI program** (Educative's AI Skills Learning Path for Software Engineers, 89 lessons): LLM internals, tool calling and MCP, RAG and memory systems, multi-agent orchestration, and shipping LLM apps to production
- **LangChain ecosystem**: hands-on with LangChain, LangGraph, and LangSmith, down to LangGraph checkpointer internals (Postgres schema, thread and checkpoint model, time travel) and per-user conversation isolation
- **Evals**: golden datasets, validated LLM-as-judge, and trace-driven error analysis
- **Framework landscape**: comparative study of Google ADK, OpenAI Agents SDK, Claude Agent SDK, and CrewAI
- **Up next**: an end-to-end LangGraph agent deployed on AWS, traced in LangSmith, with an eval suite and error analysis

### Crypto / DeFi

**Senior Software Engineer, [Rage Trade](https://github.com/RageTrade)** (Apr 2023 - Oct 2025)

- **Perp aggregator**: core layer unifying 7+ venues (GMX, Hyperliquid, Drift, Jupiter, Synthetix, Lighter, Ostium) behind one normalized interface across EVM and SVM transaction and wallet models, **$6B+ cumulative volume**
- **Lighter signer**: ported Lighter's Go signer to WASM for the Node.js backend
- **Liquidation stack**: a detection engine tracking every open position's liquidation price, decoupled from a general-purpose transaction executor that owns all keeper wallets and on-chain submission
- **PERPScreener**: real-time funding rates, open interest, volume, and 2%-depth price impact across all venues, streamed over WebSockets

**Smart Contract Engineer, [mStable](https://github.com/mstable)** (May 2022 - Feb 2023)

- Co-built a 3-layer EIP-4626 vault stack (entry vault → Meta Vault → Convex leaf vaults) routing DAI/USDC/USDT through Curve 3Pool and FraxBP into Convex, shipped to Ethereum mainnet, **$10M+ TVL**
- Ported Curve's StableSwap solvers (`get_D` / `get_y`) from Vyper to Solidity as fee-aware pricing libraries, with `virtual_price` bounds on every entry and exit path against flash-loan and sandwich vectors
- Owned the external security audit end to end; hardened share accounting against ERC-4626 inflation and reward front-running
- Automated vault operations on OpenZeppelin Defender, harvesting CRV/CVX through CowSwap batch auctions

Rage Trade work was done from my work account **[@0xLadoo](https://github.com/0xLadoo)**. Most of my work at Rage Trade and mStable lives in private repos; the public ones are:

| Repo | What it is |
| --- | --- |
| [RageTrade/Perp-Aggregator-SDK](https://github.com/RageTrade/Perp-Aggregator-SDK) | Multi-venue perps SDK |
| [0xLadoo/lighter-go-fork](https://github.com/0xLadoo/lighter-go-fork) | Lighter Go SDK with WASM support |
| [mstable/metavaults](https://github.com/mstable/metavaults) | mStable EIP-4626 Meta Vaults |

### Before crypto

- **Co-Founder & CTO, Croton** (2019 - 2021): bootstrapped SaaS to 250+ paying customers and ~$60K ARR with a team of 6; full backend on Django and PostgreSQL
- **Senior Software Engineer, PaytmMall** (2018 - 2019): CQRS search indexing on Kafka and Elasticsearch across 18 languages, sustaining ~100K requests/min
- **Senior Engineer, Target India** (2017 - 2018): reusable Kafka event pipeline into Salesforce Marketing Cloud
- **Senior Software Engineer, Samsung Research** (2013 - 2016): TCP/network modem development; Fast Dormancy Algorithm cut delay 30%

### Stack

**Languages:** TypeScript · Go · Solidity · Python · Node.js · Rust (learning)

**Web3:** Foundry · Hardhat · OpenZeppelin · viem · ethers.js · go-ethereum · Pyth · Chainlink · The Graph · EIP-712 · EIP-1153 · EIP-4626 · ERC-7201 · ERC-4337

**Backend:** PostgreSQL · Kafka · Redis · MongoDB · Elasticsearch · WebSockets

**Infra:** AWS · Terraform · Docker · GitHub Actions · Prometheus · Grafana

**AI:** LangChain · LangGraph · LangSmith · Google ADK · MCP · Claude Code · Cursor

---

🎓 **IIT Guwahati**, B.Tech Electronics & Communication Engineering | JEE AIR 2195

📫 [LinkedIn](https://www.linkedin.com/in/tushargargght) · [Email](mailto:tushargargght@gmail.com) · [punt.house](https://punt.house)

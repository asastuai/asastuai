# Juan Cruz Maisu

**Independent Researcher** · Cryptography · Decentralized ML · Human–AI Collaboration
Buenos Aires, Argentina

---

## What I work on

At the intersection of cryptography, decentralized machine learning, and how humans collaborate with AI systems at depth. Non-traditional path: no CS degree, autodidact, portfolio-based. 35+ smart contracts deployed on mainnet across BSC and Base · 530+ automated tests across production projects · published Rust crate on crates.io · two papers in the Proof of Context family (one v0.6 framework, one v0.1 applied to verifiable inference).

---

## Recent research work (2026)

### [Proof of Context (v0.6)](https://github.com/asastuai/proof-of-context) — Framework paper

Names the missing verification layer in decentralized ML protocols — the gap between computational correctness (proof-of-learning, zkML, TEE attestations) and *contextual freshness* of the computation. Maps the structural analogue in DeFi (oracle-freshness / stale-price exploits, 2020-2024). Introduces four freshness dimensions, the execution-context-root construction, and the triple-anchor timestamp.

- Paper (PDF): [proof-of-context.pdf](https://github.com/asastuai/proof-of-context/blob/main/paper/proof-of-context.pdf)
- Reference implementation: [proof-of-context-impl](https://github.com/asastuai/proof-of-context-impl) — Rust crate, Phase 2 shipped (real cryptography: SHA-256 Merkle, Ed25519, MockCommitter, MockSettlementGate, end-to-end integration tests)

### [Proof of Context applied to Verifiable Inference (v0.1)](https://github.com/asastuai/proof-of-context) — Working draft, April 2026

First applied paper of the family. Specializes the v0.6 framework to commercial inference-as-a-service via a receipt-based dispute layer over TEE-attested inference. Central finding: v0.6's four freshness dimensions specialize asymmetrically to inference (one collapses, one renames, one new dimension emerges), and the resulting four dimensions partition 1-vs-3 by detection mode — only model freshness is even potentially output-observable; the other three are strictly attestation-required. This partition is itself the central conceptual contribution.

- Heart sections (§4 Four Dimensions, §5 Inference Receipt, §6 Threat Model) complete: ~5,050 words after seven rounds of adversarial review
- Surrounding sections forthcoming
- Companion benchmark: [qwen-cloud-benchmark](https://github.com/asastuai/qwen-cloud-benchmark)

### [Qwen3 14B Inference Benchmark Across GPU Tiers](https://github.com/asastuai/qwen-cloud-benchmark) — In progress

Cross-provider inference benchmark study, companion to the v0.1 paper's empirical section. Local consumer-tier baseline complete (RTX 5070, 9 cells, methodology documented). Cloud-tier sweep across Lambda, Runpod, AWS pending account provisioning. Headline early finding: throughput stays flat at ~60 tok/s regardless of concurrency, but TTFT degrades up to 1262× from c=1 to c=16 on long workload — consumer-tier is throughput-bound and concurrency-vulnerable.

### [Hermetic Computing](https://github.com/asastuai/kybalion)

A Rust framework formalizing the Seven Hermetic Principles of the Kybalion as computational primitives, paired with established analogues (group homomorphism, DFT, qubits, involutions). Built during a 6-week sustained collaboration with Claude (Anthropic) in early 2026. Paper prepared for arXiv (cs.CY) and SPLASH Onward Essays.

- 87 tests · zero dependencies · pure Rust
- Explicit framing: vocabulary contribution, not cryptographic novelty
- Public reframe from v0.1 → v0.2 documented — caught my own overclaims in the first release, rewrote the artifact in 24 hours, yanked v0.1 from crates.io, republished honestly

### [intent-cipher](https://crates.io/crates/intent-cipher)

Companion crate, published to crates.io. A stream cipher where an "intent" byte string is mixed into the key schedule. Pedagogical artifact — floating-point internals, not production crypto.

### [Opus](https://asastuai.github.io/opus/)

Six-chapter narrative documenting the 6-week collaboration — what the human contributed, what Claude contributed, what neither could have produced alone.

---

## Production DeFi infrastructure

### [SUR Protocol](https://sur-protocol.vercel.app) — Perpetual Futures DEX with agent-native layer

- 12 Solidity contracts · 531 passing tests (Foundry)
- EIP-712 signed orders · Pyth Oracle + Chainlink fallback
- Vault system with tiered and cross-margin liquidation engine
- Agent-native layer: MCP server (25 tools), A2A dark pool, intent engine, x402 payment rails
- Real-time frontend, 15 markets, TradingView charts · [Repo](https://github.com/asastuai/sur-protocol)

### [LiquidClaw Finance](https://liquidclawfinance.com) — ve(3,3) AMM DEX

- 13 smart contracts deployed on BSC mainnet + Base L2 (verified on BscScan)
- ve(3,3) tokenomics: lock, vote, earn — Aerodrome-style flywheel
- AI Vault for automated governance optimization
- Multi-language frontend (EN / ZH)
- Repos: [frontend](https://github.com/asastuai/liquidclaw-amm-) · [contracts](https://github.com/asastuai/liquidclaw-bsc)

### [BaseOracle](https://github.com/asastuai/BaseOracle) — Agent Data Oracle

Pay-per-query market data feeds for AI agents on Base. x402 micropayment protocol integration. Designed for autonomous agent consumption.

### [TrustLayer](https://github.com/asastuai/TrustLayer) — Agent Trust Infrastructure

Trust verification layer for the agentic ecosystem on Base. Reputation scoring for autonomous on-chain agents.

---

## Stack

`Rust` `Solidity` `TypeScript` `Python` `Foundry` `Next.js` `Node.js` `Ollama` `vLLM` `CUDA` `PostgreSQL` `Redis` `Wagmi/Viem` `TradingView`

---

## Background

Nine years in DeFi / crypto ecosystems (2016–2025): PancakeSwap day one on BSC, DAO governance in Lynx and TrustSwap, derivatives across Binance / Aster / Hyperliquid, early-stage token due diligence, deployed on-chain infrastructure. A decade of self-directed markets study alongside (technical analysis, Fed mechanics, equity selection). Four years of daily AI collaboration since ChatGPT launch (Nov 2022). GPU hardware fluency from crypto mining through local LLM deployment (Ollama + Qwen 3.5 on consumer GPU).

Read systems for failure modes before function.

---

## Readings that shape the work

Not favorites — sources that are operative in how I think and show up in what I build:

- **Nietzsche** — complete works; *Thus Spoke Zarathustra* and *Beyond Good and Evil* closest to how I think about system creation. Read with the body, not only with the eyes.
- **Osho** — *El dios que nunca fue* entered at 19 and restructured what thinking meant.
- **The Kybalion** (Three Initiates, 1908) — source text for Hermetic Computing.
- **Tao Te Ching** (Lao Tzu) — grounding for finitude and how to let go of a finished work.
- **Heidegger** — *Being and Time*; philosophy of technology.

Nietzsche and Osho are a chirality — mirror structures with opposed orientations of the same inquiry.

---

## Looking for

Applied research / research engineering roles where interdisciplinary intensity is valued — inference attestation, decentralized ML infrastructure, agent-native systems, crypto × AI intersection.

**Remote · full-time · any timezone · available immediately.**

Open to either employment or substantive contracting / collaboration. Particularly relevant for teams in: verifiable inference, decentralized training networks, agent execution venues, perp DEX architecture with an agent-native angle, or research labs working on attestation primitives for ML.

## Contact

- **Email:** [juancmaisu@outlook.com](mailto:juancmaisu@outlook.com)
- **Based:** Buenos Aires, Argentina
- **Languages:** Spanish (native) · Portuguese (fluent) · English (fully fluent in writing, conversational in speech)
- **Portfolio narrative:** [asastuai.github.io/opus](https://asastuai.github.io/opus/)
- **LinkedIn:** [linkedin.com/in/juan-cruz-maisu-b4b610308](https://www.linkedin.com/in/juan-cruz-maisu-b4b610308/)

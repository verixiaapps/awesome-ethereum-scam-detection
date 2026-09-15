# Awesome Ethereum Scam Detection [![Awesome](https://awesome.re/badge.svg)](https://github.com/sindresorhus/awesome)

> A curated list of tools, datasets, articles, and communities for detecting Ethereum token scams: honeypots, rug pulls, brand-jacked tickers, and adversarial deployer patterns.

The Ethereum ecosystem ships ~400 new ERC-20 contracts per day. A measurable fraction are designed to extract liquidity from retail buyers (honeypots, rug pulls, sandwich-trapped pools, brand impersonation). This list gathers the open tools, public datasets, and signal communities that help users and researchers spot them before money is lost.

## Contents

- [Real-time Detection Tools](#real-time-detection-tools)
- [Static & Bytecode Analysis](#static--bytecode-analysis)
- [Token Risk Scoring APIs](#token-risk-scoring-apis)
- [Honeypot Checkers](#honeypot-checkers)
- [On-chain Forensics](#on-chain-forensics)
- [Public Datasets](#public-datasets)
- [Articles & Research](#articles--research)
- [Communities](#communities)
- [Wallet Add-ons (defensive)](#wallet-add-ons-defensive)
- [Related Awesome Lists](#related-awesome-lists)
- [Contributing](#contributing)

## Real-time Detection Tools

Tools that watch the chain (mempool + new pool creations) and flag scams as they happen.

- [RektRadar](https://rektradar.io/) - Real-time Ethereum scam detector with mempool monitoring, deployer graph analysis (factory pattern + funding chain), and rug pull alerts. Free tier available; 36k+ tokens scanned, ~3.3k flagged as scams (open data). The codebase is open infrastructure (14 microservices on 3 nodes).
- [DexTools — Token Score](https://www.dextools.io/) - Per-token risk score on the most active DEX explorer. Closed-source.
- [DEX Screener — Audits tab](https://dexscreener.com/) - Surface honeypot/audit warnings inline with price charts.
- [HostDeFi](https://hostdefi.com/scan) - Free A+–F token-safety scanner across Solana and 7 EVM chains (mint/freeze authority, liquidity depth, holder concentration). Keyless REST API.

## Static & Bytecode Analysis

Pre-deployment / post-deployment analysis of Solidity sources or compiled bytecode.

- [Slither](https://github.com/crytic/slither) - Solidity & Vyper static analysis framework, ships with detectors for common honeypot patterns.
- [Mythril](https://github.com/ConsenSys/mythril) - Symbolic execution for EVM bytecode. Detects integer overflow, reentrancy, and several scam-relevant flaws.
- [HoneyBadger](https://github.com/christoftorres/HoneyBadger) - Academic honeypot detector for Ethereum smart contracts (heuristic + symbolic).
- [Securify v2](https://github.com/eth-sri/securify2) - Static analyzer from ChainSecurity.
- [Octopus](https://github.com/pventuzelo/octopus) - Multi-chain bytecode analyzer (BTC/ETH/EOS).

## Token Risk Scoring APIs

APIs that return a structured risk score for a given token contract.

- [GoPlus Token Security API](https://gopluslabs.io/token-security-api) - 30+ chains, free tier. Honeypot, ownership, trading-tax, and contract-quality flags.
- [Token Sniffer API](https://tokensniffer.com/) - Automated audit + heuristic risk score for ERC-20s. Web UI is free; API is paid.
- [De.Fi Scanner](https://de.fi/scanner) - Free token risk scanner with REKT vault history.

## Honeypot Checkers

Quick "can I sell this token?" simulations.

- [Honeypot.is](https://honeypot.is/) - Simulates buy/sell to detect honeypots. ERC-20 + BSC.
- [Rugscreen](https://rugscreen.com/) - Honeypot + rug indicator. Fast lookup by contract.
- [QuillCheck](https://check.quillai.network/) - Honeypot + tax + ownership analyzer.

## On-chain Forensics

Tools that map deployer wallets, fund flows, and cluster relationships.

- [Etherscan — Token Approvals & Holders](https://etherscan.io/) - The reference block explorer; deployer history is the first thing to check.
- [Arkham Intelligence](https://www.arkhamintelligence.com/) - Wallet labels, fund flow visualization, free tier.
- [Breadcrumbs](https://www.breadcrumbs.app/) - Visual transaction graph for fraud investigation.
- [Chainalysis Reactor](https://www.chainalysis.com/product/reactor/) - Industry-grade compliance tool (paid, enterprise).

## Public Datasets

Open data on confirmed scams, useful for research, ML training, and replication.

- [SCAM Database (CoinGecko)](https://www.coingecko.com/en/categories/scam) - Tokens flagged on CoinGecko.
- [RektRadar — Open Scams Dataset](https://rektradar.io/blog/) - Aggregated rug-pull and honeypot data with deployer addresses, daily refreshed.
- [The DAO Hack Database](https://medium.com/coinmonks/dao-hacks-explained) - Historical record of DeFi exploits (broader than just scams).

## Articles & Research

- [Why we built RektRadar](https://rektradar.io/blog/posts/why-we-built-rektradar/) - Manifesto on real-time scam detection.
- [How to detect an Ethereum scam token: 7 checks before you buy](https://rektradar.io/blog/posts/how-to-detect-ethereum-scam-token/) - Practical guide.
- [Top 10 brand-jacked tokens on Ethereum](https://rektradar.io/blog/posts/top-10-brand-jacked-tokens-ethereum/) - Data analysis of impersonation patterns.
- [HoneyBadger: detecting honeypots](https://arxiv.org/abs/1902.06976) - Academic paper, IEEE S&P 2019.
- [SoK: Decentralized Finance (DeFi)](https://arxiv.org/abs/2101.08778) - Systematic review of DeFi attack surfaces.

## Communities

- [r/CryptoScams](https://www.reddit.com/r/CryptoScams/) - Community-reported scams with discussion.
- [r/CryptoCurrency](https://www.reddit.com/r/CryptoCurrency/) - Largest crypto subreddit; scam discussion in daily threads.
- [r/EthereumScams](https://www.reddit.com/r/EthereumScams/) - Smaller, more focused.
- [Web3 is Going Just Great](https://web3isgoinggreat.com/) - Curated chronicle of crypto incidents (humorous tone).

## Wallet Add-ons (defensive)

Browser extensions that flag suspicious contracts at signing time.

- [Wallet Guard](https://www.walletguard.app/) - Pre-transaction warnings for phishing + scam contracts.
- [Pocket Universe](https://www.pocketuniverse.app/) - Transaction simulator + warnings.
- [Fire](https://www.joinfire.xyz/) - Pre-sign simulation with risk verdicts.

## Related Awesome Lists

- [awesome-ethereum-security](https://github.com/crytic/awesome-ethereum-security) - Static analysis, formal verification, reverse engineering.
- [awesome-web3-security](https://github.com/fabionoth/awesome-web3-security) - Broader Web3 security including bug bounties and CTFs.
- [Awesome-Smart-Contract-Security](https://github.com/saeidshirazi/Awesome-Smart-Contract-Security) - Smart contract security materials and resources.

## Contributing

Pull requests welcome. Please follow the existing format:

- One bullet per entry.
- Link the canonical project URL (not affiliate links).
- One-sentence description, factual and concise.
- No marketing language ("revolutionary", "best", etc.).
- Disclose maintainer affiliation if you're submitting your own project.

Maintained by [@mik3fly-lab](https://github.com/mik3fly-lab). Open issues for additions, removals, or category disputes.

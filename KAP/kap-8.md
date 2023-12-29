---
kap: 8
title: .hbar TLD migration
type: Action
subproject: KNS
sponsor:
author: Ken Anderson
status: Draft
created: 2023-12-29
updated: 2023-12-29
---

## Abstract

Migration of the `.hbar` TLD to the KNS protocol.

## Rationale

Kabuto Name Service is a self-sufficient DNS-like protocol built strictly in smart contracts and deployed to Hedera's Smart Contract Service. It is the only trully decentralized protocol for domain names in the Hedera ecosystem: smart contract-based, zero external database requirement, automatically deduplicating, and space optimizing.

`.hbar` is the most recognizable TLD in the Web3 space as it relates to Hedera.

## Clearance

| Organization       | Cleared? |
| ------------------ | -------- |
| IANA               | TRUE     |
| Hashgraph.name     | FALSE    |
| KNS                | TRUE     |
| UnstoppableDomains | TRUE     |

## Specification

The HBAR TLD shall be issued as `.hbar`.

This TLD will be issued as a KNS TLD NFT.

The admin of this TLD shall be 0.0.xxxxxx.

Purchases shall follow the KNS default payment model:

- a = Annual purchase price
- n = Number of years purchased
- Total = t = a \* n
- Infrastructure Share = i = $2.00 \* n
- Development Share = (t - i) \* 0.50
- Co-op Share = (t-i) \* 0.25
- TLD Admin Share = (t-i) \* 0.25

Domain resolution shall be made using a KNS Resolver or KNS Resolver-compatible relay.

Domain purchases will include an initial block of 18 records. Additional blocks of 18 records can be purchased as a multiple of the base domain price. For example, if a domain costs $5 per year, that domain comes with 18 records. If the purchaser requires 50 records, for example, that would require purchasing an additional two blocks of records for a total of three blocks of records (18 \* 3 = 54 total records available) which would cost $15 per year.

Domains can be purchased using standard characters or special characters. Standard characters are those that fit into the ASCII encoding set. Any characters that fall under the non-ASCII encoding set, or require multiple unicode points in the UTF-8 encoding set, will be categorized as special characters. Domains containing any special characters will be priced at double the corresonding standard character domain price.

Additionally, character count affects pricing. Domains with three or more standard characters is the baseline for pricing. Setting that price allows for all other prices to be calculated. Standard domains with 2 characters are 10x the baseline price. Standard domains with 1 character are 100x the baseline price. Again, special domains are twice the price of their standard counterparts.

The pricing of domains under this TLD shall follow the following pricing model:

| Characters | Standard | Special |
| ---------- | -------- | ------- |
| 3+         | $5       | $10     |
| 2          | $50      | $100    |
| 1          | $500     | $1000   |

## Open Issues

Currently, hashgraph.name (HGN) is the sole issuer of `.hbar` domains. Issuing `.hbar` domains on KNS will result in duplicate domain issuance between hashgraph.name and KNS. This creates an additional problem for wallets in the ecosystem. If there are two uncoordinated domain name resolvers in the Hedera ecosystem, which does a wallet provider resolve to? It can create confusion for users if sending to one `.hbar` domain results in another user receiving the funds.

The options for resolution here are:

- KNS & HGN pre-check each domain sale against each others' resolver to ensure that neither sells a domain already issued on the other protocol. This approach affords no technical guarantee of non-collision.
- HGN adopts KNS as an infrastructure layer, becomes the TLD admin for `.hbar` and sells `.hbar` however they want. This approach guarantees non-collision of domains since the smart contracts handle the domain checks.

## References

- [Hedera Domains Service](https://www.hedera.domains/)
- [Kabuto Name Service ("KNS")](https://kabuto.sh/)
-

## Copyright / License

This document is licensed under the Apache License, Version 2.0 -- (<https://www.apache.org/licenses/LICENSE-2.0>)

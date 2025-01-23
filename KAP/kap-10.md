---
kap: 10
title: .bit TLD
type: Information
subproject: KNS
sponsor: Hashgraph Online
author: Michael Kantor
status: Draft
created: 2025-01-23
deadline: 2025-01-30
---

## Abstract

Issuance of `.bit` as a TLD on the KNS protocol.

## Rationale

Hashgraph Online is building a fully on-chain internet using Hedera and HCS standards. The .bit TLD will serve as the native domain for the planned Hashgraph Online browser, enabling direct resolution of on-chain resources.

The upcoming browser will integrate with HCS standards to provide file storage (HCS-1), registries (HCS-2), recursion (HCS-3), and other decentralized services. By controlling the .bit namespace, Hashgraph Online can ensure consistent domain resolution and resource access across their future browser ecosystem.

## Clearance

| Organization       | Cleared? |
| ------------------ | -------- |
| IANA               | TRUE     |
| Hashgraph.name     | TRUE     |
| KNS                | TRUE     |
| UnstoppableDomains | TRUE     |

## Specification

The Hashgraph Online TLD should be issued as `.bit`.

This TLD will be issued as a KNS TLD NFT.

The admin of this TLD shall be 0.0.8153909.

Purchases shall follow the KNS default payment model with a modification to the default annual purchase price. 

Annual purchase price (a) is set by TLD admin (0.0.8153909) to $20.

- a = Annual purchase price
- n = Number of years purchased
- Total = t = a \* n
- Infrastructure Share = i = $2.00 \* n
- Development Share = (t - i) \* 0.50
- Co-op Share = (t-i) \* 0.00
- TLD Admin Share = (t-i) \* 0.50

Browser Integration:
- The .bit TLD will be natively resolved in the planned Hashgraph Online browser
- Resolution will utilize the KNS Resolver within the browser
- Additional integrations for the extension will be powered by various HCS standards like HCS-1, HCS-2, HCS-3, etc. 

## Open Issues

## References

- [Hashgraph Online](https://www.hashgraphonline.com/)
- [Kabuto Name Service ("KNS")](https://kabuto.sh/)

# Risks
 - .bit TLD was established by Namecoin https://www.nfthistory.org/wiki/.bit_Domains. It is not currently a registered TLD in the IANA registry and does not function without a chrome extension.

## Copyright / License

This document is licensed under the Apache License, Version 2.0 -- (<https://www.apache.org/licenses/LICENSE-2.0>)

---
kap: 6
title: Bug bounty reward to cobb.ℏ
type: Information
subproject: KNS
sponsor: LaunchBadge
author: Ken Anderson (@kenthejr)
status: Draft
created: 2023-02-21
updated: 
deadline: 2023-02-24
---

## Abstract

Issuance of 1,000ℏ to cobb.ℏ as reward for discovering a bug on the [KNS dApp](https://ns.kabuto.sh/).

## Rationale

On January 4th, 2023, Twitter use @CryptoCobbb discovered a bug in the KNS dApp which showed a cached address record for his domain where no address record was recorded.

Upon investigation, it was confirmed that:

1. Domain NFT ownership was correct
2. The smart contracts reflected the correct state of the related domain records
3. The KNS resolver incorrectly returned a cached address

The KNS resolver was updated and the correct response was confirmed. Additional monitoring was put in place to periodically check for such inconsistencies in the future.

*NOTE: The KNS Resolver is a convenience feature in beta at the time of this discovery. The KNS contracts can be queried for direct access to the "source of truth".*

## Issuance

COOP Budget balance at the time of this proposal is 50,332ℏ.

1,000ℏ to be issued to the KNS address `cobb.ℏ` from the COOP Budget.

## Open Issues

N/A

## References

- [Kabuto Name Service ("KNS")](https://kabuto.sh/)

## Copyright / License

This document is licensed under the Apache License, Version 2.0 -- (<https://www.apache.org/licenses/LICENSE-2.0>)

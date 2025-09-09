# BECKN-010:Keyword Definitions for Technical Specifications

## License:
This document is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

![Creative Commons License](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)

## Category:
Keywords for Technical Specification

## Published on:
January 21, 2022

## Last Updated on:
July 8th, 2024

## History: 
Click on this [link](https://github.com/beckn/protocol-specifications/commits/core-1.2-release/docs/BECKN-010-Keyword-Definitions-for-Technical-Specifications.md) to view the history of changes to this document

## Issues:
To view issues related to this document, click on this [link](https://github.com/beckn/protocol-specifications/issues?q=is%3Aissue+label%3ABECKN-010)

## Discussions:
To view discussions related to this document, click on this [link](https://github.com/beckn/protocol-specifications/discussions?discussions_q=label%3ABECKN-010)

## Authors:
1. [Ravi Prakash](https://github.com/ravi-prakash-v)

## Reviewers:
1. [Sujith Nair](https://github.com/sjthnrk)
2. [Pramod Varma](https://github.com/pramodkvarma)
3. [Venkatraman Mahadevan](https://github.com/venkatramanm)


# Abstract

This document outlines the definitions of key words that are commonly used in technical specifications, standards, and protocols. The aim is to provide a uniform interpretation of these terms to avoid ambiguity and misinterpretation.

# Introduction

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [rfc 2119](https://datatracker.ietf.org/doc/html/rfc2119). These definitions aim to ensure that the terms are understood precisely and consistently to avoid confusion in the interpretation of standards, specifications, and protocols.

## Examples and Correct Usage

In this section, we provide examples that demonstrate the correct usage of the key words defined in this document. The examples are related to a hypothetical Beckn Application Platform (BAP) that interacts with a Beckn Provider Platform (BPP) using beckn protocol APIs.

### Example 1: Using "REQUIRED" and "MUST"

- REQUIRED. The BPP MUST implement the `search` endpoint to receive an `Intent` object sent by BAPs.
- REQUIRED. The BPP MUST return a catalog of products on the `on_search` callback endpoint specified in the `context.bpp_uri` field of the `search` request body.
- REQUIRED. Any provider-related information like `name`, `logo`, `short_desc` MUST be mapped to the `Provider.descriptor` schema.
- REQUIRED. If the BPP does not want to respond to a `search` request, it MUST return an `ack.status` value equal to `NACK`.

### Example 2: Using "RECOMMENDED" and "SHOULD"
- RECOMMENDED. Upon receiving a `search` request, the BPP SHOULD return a `Catalog` that best matches the `Intent`. This can be done by indexing the catalog against the various probable paths in the `Intent` schema relevant to the use case.

## Conclusion

The definitions provided in this document are intended to clarify the interpretation of key terms used in technical specifications, standards, and protocols. Adherence to these definitions will ensure a consistent understanding and implementation of such documents.

## Acknowledgements

The authors would like to thank the following people for their support and contributions to this document. 

* Pramod Varma (Beckn Foundation)
* Sujith Nair (Beckn Foundation)
* Venkataramanan Mahadevan (Humbhionline)

> Note : This document is subject to change and may be updated to include additional terms or to refine existing definitions.



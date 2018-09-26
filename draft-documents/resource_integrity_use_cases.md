# Resource Integrity Use Cases

Authors: Ganesh Annan and Kim Hamilton Duffy

Currently, the Web provides a simple yet powerful mechanism for the dissemination of information via hyperlinks. Unfortunately, there is no generalized mechanism that enables verifying that a fetched resource has been delivered without unexpected manipulation. [Resource Integrity Proofs](https://github.com/WebOfTrustInfo/rwot7/blob/master/topics-and-advance-readings/resource-integrity-proofs.md) enable verification of any representation of a resource from any type of link. This paper describes how RIP solves use cases inspired by production deployments of self-sovereign technologies. One is the problem of [Verifiable Displays](https://github.com/WebOfTrustInfo/rwot7/blob/master/topics-and-advance-readings/verifiable_displays.md), which seeks to ensure the rendering of the VC content matches what the issuer intended. Another is verifying integrity of referenced data; for example, if the referenced data is in a mutable store. Lastly, we discuss how RIPs can be used to layer Object Capabilities on top of legacy systems.


### Meeting Regulatory Compliance
Organizations must provide documentation to regulators in order to maintain compliance. We can implement software to meet the full requirements of this use case by adding RIPs to the already composable Lego-like ecosystem of interoperable decentralized technologies such as DIDs, VCs, and OCAPs -- and by combining this ecosystem with a cryptographically auditable system, such as a blockchain. When an organization is preparing supporting documentation to meet compliance, they can post one or more RIPs and an OCAP for accessing each resource to a blockchain. This OCAP only grants access to the regulator and only to the specific items and for the duration that they need. Posting the RIP to a blockchain enables discoverability of the resource and establishes a proof of existence. The tamper-evident characteristics of the blockchain prove that the data existed as some point in the past, establishing trust via the cryptosystem rather than requiring it in the organization. The regulator then uses the delegated OCAP to dereference the url in the RIP and to ensure the data was not changed since the time of submission.

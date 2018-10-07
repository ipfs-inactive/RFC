- Feature Name: ipns-over-dns
- Start Date: 2018-09-22
- Current Status: DRAFT
- Owner: Lars Gierth - @lgierth
- RFC PR: (leave this empty)
- IPFS Issue: (leave this empty)

- node is very thin so we can ship it *anywhere*, anyone can run their own ipns-over-dns node

- resolution over dns (:53)
- resolution over api (:8080/api/v0/resolve for browsers)
- conceptually doesn't concern itself with dns zones
- implemented in rust and packaged for openwrt
- an evolution of these: dns and ipns and dnslink

- TODO: think more about integration with DNSSEC, and usage of existing crypto headers.
  - a variation of this design could well be a great approach to
    securely decentralizing existing dns infrastructure and usage (but not the root zone itself)

- Q: how is this different from the existing pubsub namesys?
  - it's not a replacement, but complements it
- Q: how do ipns, dnslink, ipns-pubsub, ipns-dns relate?

- pubsub topic is `sha256("/ipns/.well-known/all")`
- go-ipns-dns does:
  - :53
  - :8080/api/v0/resolve
  - pubsub listening
  - optional: dns-over-tls
  - optional: maintain entries as a crdt-on-ipfs
  - optional: store entries to disk
  - optional: port 8080 redirect Host=qmfoo.ipns.name to ipfs.io/ipns/QmFoo


# Summary
[summary]: #summary

This document proposes a new IPNS namesys based on PubSub and DNS.
Name updates are published to a well-known PubSub topic,
and thin resolver daemons listen to these updates.
There are well-known highly-available global resolvers,
and infinite other, preferrably more local, resolvers.
Names are resolved as DNS TXT records, or via a minimal IPFS HTTP API subset.


# Motivation
[motivation]: #motivation

Why are we doing this? What use cases does it support? What is the expected outcome?

It's intended to integrate with existing Internet infrastructure seamlessly,
and to be fast at publishing name changes and even faster at resolving names,
while also maintaing IPNS's distributed and resilient nature.



# Guide-level explanation
[guide-level-explanation]: #guide-level-explanation

Explain the proposal as if it was already included in the protocol and you were teaching it to another contributor on this project. That generally means:
- Introducing new named concepts.
- Explaining the feature largely in terms of examples.
- Explaining how programmers and other contributors should *think* about the feature, and how it should impact the way they use the software or protocols being modified. It should explain the impact as concretely as possible.
- If applicable, provide sample error messages, deprecation warnings, or migration guidance.
- If applicable, describe the differences between teaching this to existing contributors and new contributors.
For implementation-oriented RFCs (e.g. for changes to a protocol or its implementations), this section should focus on how protocol contributors should think about the change, and give examples of its concrete impact. For policy RFCs, this section should provide an example-driven introduction to the policy, and explain its impact in concrete terms.


# Reference-level explanation
[reference-level-explanation]: #reference-level-explanation

This is the technical portion of the RFC. Explain the design in sufficient detail that:
- Its interaction with other features is clear.
- It is reasonably clear how the feature would be implemented.
- Corner cases are dissected by example.

The section should return to the examples given in the previous section, and explain more fully how the detailed proposal makes those examples work.

```
> ipfs name publish -v -k schmars QmFoo
publishing /ipns/QmSchmars to pubsub: ok
publishing /ipns/QmSchmars to dns: ok
publishing /ipns/QmSchmars to kad-dht: 5/7 -- timeout

> ipfs resolve -v -r false /ipns/schmars.net
found /ipns/QmSchmars via dnslink

> ipfs resolve -v -r false /ipns/QmSchmars
subscribed to /ipfs/QmFoo via pubsub
found /ipfs/QmFoo via dns

```

```
> dig +short TXT qmschmarsbase32.ipns.name
ipns=<entry incl. sig and key>

> dig +short NS ipns.name
ns1.ipns.name
ns2.ipns.name

> ipfs config Namesys.DNS.Resolvers
["ipns.name", "ipns.local", "ipns.olsr", "cloudflare-ipns.com", "ipnsname8jh89n1c2xc12.onion"]

> ipfs config Namesys.DNS.StrictTTL
false

```


# Drawbacks
[drawbacks]: #drawbacks

Why should we *not* do this?


# Rationale, Prior Discussion and alternatives

[alternatives]: #alternatives
- Why is this design the best in the space of possible designs?
- What other designs have been considered and what is the rationale for not choosing them?
- What is the impact of not doing this?
- What prior discussions have occurred that led to this RFC (include links where possible)


# Unresolved questions
[unresolved]: #unresolved-questions

- What parts of the design do you expect to resolve through the RFC process before this gets merged?
- What parts of the design do you expect to resolve through the implementation of this feature before stabilization?
- What related issues do you consider out of scope for this RFC that could be addressed in the future independently of the solution that comes out of this RFC?

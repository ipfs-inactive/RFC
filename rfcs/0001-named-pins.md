- Feature Name: named_pins
- Start Date: 27.03.2017
- Current Status: DRAFT
- Owner: Voker57
- RFC PR: (leave this empty)
- IPFS Issue: (leave this empty)


# Summary
[summary]: #summary

Pins with hierarchical names assigned to them.

# Motivation
[motivation]: #motivation

Pins require names to be easily organized.

# Guide-level explanation
[guide-level-explanation]: #guide-level-explanation

Every pin is identified by a unique string of characters. Using slashes ('/') as separators is encouraged, but they only have special meaning when adding a new pin: path ending in a slash will have CID of added data appended to it.

Examples of pin names:

```
added/QmS4ustL54uo8FzR9455qaxZwuMiUhyvMcX9Ba8nUH4uVv
movies/TPB.AFK/TPB.AFK.mkv
```


# Reference-level explanation
[reference-level-explanation]: #reference-level-explanation

Pins are stored in key-value database, indexed by pin name. Looking up pins by prefix (like "added/") should be a cheap operation. Searching, deleting, renaming and copying items by name and their recursive versions are available. Adding a pin with name ending in slash (i.e. "added/") results in creation of pin with concatenation of given prefix with content CID (i.e "added/QmS4ustL54uo8FzR9455qaxZwuMiUhyvMcX9Ba8nUH4uVv")

# Drawbacks
[drawbacks]: #drawbacks

Looking up pin by CID is not as fast as original implementation. Can be solved by additional index. Not using DAG structure means DAG manipulation tools can't be used for pin trees.

# Rationale, Prior Discussion and alternatives
[alternatives]: #alternatives

Storing named pins in datastore allows simple and fast lookups and prefix operations, while maintaining lean codebase.

One alternative is storing pins in MFS: Uniform, but causes pins to be exposed to the network and requires complicated code to avoid race conditions and an additional layer of abstraction to map pins to unixfs.

# Unresolved questions
[unresolved]: #unresolved-questions


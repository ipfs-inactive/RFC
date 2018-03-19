- Feature Name: bootstrapping-rfc-process
- Start Date: 09 February 2018
- RFC PR: (leave this empty)
- IPFS Issue: (leave this empty)

# Summary
[summary]: #summary

Begin using an RFC process. Initially use a structure similar to the process used by the maintainers of Rust lang, as described in https://github.com/rust-lang/rfcs

# Motivation
[motivation]: #motivation

Establish a clear, repeatable process for people to propose ideas and make decisions in a way that
1. Allows everyone to see what decisions have been made and how they were made
2. Allows everyone to see what proposals have been proposed and comment on them or suggest changes
3. Works for a globally distributed group of contributors to discuss and make decisions asynchronously
4. Can be replicated/repeated in sibling projects or spinoff projects like libp2p, IPLD, etc.

# Guide-level explanation
[guide-level-explanation]: #guide-level-explanation

_[Cribbed directly from [Rust-lang/rfcs README](https://github.com/rust-lang/rfcs#rust-rfcs)]_
Many changes, including bug fixes and documentation improvements can be implemented and reviewed via the normal GitHub pull request workflow.

Some changes though are "substantial", and we ask that these be put through a bit of a design process and produce a consensus among the IPFS community and the sub-teams.

The "RFC" (request for comments) process is intended to provide a consistent and controlled path for new features to enter the language and standard libraries, so that all stakeholders can be confident about the direction the language is evolving in.

# Reference-level explanation
[reference-level-explanation]: #reference-level-explanation

The proposed RFC process is described in the [README](../README.md). It's a modified version of  the process used in the [Rust lang RFCs repository](https://github.com/rust-lang/rfcs/blob/752a02115e49c114e2d6b5247c410da69aac505c/README.md), which is dual-licensed under MIT and Apache2 licenses.

Go to [README.md](../README.md) to review and comment on the details of the proposed process. _[Note: when this RFC is merged, we should update this link to point to the README.md in the specific commit that got merged.]_

# Drawbacks
[drawbacks]: #drawbacks

Why should we *not* do this?

# Rationale and alternatives
[alternatives]: #alternatives

- It's time to establish a clear, reliable process for proposing changes and tracking the decisions we've made. If done right, this will do a lot to reduce confusion, encourage participation, and encourage a high level of transparency around important decisions that impact the project.
- Rather than starting from scratch, we're starting with the process that is being used, successfully, by a project we admire -- the Rust language
- The process described here is sufficiently minimal that we can implement it without much confusion and will be able to modify/improve it over time
- This process is generic enough that we can fork it and repeat on spinoff projects like libp2p, IPLD, etc


# Unresolved questions
[unresolved]: #unresolved-questions

- This process presumes the existence of _working groups_ and describes some of the responsibilities of working groups. Those ideas are subject to change in the next RFC [0002-ipfs-governance.md] which will outline our governance structure. That RFC might change the responsibilities of working groups or replace the notion of working groups with some other structure (ie. sub teams, product groups, functional groups etc.). Because of that, any reference to working groups in this current RFC should be treated as provisional until the governance RFC is merged.

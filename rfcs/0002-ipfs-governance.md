- Feature Name: ipfs-governance
- Start Date: 2018-02-09
- RFC PR: (leave this empty)
- IPFS Issue: (leave this empty)

# Summary
[summary]: #summary

Establish a basic, adaptable governance structure for IPFS and its surrounding protocols and projects. Design it to minimize bureaucracy, maximize transparency, and to allow the overall structure of teams/working groups etc. to evolve over time in response to practical needs.

This RFC describes the initial version of the "kernel" of the IPFS + libp2p org(s)

# Motivation
[motivation]: #motivation

IPFS and its surrounding projects have reached a point of maturity where we need a more explicit structure guiding the governance of the code bases, the protocols, the specifications, and the activities of our related projects. There are dozens of full-time contributors working on related code bases, designs and infrastructure, with thousands of people contributing to github and the [discussion forums](https://discuss.ipfs.io) and over 600 unique contributors submitting changes to our git repositories. A large and ever-growing number of applications and projects now rely on the code bases that we maintain.   We have passed beyond the point where any one person can stay up to date with every important decision and every new idea, bug or feature that is in the works. We need a reliable structure for contributors to focus their energy, ideas and time to the aspects of our projects that are most important to them while ensuring that everyone is working in concert, with sufficient coordination, information sharing, and cross-team feedback for everyone to create amazing shared momentum towards our big-picture goals.

This RFC describes a structure that's designed to provide clarity and direction to the project, enabling individual contributors to focus their time and energy on the areas they are most interested.

As a consequence from this structure, we achieve another important goal of creating welcoming entry points for the community to subscribe to bodies of work and research. These entry points are curated by the working groups themselves and should serve the purpose of encouraging new users, engaging with them and enabling contribution as simply as possible.

_This RFC is partially motivated by the IPFS Working Groups proposal that @diasdavid submitted in [this PR](https://github.com/ipfs/ipfs/pull/285/files), which predates this repository and the RFC process. Some of the text in this RFC comes from that PR._

# Guide-level explanation
[guide-level-explanation]: #guide-level-explanation

The IPFS Project  is governed by a collection of working groups. _working groups_ (WG) are teams of people that are appointed to research, develop and deploy work under the scope that the working group is focused. While its common to be involved in multiple working groups, most people's work revolves primarily around a single functional group or product group.

Its useful to distinguish between two types of working groups: _product groups_ and _functional groups_. _Product groups_ work on products or services with discrete users, use cases, functionality and release roadmaps. _Functional groups_ tackle ongoing, cross-cutting concerns like developer enablement or community engagement.

We want working groups to emerge, function, and dissolve in response to community needs. To accommodate this, working groups are created using the RFC process -- people who want to form a working group must propose it in an RFC and get that RFC merged.  That open-ended invitation to create working groups is matched by clear protocols describing when and how working groups should be dissolved.

# Reference-level explanation
[reference-level-explanation]: #reference-level-explanation

Each Working Group is able to set its own pace and objectives quarterly.

## The Core Working Group

The core working group has three main functions:

1. Set overall direction of the project
2. Keep the Working Group lifecycle running smoothly
3. Run the RFC process, delegating the decision-making to WGs whenever possible

### The Core Working Group is Responsible for
- Delivering high-level, long-term strategic OKRs in advance of other WGs doing their OKR plannings, so everyone can use them as guidance for crafting and prioritizing their OKRs
- Enforcing the WG lifecycle protocol: Guides formation if WGs, supports functioning of WGs, and dissolves them according to the WG lifecycle protocol
- Keep the RFC process moving -- either delegating decision power to whichever WG should make the decision or merging/rejecting the RFC themselves.
- Dissolves WGs (enforces protocol for lifecycle)

### Prerogatives of the Core Working Group
- The Core WG can assign/delegate ownership of a product, library, specification, or problem domain to another WG, giving that WG autonomy to make decisions as it sees fit.

### Membership in the Core Working Group
TODO: Who is in the Core Group? How do we decide? Aim for 3-5 people. 10 is too big

## Product groups and Functional Groups

Working groups

- When a WG wants something formally ratified, or wants another WG to pick it up, they should be encouraged to follow protocols like submitting RFCs and writing/updating specs.
- Functional group doesn’t form until there are multiple teams that rely on those things
- Product groups always define OKRs, Functional Groups occasionally define OKRs
- Product/Service Groups might actually deliver services to other groups rather than building actual products
- People _can_ belong to multiple Product Groups, but should avoid over committing
- Leads of Product groups are responsible for keeping track of whether people are over committed (including keeping track of whether people have overcommitted across multiple product groups)
- Functional Groups don’t have a hierarchy, but Product Groups are a tree. Product groups subdivide when a Product Group gets bigger than 3-5 people so that the group has a manageable amount of OKRs

## Working Group Lifecycle

1. Design
2. Proposal (RFC)
3. Formation
4. Functioning
5. Dissolving

## Failsafe: BDFL

As a failsafe, if all other processes and protocols fail, Juan Benet (@jbenet) will step in and exercise his prerogatives as the founder and initial creator of these projects.

# Drawbacks
[drawbacks]: #drawbacks

Why should we *not* do this?
- If we don't set the right protocols for creation & dissolution of working groups, we will end up with a lot of confusion about who is responsible for what, meaning balls will get dropped, people will get frustrated, and productive time will be wasted.

# Rationale and alternatives
[alternatives]: #alternatives

- Why is this design the best in the space of possible designs?
- What other designs have been considered and what is the rationale for not choosing them?
- What is the impact of not doing this?

# Unresolved questions
[unresolved]: #unresolved-questions

**BLOCKERS**: Questions to resolve before merging this RFC:
- [ ] Research other projects/orgs (5-6). Compare our process against 2-3 of them. Also research how they define the boundaries and responsibilities of Core group.  (see document: [Comparison of Open Source Governance Structures](https://docs.google.com/document/d/1vV-8mlqyXsgs_sb9PCuGtqoRlLrvSSjOvJNOZWmZjuI/edit?usp=sharing))
- [ ] Need: Ways to make sure individuals don’t get spread too thin.
    - People can only captain 1 WG at a time?
    - Distinguish between product groups and WGs?
    - Work assignments should happen on Product groups
- [ ]  Define: How do OKRs percolate up?
    - Some options:
      - The objectives percolate up, becoming KRs in their parent group's OKRs list
      - OKRs only exist at the leaves, not at intermediary levels
      - Teams write higher-level OKRs that condense and summarize their OKRs so they can be
      to percolated upwards
- Define membership of Core WG
    - Are top level Product Captains automatically in Core Group?


Questions to resolve through implementation
- Need to test this process with 3-4 WGs and update the protocol as necessary
- Investigate how other teams percolate OKRs upward and create an RFCs
- Need: Support Structure for people Proposing or Captaining a WG
    - Note: In Rust, the leader of a WG must be part of the core team

Questions that are out of scope

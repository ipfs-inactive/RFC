- Feature Name: ipfs-governance
- Start Date: 2018-02-09
- RFC PR: (leave this empty)
- IPFS Issue: (leave this empty)

# Summary
[summary]: #summary

Establish a basic, adaptable governance structure for IPFS and its surrounding protocols and projects. Design it to minimize bureaucracy, maximize transparency, increase the autonomy of groups across the IPFS ecosystem, and to allow the overall structure of teams/working groups etc. to evolve over time in response to practical needs.

This RFC describes the initial version of the "kernel" of the IPFS + libp2p org(s)

_This RFC is partially motivated by the IPFS Working Groups proposal that @diasdavid submitted in [this PR](https://github.com/ipfs/ipfs/pull/285/files), which predates this repository and the RFC process. Some of the text in this RFC comes from that PR._

# Motivation
[motivation]: #motivation

## Size and Maturity of the Projects

IPFS and its surrounding projects have reached a point of maturity where we need a more explicit structure guiding the governance of the code bases, the protocols, the specifications, and the activities of our related projects. There are dozens of full-time contributors working on related code bases, designs and infrastructure, with thousands of people contributing to github and the [discussion forums](https://discuss.ipfs.io) and over 600 unique contributors submitting changes to our git repositories. A large and ever-growing number of applications and projects now rely on the code bases that we maintain.   We have passed beyond the point where any one person can stay up to date with every important decision and every new idea, bug or feature that is in the works. We need a reliable structure for contributors to focus their energy, ideas and time to the aspects of our projects that are most important to them while ensuring that everyone is working in concert, with sufficient coordination, information sharing, and cross-team feedback for everyone to create amazing shared momentum towards our big-picture goals.

This RFC describes a structure that's designed to provide clarity and direction to the project, enabling individual contributors to focus their time and energy on the areas they are most interested.

## Small Teams, but no Lonely Hackers

Over the past 3 years we have experimented with a variety of team sizes and levels of coordination across teams. We find that contributors are most effective, and happiest, when they get to be on small teams (2-5 full time people). When the teams get bigger than this, the work becomes unfocused, communication becomes harder, and management overhead skyrockets. When teams are too small, especially when there is only one full time person on a "team", they easily become overloaded with responsibilities and, due to the globally distributed nature of our community, they become isolated.  

This RFC includes constraints on the size, formation, and sub-division of teams. Those constraints are aimed at encouraging people to work in small teams while maintaining regular communication with other related teams and groups.

## Self-organizing ways for People to Coordinate Across Teams

When multiple teams have a shared focus or shred need, they can form a Working Group to convene conversations and align work around those focuses or needs.

## Welcoming Entry Points and Clear Funnels for Engagement

Another important goal of these changes is to create welcoming entry points for the community to subscribe to bodies of work and research. These entry points are curated by the Teams and Working Groups themselves. These Teams and Working Groups  should serve the purpose of encouraging new users, engaging with them and enabling contribution as simply as possible.

# Guide-level explanation
[guide-level-explanation]: #guide-level-explanation

The IPFS Project  is governed by a collection of _Teams_ and _Working Groups (WGs)_. These Teams and Working Groups are appointed to research, develop and deploy work under their declared scope/focus.

We distinguish between _Teams_ and _Working Groups_.
- _Teams_ are small groups who work on products (go-ipfs, ipfs-cluster, ipfs-companion) or services (public gateways, testing infrastructure, etc). They have discrete users, use cases, functionality and release roadmaps. A Team must have at least 2 people (preferably 3 people) whose Full Time efforts are primarily focused on that Team's work, and they should avoid getting bigger than 8-10 people
- _Working Groups_ tackle ongoing, cross-cutting concerns. Some Working Groups focus on shared needs like security, benchmarking or community engagement. Others focus on shared goals and priorities like Enabling Development of Decentralized Applications, or Supporting Decentralized Data Stewardship. Working Groups do not have a size limit, and don't always have people focused full-time on that group's work.

It's common for a person to belong to a single team and multiple Working Groups. Teams are relatively focused with a small range of direct collaborators while Working Groups are cross-team and cross-functional with a larger range of collaborators.  While most of their work revolves around a single Team, the Working Groups allow them to be in conversation with many people from many teams about cross-cutting concerns.  

We want Teams and Working Groups to emerge, function, and dissolve in response to community needs. To accommodate this, Teams and Working Groups are created using the RFC process -- people who want to form a Team or Working Group must propose it in an RFC and get that RFC merged.  That open-ended invitation to create Teams and Working Groups is matched by clear protocols describing when and how working groups should be dissolved.

# Reference-level explanation
[reference-level-explanation]: #reference-level-explanation

Each Team or Working Group is able to set its own pace and objectives quarterly.

## Product/Service Teams and Working Groups

### Teams (Product Teams and Service Teams)

Some Teams focus on producing and maintaining _products_ (ie. go-ipfs, ipfs-cluster, etc.) while other Teams focus on providing _services_ for their audiences to rely on (ie. Infrastructure). The rules and guidelines here apply equally to both Product Teams and Services Teams,

- A Team must have at least 2 people whose Full Time efforts are primarily focused on that Team's work.
- Teams define  [Objectives and Key Results](https://weekdone.com/resources/objectives-key-results) (OKRs) every quarter. Members of a Team primarily derive their tasks from those OKRs.
- Some Teams have multiple products or services under their view. Others are focused on a single product or service. Teams can also _add_ products and services to their portfolio at any time.
- **Teams should subdivide when the Team gets bigger than 2-5 Full Time people** so that the group has a manageable amount of OKRs. When a  Team becomes big enough to subdivide and specialize, they can split into sub-teams. In that case, those sub-teams can create their own OKRs but they must coordinate with each other to create shared, overarching OKRs and Roadmaps. This allows external audiences to follow the work of the overall Team without having to read every sub-team's OKRs.
- People _can_ belong to multiple Teams, but should avoid over committing. **People whose time is split across teams do not count toward either Team's 2-person minimum.**
- Captains (team leads) are responsible for keeping track of whether people are over committed (including keeping track of whether people have overcommitted across multiple Teams)

### Working Groups

- A Working Group can't form until there are multiple Teams that need it to exist
- Working Groups don't necessarily have any people allocating full-time effort to that group's goals. As a result, Working Groups are likely to push work into the OKRs of Teams, which can more easily allocate people's time.
- Working Groups occasionally define OKRs, but they don't have to define OKRs every quarter.
- Working Groups don’t necessarily subdivide when they get bigger. Unlike Teams, which are encouraged to form a tree of sub-teams when they grow bigger than ~5 people, Working Groups are able to convene larger groups of stakeholders.

### The Core Working Group

This whole structure and process relies on a Core Working Group, which acts in service of the other Teams and Working Groups to maintain a healthy, adaptable system for decision making and coordinated planning.

The Core Working Group has three main functions:

1. Set overall direction of the project
2. Keep the Working Group lifecycle running smoothly
3. Keep the RFC process running smoothly, delegating the decision making to Working Groups whenever possible

### The Core Working Group is Responsible for
- Delivering high-level, long-term strategic OKRs
- Enforcing the lifecycle protocol for Teams and Working Groups: Guides formation of Teams/WGs, supports functioning of Teams & WGs, and dissolves them according to the lifecycle protocol
- Keep the RFC process moving -- either delegating decision power to whichever Team/WG should make the decision or, when no other group matches the RFC, merging/rejecting the RFC themselves.

### Prerogatives of the Core Working Group
- Core team can assign/delegate ownership of a product, library, spec, problem domain to a Team or WG, So that those groups can operate with clear mandates and healthy amounts of autonomy.
- In case of process failure or broken protocols among the teams, the Core Working Group is responsible for addressing the situation.
- They have the authority to institute short-term measures to address pressing problems/disputes
- They have the authority to fast-track RFCs that amend broken processes or protocols.

### Membership in the Core Working Group

The initial members of the Core Working Group are
- Juan Benet (@jbenet) - BDFL
- David Dias (@diasdavid) - Tech Lead for js-ipfs
- Jeromy Johnson (@whyrusleeping) - Tech Lead for go-ipfs
- Matt Zumwalt (@flyingzumwalt) - Program Manager for the IPFS ecosystem

Future RFCs will define how membership of the Core Working Group will change over time. Note: For most open source orgs the "core team"/"core working group"/"steering group" is usually about 8-12 people.

## Team and Working Group Lifecycle

### 1. Design

Anyone can propose creating a Team or Working Group. In order to be considered, it must satisfy a number of basic conditions:
- A _Team_ **must have at least 2 people** whose **Full Time** efforts are primarily focused on that Team's work.
- A _Working Group_ must be needed by at least 2 Teams or Working Groups.

When preparing to propose a Team or Working Group, make sure to answer these questions:
- What needs is the it addressing? Whose needs is it serving?
- What does success look like? If this Team or WG achieves its goals, what will the results be?
- Which other Teams and WGs will this group primarily interact with? Why? Have they expressed a need for it to exist?

### 2. Proposal (RFC)

The proposal must specify the following things about the Team or Working Group:
- Purpose (one line)
- Audiences for its outputs
- Mandate: What is it responsible for? What things does it have decision-making power over?
- Products and/or Services it manages
- Primary funnel for audience members to find it and engage (See **[TODO] Full list of Teams and WGs** for an explanation of these funnels and their relationship with Working Groups)
- Initial members and initial Captain

### 3. Formation

If the proposal is accepted, you are ready to officially form the Team or Working Group. You have maximum of 6 months to collect enough members. Until you have enough members, the Team/WG will be listed as "forming". During that time you can temporarily _merge_ with another Team or Working Group, participating in their OKR planning and work coordination (see [Dissolving or Merging](#dissolving-or-merging) for more about merging teams/groups).

In order to complete the formation of the Team/WG, in addition to getting members to sign on and allocate time, you must also:

1. Create a landing page for the group that lists its purpose, audiences, members, responsibilities, products and services. (This is often a landing page on a github repository dedicated to the group or its main product/service)
2. Add the group to the **[TODO]  Full list of Teams and WGs**, grouped according to primary funnel
3.  Update documentation and websites as necessary, routing audiences to the Team/WG's landing page

### 4. Functioning

Teams are responsible for:

- Defining  [Objectives and Key Results](https://weekdone.com/resources/objectives-key-results) (OKRs) every Quarter. Members of a Product Group primarily derive their tasks from those OKRs.
- Keeping their landing page up to date, with accurate listings of their Products, Services, Roadmaps, purpose, and members.

Captains are responsible for:
- Stewarding the creation of OKRs, freezing them, and getting them scored at mid-quarter and end-of-quarter.

### 5. Dissolving or Merging
If a Team's membership drops below 2 Full Time people, it will be marked "understaffed" and must either add more people, merge with another WG, or dissolve before the next round of OKR planning.

If a Team or WG merges with another Team/WG, the merged group:
- Does not have to modify its landing page (can still present itself to the world as a distinct group)
- Incorporates its OKRs into the new group, participating in that group's OKR planning
- Participates in the new group's planning and coordination activities (weekly check-ins, retrospectives, OKR scoring, etc.)
- Can un-merge in the future, without submitting a new RFC, if it accumulates enough members to stand on its own.

When a Team or WG is dissolved, the people dissolving it must:
1. Update its landing page to declare that the it has been dissolved. Reroute visitors accordingly.
2. Remove the it from the **[TODO] Full list of WGs**  
3. Remove it from documentation and websites, routing audiences elsewhere


## Failsafes

### First Failsafe: Core Working Group
In case of process failure or broken protocols among the teams, the Core Working Group is responsible for addressing the situation. Their powers and responsibilities are spelled out in the section titled [The Core Working Group](#the-core-working-group).

### "Snakes on the Plane" Failsafe: BDFL

If all other processes and protocols fail, @jbenet will step in and exercise his [beneficially dictatorial](https://en.wikipedia.org/wiki/Benevolent_dictator_for_life) prerogatives as the founder and initial creator of these projects.

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
- [x] Research other projects/orgs (5-6). Compare our process against 2-3 of them. Also research how they define the boundaries and responsibilities of Core group.
  - Done. See document: [Comparison of Open Source Governance Structures](https://docs.google.com/document/d/1vV-8mlqyXsgs_sb9PCuGtqoRlLrvSSjOvJNOZWmZjuI/edit?usp=sharing)
- [x] Need: Ways to make sure individuals don’t get spread too thin.
    - Ideas:
        - People can only captain 1 WG at a time?
        - Distinguish between product groups and WGs?
        - Work assignments should happen on Product groups
    - Addressed: Force 2-person minimum for Teams. Part-time members don't count towards that minimum. This incentivizes teams to get their members to commit, and focus.


Questions to resolve through implementation
- Need to test this process with 3-4 WGs and update the protocol as necessary
- Investigate how other teams percolate OKRs upward and create an RFCs
- Need: Support Structure for people Proposing or Captaining a WG
    - Note: In Rust, the leader of a WG must be part of the core team
- [ ]  Define: How do OKRs percolate up from sub-teams?
    - Some options:
      - The objectives percolate up, becoming KRs in their parent group's OKRs list
      - OKRs only exist at the leaves, not at intermediary levels
      - Teams write higher-level OKRs that condense and summarize their OKRs so they can be
      to percolated upwards
- Define how membership of Core WG will be updated over time
    - One leading approach is for the captains of all top-level Teams to be automatically on the Core Working Group, but this runs a risk of the group getting too big when we form more Teams and Working Groups.

Questions that are out of scope

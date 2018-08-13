- Feature Name: testing-wg
- Start Date: 2018-08-08
- Current Status: DRAFT
- Owner: Victor Bjelkholm - @VictorBjelkholm
- RFC PR: (leave this empty)
- IPFS Issue: (leave this empty)

# Summary
[summary]: #summary

<!--  One paragraph explanation of the feature. -->

Defining and starting a Working Group that focuses on:

- Realizing and implementing reusable testing and development strategies across projects
- Develop and maintain tools for testing and developer productivity
- Create and maintain a sound testing infrastructure for projects
- Define and help achieve Sustainable Open Source Modules

# Motivation
[motivation]: #motivation

<!--  Why are we doing this? What use cases does it support? What is the expected outcome? -->

Testing and developer productivity is important for the quality and stability
of everything that we build. Reusability becomes more important the more projects
and libraries we have to care about. By having a focused Working Group on these
areas, we can leverage experience and tooling built for one project for many.

# Guide-level explanation
[guide-level-explanation]: #guide-level-explanation

<!--
Explain the proposal as if it was already included in the protocol and you were teaching it to another contributor on this project. That generally means:

- Introducing new named concepts.
- Explaining the feature largely in terms of examples.
- Explaining how programmers and other contributors should *think* about the feature, and how it should impact the way they use the software or protocols being modified. It should explain the impact as concretely as possible.
- If applicable, provide sample error messages, deprecation warnings, or migration guidance.
- If applicable, describe the differences between teaching this to existing contributors and new contributors.

For implementation-oriented RFCs (e.g. for changes to a protocol or its implementations), this section should focus on how protocol contributors should think about the change, and give examples of its concrete impact. For policy RFCs, this section should provide an example-driven introduction to the policy, and explain its impact in concrete terms. 
-->

With the Working Group implemented, members of the group would convene weekly
to talk about experiences, issues found while working and about current progress
on agreed tasks.

# Reference-level explanation
[reference-level-explanation]: #reference-level-explanation

The Working Group will do the following things:

- Project / Working Group Management
- Interop Testing
  - Protocol
  - CLI
  - Repository
- Benchmarking
- Releases
- Developer Tools
- Sustainable Open Source Modules (OSS Productivity)
- Testing Theory and Strategy
  - Standarization
  - Performance
  - Libraries/Utilities
- Application Testing
- Network Testing
- Continuous Integration
  - Infrastructure
  - Pipelines
  - CI Strategy

<!--
This is the technical portion of the RFC. Explain the design in sufficient detail that:

- Its interaction with other features is clear.
- It is reasonably clear how the feature would be implemented.
- Corner cases are dissected by example.

The section should return to the examples given in the previous section, and explain more fully how the detailed proposal makes those examples work.
-->

# Drawbacks
[drawbacks]: #drawbacks

<!-- Why should we *not* do this? -->

By having just certain people be more responsible and knowledgeable about testing,
we could make people not part of the Working Group feel like they should not
care about testing and quality as much, as there is others who focus on those areas.

The Working Group could also suffer heavily from scope-creep, where unless we
define the boundary for what work should be done by the Working Group, it becomes
a catch-all group for miscellaneous tasks.

# Rationale, Prior Discussion and alternatives
[alternatives]: #alternatives

<!--
- Why is this design the best in the space of possible designs?
- What other designs have been considered and what is the rationale for not choosing them?
- What is the impact of not doing this?
- What prior discussions have occurred that led to this RFC (include links where possible)
-->

# Unresolved questions
[unresolved]: #unresolved-questions

- This Working Group should contain a mix of full-time and part-time contributors which
  collides with the proposed structure here: https://github.com/ipfs/ipfs/pull/285/files#diff-ca5fe70b286df6e5e4acb856de2d7c66R43

<!--
- What parts of the design do you expect to resolve through the RFC process before this gets merged?
- What parts of the design do you expect to resolve through the implementation of this feature before stabilization?
- What related issues do you consider out of scope for this RFC that could be addressed in the future independently of the solution that comes out of this RFC?
-->

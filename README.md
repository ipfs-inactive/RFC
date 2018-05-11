IPFS RFCs
=====

## Table of Contents
[Table of Contents]: #table-of-contents

  - [Opening](#ipfs-rfcs)
  - [Table of Contents]
  - [When you need to follow this process]
  - [Before creating an RFC]
  - [The RFC life-cycle]
  - [Reviewing RFCs]
  - [Implementing an RFC]
  - [RFC Postponement]
  - [Help this is all too informal!]
  - [License]


## When you need to follow this process
[When you need to follow this process]: #when-you-need-to-follow-this-process

You need to follow this process if you intend to make "substantial" changes to
IPFS, libp2p or the RFC process itself. What constitutes a
"substantial" change is evolving based on community norms and varies depending
on what part of the ecosystem you are proposing to change, but may include the
following.

  - Any semantic or syntactic change to the protocols that is not a bugfix.
  - Removing protocol features, including those that are feature-gated.
  - Adding anything to our list of officially supported projects, libraries, and specifications.

Some changes do not require an RFC:

  - Rephrasing, reorganizing, refactoring, or otherwise "changing shape does not change meaning".
  - Additions that strictly improve objective, numerical quality criteria
    (warning removal, speedup, better platform coverage, more parallelism, trap more errors, etc.)
  - Additions only likely to be _noticed by_ other developers-of-ipfs, but
    invisible to users-of-ipfs.

If you submit a pull request to implement a new feature without going through
the RFC process, it may be closed with a polite request to submit an RFC first.


### working group specific guidelines
[working group specific guidelines]: #working-group-specific-guidelines

As working groups take form, they will have the prerogative to add further guidelines regarding RFCs that apply to their domain of work.

## Before creating an RFC
[Before creating an RFC]: #before-creating-an-rfc

A hastily-proposed RFC can hurt its chances of acceptance. Low quality
proposals, proposals for previously-rejected features, or those that don't fit
into the near-term roadmap, may be quickly rejected, which can be demotivating
for the unprepared contributor. Laying some groundwork ahead of the RFC can
make the process smoother.

Although there is no single way to prepare for submitting an RFC, it is
generally a good idea to pursue feedback from other project developers
beforehand, to ascertain that the RFC may be desirable; having a consistent
impact on the project requires concerted effort toward consensus-building.

The most common preparations for writing and submitting an RFC include talking
the idea over on the #ipfs, #ipfs-dev and #libp2p irc channels, filing and discussing ideas on the
[RFC issue tracker], and occasionally posting "pre-RFCs" on the
[ipfs discussion forum](https://discuss.ipfs.io/t/rfcs-and-pre-rfcs) for early review.

As a rule of thumb, receiving encouraging feedback from long-standing project
developers, and particularly members of the relevant [working group] is a good
indication that the RFC is worth pursuing.

A note about key words:
In an effort to avoid ambiguity, and to make RFCs easier for non-native english speakers to interpret, use the key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and  "OPTIONAL" in your RFCs according to the guidelines in [IETF RFC 2119](https://www.ietf.org/rfc/rfc2119.txt)


## The RFC life-cycle
[The RFC life-cycle]: #the-rfc-life-cycle

In short, to get a major feature added to IPFS, one must first get the RFC
merged into the RFC repository as a markdown file. At that point the RFC is
"Accepted" and may be implemented with the goal of eventual inclusion into the corresponding protocols or libraries.

As it grows from an idea to shipping in a supported release, an RFC will traverse along:

1. **Draft**: The owner of the RFC has started to draft up how the subject will be handled and may be reviewing with the relevant working group.  Comments are certainly welcome at this stage even though the owner hasn't worked through enough details to ask for...
2. **Review**: This RFC is in a review period. Stakeholders and the owner may still be iterating on some final details before signoff.
3. **Final Call (FCP)**: 10-day Final Comment Period before an RFC is merged, closed or postponed.
4. **Accepted**: All stakeholders have signed off and this RFC is now or will be implemented soon.


### Status: Draft

When you've done the preparation described in [Before creating an RFC] and are ready to submit your RFC, create the pull request following these steps:


  - Fork the RFC repo [RFC repository]
  - Copy `0000-template-rfc.md` to `rfcs/0000-my-feature.md` (where "my-feature" is
    descriptive. don't assign an RFC number yet).
  - Fill in the RFC. Put care into the details: RFCs that do not present
    convincing motivation, demonstrate understanding of the impact of the
    design, or are disingenuous about the drawbacks or alternatives tend to be
    poorly-received.
  - Submit a pull request. As a pull request the RFC will receive design
    feedback from the larger community, and the author should be prepared to respond to feedback and possibly revise the proposal.

### Status: Review

Once a an RFC has been submitted, it's ready for Review.

  - Each pull request will be labeled with the most relevant [working group], which
    will lead to its being triaged by that team in a future meeting and assigned
    to a member of the working group.
  - At this point, the status in the RFC markdown document should be marked "Review"
  - Build consensus and integrate feedback. RFCs that have broad support are
    much more likely to make progress than those that don't receive any
    comments. Feel free to reach out to the RFC assignee in particular to get
    help identifying stakeholders and obstacles.
  - The working group will discuss the RFC pull request, as much as possible in the
    comment thread of the pull request itself. Offline discussion must be
    summarized on the pull request comment thread.
  - RFCs rarely go through this process unchanged, especially as alternatives
    and drawbacks are shown. You can make edits, big and small, to the RFC to
    clarify or change the design, but make changes as new commits to the pull
    request, and leave a comment on the pull request explaining your changes.
    Specifically, do not squash or rebase commits after they are visible on the
    pull request.

### Status: Final Call (FCP)

At some point, a member of the working group will propose a motion for _"final
comment period"_ (FCP), along with a *disposition* for the RFC (merge, close,
    or postpone).

  - This step is taken when enough of the tradeoffs have been discussed that
  the working group is in a position to make a decision. That does not require
  consensus amongst all participants in the RFC thread (which is usually
  impossible). However, the argument supporting the disposition on the RFC
  needs to have already been clearly articulated, and there should not be a
  strong consensus *against* that position outside of the working group. Working group
  members use their best judgment in taking this step, and the FCP itself
  ensures there is ample time and notification for stakeholders to push back
  if it is made prematurely.
  - For RFCs with lengthy discussion, the motion to FCP is usually preceded by
    a *summary comment* trying to lay out the current state of the discussion
    and major tradeoffs/points of disagreement.
  - Before actually entering FCP, *all* members of the working group must sign off;
  this is often the point at which many working group members first review the RFC
  in full depth.
- The FCP lasts ten calendar days, so that it is open for at least 5 business
  days. It is also advertised widely,
  e.g. in the [Weekly IPFS All Hands Call](https://github.com/ipfs/pm/#weekly-all-hands). This way all
  stakeholders have a chance to lodge any final objections before a decision
  is reached.
- In most cases, the FCP period is quiet, and the RFC is either merged or
  closed. However, sometimes substantial new arguments or ideas are raised,
  the FCP is canceled, and the RFC goes back into the "Review" stage.

### Status: Accepted    

Once an RFC becomes "Accepted" then authors may implement it and ©. Being "Accepted" is not a rubber
stamp, and in particular still does not mean the feature will ultimately be
merged; it does mean that in principle all the major stakeholders have agreed
to the feature and are amenable to merging it.

Furthermore, the fact that a given RFC has been accepted and is "Accepted"
implies nothing about what priority is assigned to its implementation, nor does
it imply anything about whether an IPFS developer has been assigned the task of
implementing the feature. While it is not *necessary* that the author of the
RFC also write the implementation, it is by far the most effective way to see
an RFC through to completion: authors should not expect that other project
developers will take on responsibility for implementing their accepted feature.

### Modifications to Accepted RFCs

Modifications to "Accepted" RFCs can be done in follow-up pull requests. We
strive to write each RFC in a manner that it will reflect the final design of
the feature; but the nature of the process means that we cannot expect every
merged RFC to actually reflect what the end result will be at the time of the
next major release.

In general, once accepted, RFCs should not be substantially changed. Only very
minor changes should be submitted as amendments. More substantial changes
should be new RFCs, with a note added to the original RFC. Exactly what counts
as a "very minor change" is up to the working group to decide.

_If_ you make changes to an RFC after it's been accepted, add a note in the header of the RFC with a very short summary of the change and links to any relevant discussions. This way the change is very explicit and hard to miss.

## Reviewing RFCs
[Reviewing RFCs]: #reviewing-rfcs

While the RFC pull request is up, the working group may schedule meetings with the
author and/or relevant stakeholders to discuss the issues in greater detail,
and in some cases the topic may be discussed at a working group meeting. In either
case a summary from the meeting must be posted back to the RFC pull request.

A working group makes final decisions about RFCs after the benefits and drawbacks
are well understood. These decisions can be made at any time, but the working group
will regularly issue decisions. When a decision is made, the RFC pull request
will either be merged or closed. In either case, if the reasoning is not clear
from the discussion in thread, the working group will add a comment describing the
rationale for the decision.


## Implementing an RFC
[Implementing an RFC]: #implementing-an-rfc

Some accepted RFCs represent vital features that need to be implemented right
away. Other accepted RFCs can represent features that can wait until some
arbitrary developer feels like doing the work. Every accepted RFC has an
associated issue tracking its implementation in the corresponding IPFS repository; thus that
associated issue can be assigned a priority via the triage process that the
teams use for all issues in the IPFS repositories.

The author of an RFC is not obligated to implement it. Of course, the RFC
author (like any other developer) is welcome to post an implementation for
review after the RFC has been accepted.

If you are interested in working on the implementation for an "Accepted" RFC, but
cannot determine if someone else is already working on it, feel free to ask
(e.g. by leaving a comment on the associated issue).


## RFC Postponement
[RFC Postponement]: #rfc-postponement

Some RFC pull requests are tagged with the "postponed" label when they are
closed (as part of the rejection process). An RFC closed with "postponed" is
marked as such because we want neither to think about evaluating the proposal
nor about implementing the described feature until some time in the future, and
we believe that we can afford to wait until then to do so. Postponed pull
requests may be re-opened when the time is right. We don't have any formal
process for that, you should ask members of the relevant working group.

Usually an RFC pull request marked as "postponed" has already passed an
informal first round of evaluation, namely the round of "do we think we would
ever possibly consider making this change, as outlined in the RFC pull request,
or some semi-obvious variation of it." (When the answer to the latter question
is "no", then the appropriate response is to close the RFC, not postpone it.)


### Help this is all too informal!
[Help this is all too informal!]: #help-this-is-all-too-informal

The process is intended to be as lightweight as reasonable for the present
circumstances. As usual, we are trying to let the process be driven by
consensus and community norms, not impose more structure than necessary.


[ipfs discussion forum]: https://discuss.ipfs.io/
[RFC issue tracker]: https://github.com/ipfs/rfcs/issues
[RFC repository]: http://github.com/ipfs/rfcs
[working group]: https://github.com/ipfs/ipfs/pull/285

## License
[License]: #license

This repository is currently in the process of being licensed under MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

_The original version of this document was cloned from the [Rust lang RFCs repository](https://github.com/rust-lang/rfcs/blob/752a02115e49c114e2d6b5247c410da69aac505c/README.md), which is dual-licensed under MIT and Apache2 licenses._

### Contributions

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in the work by you, as defined in the MIT license, shall be licensed as above, without any additional terms or conditions.

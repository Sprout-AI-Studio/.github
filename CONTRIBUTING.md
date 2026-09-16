# How we write tickets

> *"Everything should be made as simple as possible, but not simpler."* — Einstein

Tickets carry the why and the what, not the how. Product decisions get made before a
ticket reaches engineering; engineers own the technical approach.

## Who owns the ticket

The person who opens the issue owns it. Reading it end to end and editing it before
posting is required, not optional. Whoever approves a Claude-drafted ticket owns its
accuracy.

Four checks before posting, from our four tests for writing with AI:

| Test | For a ticket |
|---|---|
| **Origination** | Did your thinking come first? The ticket should start from something you noticed, not from a prompt. |
| **Length** | Did you decide how long it should be before drafting? Short and high level is the target. A ticket nobody reads is worse than no ticket. |
| **Investment** | Did you spend more time editing than the ticket takes to read? Cheap to produce is not the same as ready to send. |
| **Ownership** | Could you explain the whole ticket without opening it? If someone questions the scope in standup, you should be able to answer without scrolling. |

These four are on the author. A tool can run the self-review; it can't do these.

## The detail isn't the valuable part. Your thinking is.

Use common sense where the ticket leaves gaps, and say something when the gap is one
you can't fill, when a real product decision is missing, or when the ask doesn't fit
the week.

Neither side gets this right alone. Sometimes you'll be given too little; sometimes
you'll assume too much. The fix is a quick conversation, not a longer ticket.

## The four templates

| Template | Use it when |
|---|---|
| **Bug** | Behavior differs from what it should be. |
| **Feature / Task** | A well-defined piece of work with a clear beginning and end. |
| **Research / Investigate** | The deliverable is understanding, not code. Can be pre or post epic. |
| **Epic** | The broader outcome, wrapping a set of features and tasks. |

Epics are for product. Sub-issues are for technical.

**Before writing an epic, check the conversation has happened.** A large epic starts
as a doc everyone reads and a discussion that lands on a plan — brainstorming over
video beats writing it out. The ticket records the outcome; it isn't the place to work
it out.

A new bug gets a new ticket that references the old one rather than reopening it.
Keep statuses current: in progress → in review → done.

## Dictionary

The templates are built from these blocks. A block means the same thing everywhere it
appears.

### Who, What and Why

Three labeled lines, under 100 words total. Written from the user's seat, not the
system's.

- **WHO** — The people who will notice this. A role, a team, a type of user. Never
  "we," "the system," or "the pipeline." Test: could this person read the ticket and
  recognize their own problem?
- **WHAT** — What we're building, fixing, or figuring out. One line if it's one thing.
  For research tickets, say "decide how" or "figure out" so it's clear we're buying
  understanding, not code. Should include a high level of the deliverable, so the
  assignee has context on what they're delivering.

  When you're reporting several things you noticed on one screen, write a lead line
  plus a bullet per thing, each with three parts: what's on screen now, why it reads
  wrong to you, and what you expected instead. Say what you want in plain user
  language, even when it's a decision — "this should be one card." A decision you've
  already made belongs here. What stays out is *how* it gets built.

  Test: could a person point at the thing your bullet names? *"The chip vocabulary is
  unclear"* fails. *"I don't understand what 'One Question' means — is it necessary
  with the (?)"* passes.
- **WHY** — What the WHO gets, or stops suffering, when this is done. Write it the way
  they'd say it, not the way the code would. *"Intros that don't look silly"* beats
  *"matching uses stale profiles."*

Numbers, budgets, limits, and how the system works today do not go here. They go in
Scope or Reference Information.

### Reference Information

Links to relevant documents, screenshots, and other issues, each with one line on why
it matters. A description of how things work today belongs here, as does anything you
already checked that turned out not to be the cause.

If you have a theory about the answer, put it here in a collapsed block labeled as
your current thinking — not in the sections above.

### Acceptance Criteria

A bulleted list of what should work and what should fail. Minimum required
functionality plus common edge cases. Not an exhaustive spec.

### Scope

The size and limits of the build: time-box, cost, run time, what's explicitly out.
Any number or budget in the ticket lives here.

### Deliverables

The expected output from the assignee. For research, the note or bench or experiment
results, and the questions it must answer.

### Left Open

Decisions purposely left to the assignee, and why. Naming them here is a deliberate
handoff, not a gap. Each one names who resolves it and when. See the planning doc for
who decides what.

A decision you've already made but haven't written down is not Left Open. If you know
you want the chips gone, say so in the WHAT. Left Open is only for decisions you're
genuinely handing over.

## Technical Overview

Engineering adds a Technical Overview as a comment on the epic before work starts. It
doesn't go in the body — the body is product.

## Open questions

Open questions live only in investigation tickets. A question about *what* to build
means the ticket isn't ready — answer it, or file a Research ticket. A decision handed
to the assignee about *how* to build it is Left Open, with who resolves it and when.

## Drafting with Claude

Claude drafts; you own it. The `issue-writing` skill carries these conventions.

**Expect to be asked questions.** The skill reads the code first, then asks about
what's left over — a gap it can't fill, a product decision nobody has made, or an ask
that doesn't fit the week. Being asked isn't the tool failing. Answering three
questions before a draft is cheaper than editing a ticket built on guesses.

When it can't ask — you're not there, or it's working through a batch — it marks the
gap in the ticket with a ❓ instead of guessing quietly. Those are yours to resolve
before posting.

It won't run the four checks above. Those stay with the author.

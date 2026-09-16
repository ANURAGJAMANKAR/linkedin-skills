---
name: linkedin-content-log
description: "Maintain a running log of every LinkedIn post, comment, and reply you draft, and check it before drafting anything new so you never repeat a topic by accident. Allows a genuine update on an evolving story, blocks a stale rehash. Reads and writes references/content-log.md. Not for planning future posts (use linkedin-content-planner)."
---

# LinkedIn Content Log

The bundle's memory. It keeps a running record of what you have already said on
LinkedIn so the writing skills stop accidentally repeating a topic, an angle, or
the same numbers a month apart. It runs in two directions: a **pre-draft check**
that every writing skill calls before it drafts, and a **post-approval append**
that records what actually went out.

The log lives at `../../references/content-log.md`. It is a plain markdown file
you own, in the same family as `../../references/voice-profile.md` and
`../../references/story-bank.md`. Nothing in it is sent anywhere; it only steers
your own drafts. Skills read it when its `filled:` flag is `yes`.

## When to use

- **Automatically, before every draft.** `linkedin-post-writer`,
  `linkedin-repurposer`, and `linkedin-comment-drafter` call the pre-draft check
  as their first step. You do not have to ask for it.
- **Automatically, after every approval.** The same skills append an entry once
  you approve a post, comment, or reply.
- **On demand.** "What have I posted about X?", "have I said this before?",
  "show my last month of topics", "log this post I published manually".

## The log file

`../../references/content-log.md` holds a table, newest first. Each row:

| Field | Meaning |
|---|---|
| `date` | ISO date the post went out or was drafted (YYYY-MM-DD) |
| `type` | post / comment / reply |
| `topic` | the subject in 2-5 words (e.g. "AI agencies replacing traditional") |
| `pillar` | content pillar if known (Authority / Narrative / Community / Product, or a founder pillar) |
| `formula` | hook formula code used (F1-F20), if a post |
| `angle` | the specific take in one line (what made this post's argument) |
| `key_facts` | the concrete numbers, names, or claims used, comma separated |
| `status` | drafted / posted / scheduled, plus a URL once live |

An evergreen topic can appear many times; what must not repeat is the same
**topic + angle + key_facts** with nothing new added.

## Pre-draft check (the repeat guard)

Before any new draft, the calling skill hands this skill the proposed topic and,
if known, the angle and key facts. Steps:

1. If `../../references/content-log.md` is missing or `filled: no`, there is no
   history yet. Return `FRESH` and continue. Do not block a first-ever draft.
2. Load the log. Compare the proposed draft against entries from the **last 90
   days** (use the full log for a topic the user calls evergreen).
3. Classify and return one of:
   - **FRESH** — topic not seen, or a clearly different angle. Proceed normally.
   - **UPDATE (allowed)** — same topic, but there is genuinely new information: a
     new date, a new number, a funding round, a shipped version, a changed
     outcome, a fresh example. This is the "update in tech or business is okay"
     case. Proceed, and tell the writer to open by acknowledging it builds on the
     earlier post rather than restating it.
   - **REPEAT (warn)** — same topic AND same angle AND no new facts versus a prior
     entry. Do not silently draft. Surface the prior entry (its date and one-line
     angle) and offer three ways forward: a different angle on the same topic, a
     genuine update if the user has new information, or a deliberate re-share of
     the original. Draft only after the user picks one.
4. A REPEAT is a warning, never a hard block. The user can always say "yes, post
   it again anyway" and you proceed.

Matching is by meaning, not string equality: "AI agencies are dead" and "why
traditional agencies are being replaced by AI" are the same topic. Weigh
`topic` first, then `angle`, then overlap in `key_facts`.

## Post-approval append

After the user approves a post, comment, or reply, add one row to the top of the
table in `../../references/content-log.md` with today's date and the fields
above. Fill `key_facts` from what the draft actually used so future checks have
something concrete to compare against. If the file is `filled: no`, flip it to
`filled: yes` on the first append. Never remove or rewrite the user's existing
rows; only prepend.

## Rules

- Never invent history. If the log is empty, say so and treat every draft as FRESH.
- Never block. The guard warns and offers options; the user decides.
- A comment or reply counts too: repeating the same "sharp take" as a comment on
  five different posts in a week is the same fatigue a repeated post causes.
- Keep entries short. The log is a memory index, not a copy of every post.
- The file is the user's. Only prepend rows and flip the `filled:` flag; leave
  everything else they wrote untouched.

## How the other skills call it

- **`linkedin-post-writer`** — step 1, before picking a formula: run the pre-draft
  check on the topic. After approval: append the entry.
- **`linkedin-repurposer`** — before rebuilding source content: check that the
  same source or angle was not already repurposed recently. After approval: append.
- **`linkedin-comment-drafter`** — before drafting: check the take is not one you
  already used this week. After approval: append.

## Files

- `SKILL.md` — this file
- `../../references/content-log.md` — the running log (user-owned, `filled:` flag)

## Related skills

- `linkedin-content-planner` — plans future posts; reads this log to avoid
  scheduling a topic you just covered
- `linkedin-brand-manager` — sets the pillars each logged post should ladder up to
- `linkedin-post-writer`, `linkedin-repurposer`, `linkedin-comment-drafter` — the
  writers that call this skill before and after drafting

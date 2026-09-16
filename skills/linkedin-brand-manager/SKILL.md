---
name: linkedin-brand-manager
description: "Build and maintain your LinkedIn personal-brand strategy: niche positioning, target audience, content pillars, a cadence sized to your real weekly bandwidth, success metrics, and a 30/60/90 day roadmap. Writes references/brand-profile.md that the planner and post writer read. Not for a single week's calendar (use linkedin-content-planner) or the profile page (use linkedin-profile-optimizer)."
---

# LinkedIn Brand Manager

The strategist that sits above the tactical skills. Before you plan a week or
draft a post, this decides what you are building toward: who you want to be known
as, to whom, on what topics, at a pace you can actually sustain, measured against
targets that mean something. It interviews you once, writes a lasting
`../../references/brand-profile.md`, and then the planner and the post writer read
that profile so every draft ladders up to the strategy instead of being one-off.

Use it when someone wants to put themselves forward as a brand: an entrepreneur,
an expert, a "category of one" in a specific niche. It is honest about
bandwidth: a plan you cannot keep is worse than a smaller plan you can.

## When to use

- "Help me build my personal brand", "position myself as X", "I want to be known
  for Y", "grow my authority in Z niche"
- "What should my strategy be", "who's my audience", "what should my pillars be",
  "how often should I realistically post"
- Setting or resetting direction before using `linkedin-content-planner`
- A quarterly strategy review against the metrics you set last time

Not for: a single week's calendar (`linkedin-content-planner`), the profile page
itself (`linkedin-profile-optimizer`), or a team program
(`linkedin-employee-advocacy`).

## What it produces

A `../../references/brand-profile.md` with six parts:

1. **Positioning** — one sentence that makes you the obvious choice for one thing.
   Niche, the audience's before/after, and what makes you the category of one
   (not "AI consultant", but "the person who ships AI agents for seed-stage
   founders in a weekend"). Includes 2-3 competitors or adjacent voices and how
   you differ.
2. **Audience / ICP** — who you are writing for, their role, their stakes, the
   problems they will pay attention to, and the "audience of one" you would most
   want in the comments (the next investor, hire, or design partner).
3. **Content pillars** — 3-5 themes with a target share of your posts. Each pillar
   gets a one-line reason it earns trust with the audience above. These become the
   pillars `linkedin-content-planner` rotates through.
4. **Cadence, sized to bandwidth** — you say how many hours a week you can spend;
   this converts that into a realistic plan (posts/week + comments/day), never a
   fantasy calendar. See the bandwidth table below.
5. **Metrics and checkpoints** — the 2-4 numbers that actually track authority for
   your goal (not vanity), with 30/60/90 day targets and a review date.
6. **90-day roadmap** — the phases: what to establish first (voice, proof), what
   to build next (reach, relationships), what to convert last (inbound, offers).

## Bandwidth to cadence

Ask for real weekly hours, then propose from this table. Always round **down**;
consistency beats volume, and the 360Brew feed penalizes stop-start posting more
than a lower steady cadence.

| Hours/week | Posts/week | Comments/day | What to drop first |
|---|---|---|---|
| 1-2 | 1-2 | 5 | carousels, video; text posts only |
| 3-4 | 2-3 | 10 | net-new research; repurpose more |
| 5-7 | 3-4 | 10-15 | nothing; this is the sustainable sweet spot |
| 8+ | 4-5 | 15-20 | add formats (carousel, poll) before adding posts |

6+ posts/week triggers cannibalization signal; do not recommend it even at high
bandwidth. Growth past that comes from better posts and more comments, not more posts.

## Metrics that mean something

Pick by goal, not by what is easy to count.

| Goal | Track | Ignore |
|---|---|---|
| Authority / inbound | profile views, DMs and connection requests from ICP, saves | raw impressions |
| Audience growth | follower growth rate, comment-to-like ratio, repost rate | one-off viral spikes |
| Pipeline / offers | inbound conversations, calls booked, mentions by others | vanity likes |

Set a baseline today, a 30/60/90 target, and a review date. Revisit with the
user at each checkpoint and adjust the profile.

## Steps

1. **Check for an existing profile.** If `../../references/brand-profile.md` is
   `filled: yes`, load it and offer to review or update rather than starting over.
2. **Interview.** Ask, in order: the one thing you want to be known for; who you
   want in the comments; what you have actually done that proves it (pull from
   `../../references/story-bank.md` if `filled: yes`, and offer
   `linkedin-interviewer` if the bank is empty); 2-3 voices in your space; your
   honest weekly hours; your primary goal (authority / audience / pipeline).
3. **Draft the positioning.** One sentence, category-of-one. Test it against the
   "so what / who else could say this" filter; if a competitor could copy it word
   for word, sharpen it.
4. **Set pillars.** 3-5, with shares summing to 100% and none above 50%. Tie each
   to the audience and the goal.
5. **Size the cadence.** Convert hours to the table above; state what to drop.
6. **Choose metrics + targets.** 2-4 numbers, baseline now, 30/60/90 targets.
7. **Write the roadmap.** Three phases across 90 days.
8. **Write the profile.** Save all six parts to
   `../../references/brand-profile.md` and flip `filled: yes`. Then hand off:
   offer to run `linkedin-content-planner` for week one against the new pillars.

## Rules

- **Honesty over ambition.** Never propose a cadence the stated bandwidth cannot
  sustain. A dropped plan costs more reach than a modest one kept.
- **Category of one, not a category.** Positioning must be a claim a competitor
  cannot copy verbatim. Push until it is specific.
- **Metrics tied to the goal**, not vanity impressions. Name what to ignore.
- **Never fabricate proof.** Positioning rests on what the Story Bank or the user
  actually supplies. If there is nothing concrete, send them to
  `linkedin-interviewer` first.
- The profile is the user's file. Rewrite it only with their agreement at a review.

## Files

- `SKILL.md` — this file
- `../../references/brand-profile.md` — the strategy profile (user-owned, `filled:` flag)
- `../../references/founder-topics.md` — founder angle library, for founder positioning

## Related skills

- `linkedin-content-planner` — turns these pillars and cadence into a weekly calendar
- `linkedin-post-writer` — reads the positioning and pillars so each post is on-strategy
- `linkedin-profile-optimizer` — applies the positioning to the actual profile page
- `linkedin-interviewer` — fills the Story Bank the positioning draws its proof from

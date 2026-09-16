# Content Log

A running record of what you have already posted, commented, and replied on
LinkedIn. The `linkedin-content-log` skill reads this before any new draft to
catch accidental repeats, and appends to it after you approve something. The
Voice Profile holds *how you sound*, the Story Bank holds *what you have to say*,
and this holds *what you have already said*.

Skills only read this log when `filled: yes` below. An empty template is
ignored, so a first-ever draft is never blocked.

> **It is a file in this repository, so git can carry it.** If you cloned or
> forked this repo and you push, a filled log goes wherever you push it,
> including a public fork. Either add `references/content-log.md` to your
> `.gitignore`, or keep the filled copy outside the repo and paste it in when you
> want the guard. The bundle never ships your filled log: `content-log.md` is on
> the sync exclusion list, so it is not copied into the published Codex package.

## Status

- filled: no

## How to read a row

Newest entries go on top. Fields: `date` (YYYY-MM-DD), `type` (post / comment /
reply), `topic` (2-5 words), `pillar`, `formula` (F1-F20 for posts), `angle` (the
specific take in one line), `key_facts` (the concrete numbers, names, or claims,
comma separated), `status` (drafted / posted / scheduled, plus a URL once live).

The same topic may appear many times. What must not repeat is the same
**topic + angle + key_facts** with nothing new added. A genuine update (a new
number, date, version, or outcome) is allowed and encouraged.

## Log

| date | type | topic | pillar | formula | angle | key_facts | status |
|---|---|---|---|---|---|---|---|
| _example, delete me_ | post | AI agencies replacing traditional | Authority | F10 | contrarian: taste is the moat, not tools | 3 mo build, taste-over-tools | drafted |

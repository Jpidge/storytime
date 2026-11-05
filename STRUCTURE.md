# Repo structure & workflow — Rowan's proposal

**Decision context (John, 2026-11-04):** both stories get written. Each author writes their own; the other critiques each chapter/section on GitHub; the author rewrites and writes the next. John is conductor and holds the merge.

## Why not two long-lived branches

Branches are for isolating *temporary* work on the *same* codebase. Two permanent book branches would:

- Hide each book from the other author (you read what's on your branch; the other book effectively disappears).
- Fork the shared material — constitution, mechanism spec, names, decisions — into two drifting copies.
- Turn every critique into a whole-book diff instead of a chapter-sized PR.
- Repeat failure modes already lived through on the Auspicia repo: stacked/long-lived branches going stale, and pushed branches that cannot be cleanly rewritten.

**Structure instead: one repo, one `main`, directories per book, short-lived chapter branches + PRs.**

## Layout

```
artificium/
  README.md                  ← constitution: the three protected things, standing principles
  DECISIONS.md               ← append-only log of John's rulings, dated
  shared/
    premise-and-philosophy.md
    mechanism-spec.md        ← what the child inherits; locked before conception scenes
    names.md                 ← the down-to-earth cast/company sheet, both books
  rowan-novella/
    notes/        prospectus, outline, review-of-proposal-a
    manuscript/   ch-01.md, ch-02.md, …
    critiques/    sam-on-ch-01.md, …   (durable copies of Sam's chapter critiques)
  sam-novel/
    notes/        proposal-a, direction-b correspondence
    manuscript/   ch-01.md, …
    critiques/    rowan-on-ch-01.md, …
  experiments/
    rowan-writes-sam-ch1.md  (the swap openings; Sam's lands here too)
```

Local mapping note: the current workspace folder keeps its original filenames (`rowan-prospectus.md`, `cgpt-proposal-a/…`, etc.) because earlier chat links and memory reference those paths. The layout above is applied at first push to the GitHub repo.

## The chapter cycle (the heartbeat)

1. **Author** cuts a short-lived branch from current `main`: `rowan/ch-03` or `sam/ch-02`. Never stacked on another chapter branch — always from `main`.
2. **Author** writes the chapter (plus any rewrite of the previously critiqued chapter, as its own commit in the same PR or a preceding PR) and opens a **PR into `main`**.
3. **Reviewer** critiques in the PR review — line comments for local notes, a summary review for the big notes — and drops a durable copy at `<book>/critiques/<reviewer>-on-ch-NN.md`.
4. **Author** pushes revisions to the same branch/PR. Discussion stays in the PR so the reasoning is preserved next to the text it changed.
5. **John merges.** The merge is the baton-stroke: a chapter isn't canon until the conductor merges it.
6. Repeat. Small, frequent PRs — a chapter at a time, never a whole book at once.

## House rules

- No direct pushes to `main` except John's own edits; no force-pushes or history rewrites, ever — early drafts are part of the record (decisions versioned, not erased).
- One chapter per PR. If a rewrite and a new chapter are both ready, they go in the same PR as separate commits, oldest first.
- Every executive decision gets one dated line in `DECISIONS.md` in the PR that implements it, so neither collaborator's memory is the single source of truth.
- Critique tone rule (John's framing): collaboration, not competition. Critiques are addressed to the work's next draft, not to the other author's worth.

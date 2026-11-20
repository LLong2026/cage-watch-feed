# cage-watch-feed

Two files: `cage_watch_feed.json`, the live receipts feed for the SQUIRL OS
containment programme, read by the Containment Watch dashboard and the showcase
site, and the pre-escrow register described below.

This repository exists so the feed has a public home that carries nothing else.
It previously lived inside a repository that also held working material; that
repository is private now, so the feed was unreachable and the dashboard fell
back to a stored snapshot.

Public by design. The feed contains programme receipts and no personal data.

## The unverifiable corpus, published

`CONTAINMENT_REPORT_01_PRE_ESCROW_REGISTER_2026-11-06.json` is the register
behind the figure quoted on the showcase site: how many crossings predate
payload escrow and therefore cannot be verified from the ledger alone.

- Generated 2026-11-06T17:40Z by `conclave-live/hub_content_audit.py`, full paging.
- Escrow era begins 2026-11-03T17:47:00Z. Rows journaled before that instant had
  no bytes escrowed, and none can be reconstructed without inventing them.
- `pre_era_total`: 169 rows, listed individually so the corpus is bounded rather
  than an unquantified caveat. Per box: C1 80, C2 29, C3 60.
- Those 169 rows carry **166 distinct digests**. Two digests repeat:
  `26a96da584fd31bc` appears on C1 and C2, and `aa00000000000000` appears three
  times on C3 (the rogue-injection marker). A reader comparing a digest count to
  the row count should expect 166 against 169, and the difference is named here
  rather than left to be discovered.
- Each row carries a truncated digest, a timestamp, an epoch and a journal row
  id. No payload text, no customer data, no personal data. Scanned with the
  personal-data gate before publication: PASS, 0 blocks, 0 warnings.

The earlier figure of 78 was measured 2026-11-03 against a smaller ledger and
counted journal rows rather than the full pre-escrow set. 169 supersedes it.

Public by design, same as the feed.

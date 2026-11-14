MET

Scored on submit-OK, not on inclusion. Inclusion, reported and not scored: in 4 of 4 minutes our payments included (desk counter) were within 10 percent of submit-OK.

# HOLD-1, desk, pre-run 34

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

HOLD-1 offers 1013 simple payments a second at 150 sompi/gram (one third of 3,040 payments a second) on the kept public TN10 nodes. The covenant families, the KCC-20 mint line and the tic-tac-toe guest keep running on the desk node. No heavy lane. The desk node is not restarted.

Payment offer 1,013 tx/s at 150 sompi/gram, from 9 payment senders, 3 per kept public node (3 unique kaspads), each its own process and connection. Families offer 1.2 hop/s, 13 families live, one family-sender process and one builder: floor (families 1–12) 200 sompi/gram on the desk's private node, kcc (families 13–13) 100 sompi/gram on the desk's private node (public map ).

Payment pile: 5,408 coins on the payment key at the preflight, dealt evenly over the 9 senders before the first payment. A deal never holds more coins than the preflight pile. A coin is re-used about once a second, so one sender's ceiling is about its pool per second.

## Submit-OK and included, per minute

| Minute (UTC) | Pay submit-OK | Our payments included | Included, all non-coinbase | Counter |
|---|---:|---:|---:|---|
| 2026-11-14T13:50 | 60,565 | 61,106 | 64,930 | kept pace |
| 2026-11-14T13:51 | 60,623 | 60,252 | 63,991 | kept pace |
| 2026-11-14T13:52 | 60,416 | 60,954 | 64,659 | kept pace |
| 2026-11-14T13:53 | 61,330 | 60,788 | 64,506 | kept pace |

Submit-OK counts in the minute a submit was answered. Included counts in the minute of the chain block that accepted it, so a payment submitted late in one minute can be included in the next. "Kept pace" means the desk node's DAA stayed within 100 of the kept public kaspad and its sink was under 30 s old in every sample of that minute; "LAGGING" means it did not, and the count is what the node had accepted, not a network figure.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (200) | Kcc hops (100) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-14T13:50 | 64,930 | 61,106 | 775 | 3 | 3,085 | 280 | 0 | 634 | 20 | kept pace |
| 2026-11-14T13:51 | 63,991 | 60,252 | 778 | 4 | 3,007 | 295 | 0 | 478 | 20 | kept pace |
| 2026-11-14T13:52 | 64,659 | 60,954 | 709 | 3 | 3,043 | 275 | 0 | 749 | 20 | kept pace |
| 2026-11-14T13:53 | 64,506 | 60,788 | 738 | 4 | 3,027 | 288 | 0 | 687 | 20 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–12, desk private node): 200 sompi/gram per hop. Kcc (families 13–13, desk private node): no rows sompi/gram per hop. In pre-run 34 that rate is on the hop's node-side mass (kit21): the builder is asked for a bill rate on its own mass so that fee / node mass is the tier's rate.

| Tier | Node rate as built, median (min–max) | Bill rate, median | Node mass, median (min–max) | Node rate in the desk mempool, lowest–highest (probe) |
|---|---|---:|---|---|
| floor (200) | 200.14 (200–200.32) | 629 | 41,001 (40,390–43,869) | 200–200.32 |
| kcc (100) | - | - | - | 100.13–100.25 |

Node rate as built is kit21's fee / node mass (rusty-kaspa v2.1.0 storage mass with UTXO plurality, or compute or transient/2 if larger). In the desk mempool the probe divides the node's fee by the larger of the storage and compute mass the node reports.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 4 (1,160), 8 (209), 10 (207), 6 (199), 7 (192), 9 (183), 5 (171), 11 (164), 12 (113), 15 (102), 14 (99), 13 (93), and 51 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | Kcc OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---:|---:|---|
| 2026-11-14T13:50 | 60,565 | 60,566 | 0 | 0 | 1 | 774 / 1118 / 0 / 0 / 9 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-14T13:51 | 60,623 | 60,625 | 0 | 0 | 2 | 781 / 1107 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-14T13:52 | 60,416 | 60,416 | 0 | 0 | 0 | 709 / 1105 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-14T13:53 | 61,330 | 61,333 | 0 | 0 | 3 | 732 / 1108 / 0 / 0 / 6 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | yes |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 34 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 54,702 to 66,858 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 3, 7. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 7 candidate endpoints passed the check and were 3 kaspads (node 2 is node 1, node 4 is node 1, node 5 is node 1, node 6 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 623281629 | 81,281 | 3 | 0 | 32 |
| 3 | yes | 623281629 | 81,061 | 2 | 0 | 37 |
| 7 | yes | 623281629 | 80,592 | 1 | 0 | 68 |

## Payment senders

| Sender | Node | Pay submit-OK | Rejects | Minutes with a row |
|---|---:|---:|---:|---:|
| 1.1 | 1 | 27,087 | 1 | 4 of 4 |
| 1.2 | 1 | 27,099 | 1 | 4 of 4 |
| 1.3 | 1 | 27,095 | 1 | 4 of 4 |
| 3.1 | 3 | 27,101 | 1 | 4 of 4 |
| 3.2 | 3 | 27,098 | 1 | 4 of 4 |
| 3.3 | 3 | 26,862 | 0 | 4 of 4 |
| 7.1 | 7 | 26,868 | 0 | 4 of 4 |
| 7.2 | 7 | 26,863 | 0 | 4 of 4 |
| 7.3 | 7 | 26,861 | 1 | 4 of 4 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 2996 of 2996 | 760 | 1515 |
| kcc | 0 of 0 | - | - |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Our heavy in mempool / ready | Floor in mempool / ready | Kcc in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: our heavy | Template: floor | Template: kcc | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 3 mempool | Public 7 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|
| 2026-11-14T13:50 | 3 | 391 | 391 | 2.38 | 4 | 4 | - | - | 378 | 0 / 0 | 10 / 10 | 0 / 0 | 122 | 245,404 | 0 | 115 | 0 | 6 | 0 | 1 | 207.4 / 152.8 / 111.2 | 589 | 539 | 619 |
| 2026-11-14T13:51 | 3 | 239 | 391 | 2.39 | 6 | 6 | - | - | 372 | 0 / 0 | 12 / 12 | 0 / 0 | 139 | 285,220 | 0 | 132 | 0 | 7 | 0 | 1 | 197.2 / 149.7 / 110.8 | 827 | 714 | 714 |
| 2026-11-14T13:52 | 3 | 394 | 716 | 3.19 | 35 | 35 | - | - | 706 | 0 / 0 | 9 / 9 | 0 / 0 | 259 | 82,052 | 0 | 257 | 0 | 2 | 0 | 9 | 259.0 / 165.3 / 112.7 | 944 | 1,050 | 1,054 |
| 2026-11-14T13:53 | 3 | 319 | 319 | 2.06 | 7 | 7 | - | - | 306 | 0 / 0 | 9 / 9 | 0 / 0 | 130 | 284,314 | 0 | 121 | 0 | 7 | 0 | 1 | 178.3 / 142.9 / 109.8 | 852 | 735 | 655 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Pre-run 17: ready count and ready mass come from the full mempool read up to 10,000 entries and from the node's own figures (getFeeEstimateExperimental, verbose) above that, where the per-class columns stay blank (the node's wRPC replies are capped at 128 MiB, about 12,500 entries). Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs (our heavy lane is its own class, our heavy); its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.

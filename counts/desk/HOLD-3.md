NOT MET

Scored on submit-OK, not on inclusion. Inclusion, reported and not scored: in 10 of 12 minutes our payments included (desk counter) were within 10 percent of submit-OK.

# HOLD-3, desk, pre-run 34

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

HOLD-3 offers 3040 simple payments a second at 150 sompi/gram (three thirds of 3,040 payments a second) on the kept public TN10 nodes. The covenant families, the KCC-20 mint line and the tic-tac-toe guest keep running on the desk node. No heavy lane. The desk node is not restarted.

Payment offer 3,040 tx/s at 150 sompi/gram, from 9 payment senders, 3 per kept public node (3 unique kaspads), each its own process and connection. Families offer 1.2 hop/s, 13 families live, one family-sender process and one builder: floor (families 1–12) 200 sompi/gram on the desk's private node, kcc (families 13–13) 100 sompi/gram on the desk's private node (public map ).

Payment pile: 5,408 coins on the payment key at the preflight, dealt evenly over the 9 senders before the first payment (last deal, repair: 125 coins in all, 14 / 14 / 14 / 14 / 14 / 14 / 14 / 14 / 13, even, from the handoff pools). A deal never holds more coins than the preflight pile. A coin is re-used about once a second, so one sender's ceiling is about its pool per second.

## Submit-OK and included, per minute

| Minute (UTC) | Pay submit-OK | Our payments included | Included, all non-coinbase | Counter |
|---|---:|---:|---:|---|
| 2026-11-14T14:00 | 31,099 | 89,161 | 92,914 | kept pace |
| 2026-11-14T14:01 | 7,666 | 9,434 | 13,311 | kept pace |
| 2026-11-14T14:02 | 7,552 | 7,582 | 11,534 | kept pace |
| 2026-11-14T14:03 | 7,566 | 7,621 | 11,589 | kept pace |
| 2026-11-14T14:04 | 7,543 | 7,635 | 11,665 | kept pace |
| 2026-11-14T14:05 | 7,518 | 7,461 | 11,444 | kept pace |
| 2026-11-14T14:07 | 7,318 | 7,389 | 11,412 | kept pace |
| 2026-11-14T14:08 | 7,245 | 7,216 | 11,348 | kept pace |
| 2026-11-14T14:09 | 7,112 | 7,088 | 11,086 | kept pace |
| 2026-11-14T14:10 | 7,034 | 7,022 | 11,063 | kept pace |
| 2026-11-14T14:11 | 7,021 | 7,086 | 11,127 | kept pace |
| 2026-11-14T14:12 | 7,101 | 7,061 | 11,189 | kept pace |

Submit-OK counts in the minute a submit was answered. Included counts in the minute of the chain block that accepted it, so a payment submitted late in one minute can be included in the next. "Kept pace" means the desk node's DAA stayed within 100 of the kept public kaspad and its sink was under 30 s old in every sample of that minute; "LAGGING" means it did not, and the count is what the node had accepted, not a network figure.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (200) | Kcc hops (100) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-14T14:00 | 92,914 | 89,161 | 505 | 3 | 3,261 | 238 | 0 | 932 | 20 | kept pace |
| 2026-11-14T14:01 | 13,311 | 9,434 | 880 | 4 | 3,077 | 291 | 0 | 429 | 20 | kept pace |
| 2026-11-14T14:02 | 11,534 | 7,582 | 871 | 4 | 3,119 | 324 | 1 | 417 | 20 | kept pace |
| 2026-11-14T14:03 | 11,589 | 7,621 | 875 | 4 | 3,144 | 317 | 0 | 505 | 20 | kept pace |
| 2026-11-14T14:04 | 11,665 | 7,635 | 954 | 3 | 3,116 | 364 | 0 | 511 | 20 | kept pace |
| 2026-11-14T14:05 | 11,444 | 7,461 | 918 | 4 | 3,102 | 376 | 1 | 1067 | 20 | kept pace |
| 2026-11-14T14:07 | 11,412 | 7,389 | 912 | 3 | 3,165 | 390 | 0 | 660 | 20 | kept pace |
| 2026-11-14T14:08 | 11,348 | 7,216 | 972 | 4 | 3,191 | 439 | 0 | 434 | 20 | kept pace |
| 2026-11-14T14:09 | 11,086 | 7,088 | 974 | 4 | 3,062 | 427 | 1 | 316 | 20 | kept pace |
| 2026-11-14T14:10 | 11,063 | 7,022 | 976 | 2 | 3,126 | 401 | 0 | 587 | 20 | kept pace |
| 2026-11-14T14:11 | 11,127 | 7,086 | 936 | 0 | 3,155 | 362 | 0 | 388 | 19 | kept pace |
| 2026-11-14T14:12 | 11,189 | 7,061 | 1019 | 0 | 3,165 | 424 | 1 | 441 | 20 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–12, desk private node): 200 sompi/gram per hop. Kcc (families 13–13, desk private node): no rows sompi/gram per hop. In pre-run 34 that rate is on the hop's node-side mass (kit21): the builder is asked for a bill rate on its own mass so that fee / node mass is the tier's rate.

| Tier | Node rate as built, median (min–max) | Bill rate, median | Node mass, median (min–max) | Node rate in the desk mempool, lowest–highest (probe) |
|---|---|---:|---|---|
| floor (200) | 200.18 (200–200.32) | 623 | 40,606 (40,390–43,872) | 200–200.32 |
| kcc (100) | - | - | - | 100–100.11 |

Node rate as built is kit21's fee / node mass (rusty-kaspa v2.1.0 storage mass with UTXO plurality, or compute or transient/2 if larger). In the desk mempool the probe divides the node's fee by the larger of the storage and compute mass the node reports.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 4 (98), 5 (70), 6 (66), 7 (52), 8 (44), 11 (17), 9 (16), 10 (11), 12 (9), 3 (7), 13 (5), 14 (3), and 42 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | Kcc OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---:|---:|---|
| 2026-11-14T14:00 | 31,099 | 33,636 | 0 | 0 | 2537 | 505 / 1031 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:01 | 7,666 | 7,666 | 0 | 0 | 0 | 880 / 1087 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:02 | 7,552 | 7,552 | 0 | 0 | 0 | 870 / 1104 / 0 / 0 / 11 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:03 | 7,566 | 7,566 | 0 | 0 | 0 | 876 / 1132 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:04 | 7,543 | 7,545 | 0 | 0 | 2 | 943 / 1152 / 0 / 0 / 1 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:05 | 7,518 | 7,519 | 0 | 0 | 1 | 929 / 1111 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:07 | 7,318 | 7,319 | 0 | 0 | 1 | 912 / 1113 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:08 | 7,245 | 7,247 | 0 | 0 | 2 | 970 / 1138 / 0 / 0 / 10 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:09 | 7,112 | 7,114 | 0 | 0 | 2 | 975 / 1171 / 0 / 0 / 11 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:10 | 7,034 | 7,034 | 0 | 0 | 0 | 977 / 1150 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:11 | 7,021 | 7,021 | 0 | 0 | 0 | 936 / 1138 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T14:12 | 7,101 | 7,101 | 0 | 0 | 0 | 1019 / 1169 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 34 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 164,160 to 200,640 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 3, 7. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 7 candidate endpoints passed the check and were 3 kaspads (node 2 is node 1, node 4 is node 1, node 5 is node 1, node 6 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 623292546 | 37,299 | 1385 | 0 | 31 |
| 3 | yes | 623292546 | 23,565 | 4 | 0 | 37 |
| 7 | yes | 623292547 | 50,911 | 1156 | 0 | 67 |

## Payment senders

| Sender | Node | Pay submit-OK | Rejects | Minutes with a row |
|---|---:|---:|---:|---:|
| 1.1 | 1 | 15,278 | 575 | 12 of 12 |
| 1.2 | 1 | 11,365 | 324 | 12 of 12 |
| 1.3 | 1 | 10,656 | 486 | 12 of 12 |
| 3.1 | 3 | 7,414 | 1 | 12 of 12 |
| 3.2 | 3 | 8,977 | 1 | 12 of 12 |
| 3.3 | 3 | 7,174 | 2 | 12 of 12 |
| 7.1 | 7 | 20,768 | 581 | 12 of 12 |
| 7.2 | 7 | 19,819 | 575 | 12 of 12 |
| 7.3 | 7 | 10,324 | 0 | 12 of 12 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 11558 of 11558 | 593 | 1207 |
| kcc | 0 of 0 | - | - |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Our heavy in mempool / ready | Floor in mempool / ready | Kcc in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: our heavy | Template: floor | Template: kcc | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 3 mempool | Public 7 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|
| 2026-11-14T14:00 | 3 (entries skipped: over the read cap) | 19,430 | 2,164 | 15.43 | 4 | 4 | - | - | 2,040 | 0 / 0 | 11 / 11 | 0 / 0 | 258 | 82,203 | 0 | 0 | 0 | 0 | 0 | 0 | 294.5 / 171.3 / 113.3 | 19,039 | 19,038 | 19,046 |
| 2026-11-14T14:01 | 3 | 40 | 38 | 1.24 | 3 | 3 | - | - | 35 | 0 / 0 | 11 / 11 | 0 / 0 | 37 | 450,103 | 0 | 30 | 0 | 11 | 0 | 2 | 100.0 / 100.0 / 100.0 | 59 | 116 | 115 |
| 2026-11-14T14:02 | 3 | 16 | 17 | 0.90 | 1 | 1 | - | - | 14 | 0 / 0 | 10 / 10 | 0 / 0 | 17 | 369,186 | 0 | 14 | 0 | 9 | 0 | 1 | 100.0 / 100.0 / 100.0 | 34 | 40 | 70 |
| 2026-11-14T14:03 | 3 | 46 | 46 | 1.10 | 0 | 0 | - | - | 33 | 0 / 0 | 12 / 12 | 0 / 0 | 39 | 450,945 | 0 | 27 | 0 | 11 | 0 | 0 | 103.8 / 102.8 / 100.9 | 126 | 110 | 117 |
| 2026-11-14T14:04 | 3 | 12 | 12 | 0.52 | 0 | 0 | - | - | 0 | 0 / 0 | 3 / 3 | 0 / 0 | 12 | 204,587 | 0 | 0 | 0 | 3 | 0 | 0 | 100.0 / 100.0 / 100.0 | 18 | 25 | 108 |
| 2026-11-14T14:05 | 3 | 11 | 11 | 0.90 | 0 | 0 | - | - | 2 | 0 / 0 | 11 / 11 | 0 / 0 | 11 | 405,274 | 0 | 2 | 0 | 10 | 0 | 0 | 100.0 / 100.0 / 100.0 | 59 | 57 | 58 |
| 2026-11-14T14:07 | 3 | 34 | 34 | 1.05 | 0 | 0 | - | - | 22 | 0 / 0 | 12 / 12 | 0 / 0 | 33 | 449,230 | 0 | 22 | 0 | 11 | 0 | 0 | 111.4 / 108.1 / 102.5 | 41 | 41 | 42 |
| 2026-11-14T14:08 | 2 | 23 | 121 | 1.33 | 7 | 7 | - | - | 120 | 0 / 0 | 12 / 12 | 0 / 0 | 67 | 406,167 | 0 | 57 | 0 | 10 | 0 | 7 | 157.7 / 134.3 / 108.4 | 80 | 80 | 81 |
| 2026-11-14T14:09 | 3 | 10 | 42 | 0.99 | 2 | 2 | - | - | 27 | 0 / 0 | 10 / 10 | 0 / 0 | 37 | 451,652 | 0 | 26 | 0 | 10 | 0 | 2 | 116.1 / 111.3 / 103.4 | 67 | 50 | 51 |
| 2026-11-14T14:10 | 3 | 12 | 12 | 0.98 | 0 | 0 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 12 | 490,330 | 0 | 0 | 0 | 12 | 0 | 0 | 100.0 / 100.0 / 100.0 | 39 | 52 | 52 |
| 2026-11-14T14:11 | 3 | 26 | 32 | 1.05 | 0 | 0 | - | - | 14 | 0 / 0 | 12 / 12 | 0 / 0 | 31 | 453,252 | 0 | 14 | 0 | 11 | 0 | 0 | 114.5 / 110.3 / 103.1 | 24 | 15 | 15 |
| 2026-11-14T14:12 | 3 | 10 | 10 | 0.81 | 0 | 0 | - | - | 0 | 0 / 0 | 10 / 10 | 0 / 0 | 10 | 405,319 | 0 | 0 | 0 | 10 | 0 | 0 | 100.0 / 100.0 / 100.0 | 26 | 26 | 40 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Pre-run 17: ready count and ready mass come from the full mempool read up to 10,000 entries and from the node's own figures (getFeeEstimateExperimental, verbose) above that, where the per-class columns stay blank (the node's wRPC replies are capped at 128 MiB, about 12,500 entries). Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs (our heavy lane is its own class, our heavy); its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.

> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine. Pre-run 34. Not Wednesday. Not Tuesday. Not pre-runs 1 to 33.

# Targets

**Question.** Pre-run 33 ran this same ladder with floor hops at 100 sompi per gram and payments at 150. On our desk, payment submit-OK stayed near the offer through 3,040 a second, and same-minute inclusion of our payments matched it through 2,027. Floor hops left their quiet pace (953 and 970 a minute) in the first 1,013 minute (736, then about 600) and were about 100–160 a minute at 2,027 and about 60–100 at 3,040. The selector weight we are using is (fee / mass) cubed. 100 against 150 is a weight of about 0.30. 200 against 150 is a weight of about 2.37. This run asks whether that flip keeps the hop line nearer its quiet pace while the payment ladder is the same.

**Target.** Between `PRE-RUN-OPEN` and the end of RETURN, at least one covenant hop, one KCC-20 mint and one tic-tac-toe carrier are accepted on our desk node. Each scored payment step is three clean minutes of submit-OK within 10 percent, or `NOT MET` after one repair. The 4,053 minute is an observation. The run names the first component that falls behind. Retry count 0.

## The one knob, written before the arm

**The floor-family fee.** Families 1–12 pay 200 sompi per gram of node mass. They paid 100 in pre-run 33. The payment offer is unchanged: 1,013, then 2,027, then 3,040, then one minute at 4,053, then 1,013 again, at 150 sompi per gram, to the kept public TN10 nodes. The families, the mint line and the guest stay on the desk node.

What stays put, so it is not a second knob:

- Twelve covenant families, 1.2 hops a second, one sender, one builder.
- The KCC-20 family stays at 100. It is not part of the knob.
- The KCC-20 mint line, one mint at a time, 15 s after each accept. The cap we intend is 120. In pre-run 33 the parent set 120 and the mint process ran at its default of 30, because that setting never arrived. This run passes the cap into the child. That is a fix of our tool, recorded here, not a second network knob.
- One tic-tac-toe match, one carrier at a time. Pre-run 33 started six matches; only the first logged a finished game inside our 8-minute wait. This run plans one match, so a later hang is not part of the question. A carrier counts only when its id is among the desk node's accepted ids.
- No heavy lane. The desk node is not restarted. We do not stop it for this send.

Two recorded facts that are not a second knob:

- The Mini is not reachable from this desk. This run has one counter, the desk node. [logs/MINI-NOT-REACHABLE.md](../logs/MINI-NOT-REACHABLE.md) is on origin before the arm. We do not write a Mini-armed file.
- Keys 1 and 2 are not used. One distinct key per family. The payment pile is a different key. Our payment sender stops every sender when usable funds on the funding key fall under 18,000 tKAS. A coin-count line under 2,500 is logged and does not stop the senders. In pre-run 33 the coin-count line stopped RETURN for six minutes while usable funds were still about 49,772 tKAS. That stop is the tool we changed. It is not a network result.

## What we are checking in our own earlier pages

- Pre-run 33's combined target was met: 13,620 hops, 30 of 30 mints, 8 of 8 carriers. The capacity reading is the timeline, not the met flag. Submit-OK and same-minute inclusion diverged at 3,040. By the end of the tail, 3,272,071 of 3,272,071 payment submits were included.
- The chain-block column in the quiet minutes was about 350–420. We do not read that as ten blue blocks a second, and we do not treat pre-run 33 as a correction of finding 1.
- The local lane label in pre-run 33's timeline still says N0-drain on some rows. That was the runner's text. We left it.

## Order

1. Disk floor written. Desk free space at 2026-11-14T13:36:51Z: 337.4 GB. Abort under 150 GB. The desk node is not restarted.
2. Free check, read-only, committed before any submit. Names that do not answer are logged and dropped. A raw address found by a scan is not a send target.
3. Funding-key split, logged, before the hashes, if the count of coins over 3 tKAS is thin. Family top-up only if a key has no coin of at least 15 tKAS. The new coins are left until their block DAA is behind the tip. The payment pile is reused if it still has at least 4,500 coins over 10 tKAS.
4. Hashes first. Thirteen rows in [hashes/SIXTEEN.md](../hashes/README.md) (the file keeps that name). The offline check builds them and does not submit.
5. `PRE-RUN-OPEN`, then genesis of the thirteen covenants, then the lines, then the ladder.

| Order | File | Payments | What else runs |
|---:|---|---|---|
| 1 | BASE | none | families, mint line, one guest match. 2 whole minutes. Not scored |
| 2 | HOLD-1 | 1,013 tx/s | the three lines stay up |
| 3 | HOLD-2 | 2,027 tx/s | the same |
| 4 | HOLD-3 | 3,040 tx/s | the same |
| 5 | HOLD-4 | 4,053 tx/s | one pinned minute. Not scored |
| 6 | RETURN | 1,013 tx/s | the same, to see whether the lines come back |
| 7 | tail | stopped | the counter reads on for 5 minutes |

The knob is the floor fee. It does not change during the run. One repair per scored step, the same handoff the earlier payment runs used, and then the step stands.

## Cohorts

| Cohort | Families | Rate, sompi/gram of node mass | Where |
|---|---|---:|---|
| floor | 1–12 | 200 | desk node |
| kcc | 13 | 100 | desk node, the mint line |
| payments | — | 150 sompi/gram, on the payment's own mass | kept public TN10 nodes |

Finding 1 is still the capacity line we are using for the offer sizes: about 304–308 simple payments in a full block, about 3,040–3,080 a second at 10 blocks a second. 1,013, 2,027, 3,040 and 4,053 are one third, two thirds, three thirds and four thirds of the low edge. We may be dividing it wrong. The count files will say what the node did.

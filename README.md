> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **This is a pre-run. Pre-run 34.** It is not the Wednesday run. It is not the Tuesday run. It is not pre-run 1 to 33, and it does not edit their repos. A read does not start a runner.

# tn10-storm-2026-11-11-prerun-34

**Pre-run 34: the same payment ladder as pre-run 33, with the floor-family fee raised from 100 to 200 sompi per gram.** The neuron stays [tn10-storm-2026-11-11](https://github.com/STP-KAS/tn10-storm-2026-11-11). This repo does not edit that repo.

> **Our own testing.** This is our own Kaspa Testnet-10 testing, run on our own machines and nodes. What these pages report is what we observed in this run; it is not a claim of how TN10 or Kaspa behave in general.

| Field | Value |
|---|---|
| Target | The three lines stay up while simple payments are offered at 1,013, then 2,027, then 3,040, then one minute at 4,053, then 1,013 again. At least one hop, one mint and one guest carrier land in the open window. The run names the first line that falls behind |
| The change | One knob: floor families 1–12 pay 200 sompi per gram of node mass. In pre-run 33 they paid 100, and the payments paid 150. Payments stay at 150. Families stay at 12. No heavy lane |
| Met or not met | **not met**. HOLD-1 and HOLD-2 met on payment submit-OK. HOLD-3 did not. HOLD-4 is an observation. RETURN had started and was not scored. The runner stopped at 14:19:36Z on the family-key abort (usable tKAS under 18,000). Guest carriers 8 of 8. Mint line 90 accepts, 0 rejects, stopped on its try cap |
| Retry count | 0. The next attempt is a new repo. This one is not resumed |
| Core tags | 1. A lingering-id sample was not closed; the rot log is empty, so no count is given |
| Status | failed. Closed from the published step files and the counter's last snapshot |

Plan, lock, and the prediction are in [plan/PLAN.md](plan/PLAN.md), [locks/LOCKED.md](locks/LOCKED.md), and [plan/PREDICTIONS.md](plan/PREDICTIONS.md). Written before any submit.

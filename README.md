# Kabocha tasks

The jobs Kabocha needs done, and how to pick one up. Shown live at
[birdbrain.wtf/networks/kabocha/tasks](https://birdbrain.wtf/networks/kabocha/tasks).

Kabocha is parachain 2113 on Kusama. Kusama's validators secure it, so it needs no validators of
its own. What it lacks is independent infrastructure. Today Birdbrain runs its only collator and
both of Birdbrain's servers sit with one hosting company. A healthy parachain has at least three
collators run by different people on different machines, two independent public RPC endpoints
and an archive node. Each of those is a job on this board.

## How it works

1. **Every job has a test.** A card says what the job is, what machine it needs and how we
   measure it from outside. "Help with infrastructure" is not a job. "Keep a public RPC
   answering, checked by outside probes every ten minutes" is.
2. **You offer a plan, not a price.** [Open an offer](../../issues/new?template=offer.yml) on the
   job you want. Tell us the machine, the hosting company and country, how you keep keys, how you
   would notice an outage and what you have run before. Offers on hosting companies Kabocha does
   not already use go first, because the point is independence.
3. **Trust is built in public, one rung at a time.** Nobody skips a rung, including people we
   already know. The record from each rung is attached to the next ask.

| Rung | Job | Needs a key? | Needs a vote? | Record we keep |
| --- | --- | --- | --- | --- |
| 1 | [Run a plain node](jobs/node.md) for 14 days | No | No | Seen synced from our side |
| 2 | [Run a public RPC endpoint](jobs/rpc.md) | No | No | Uptime from outside probes |
| 3 | [Hold a collator seat](jobs/collator.md) | A session key, made on your server | Yes, a holders' referendum | Blocks authored each session, read on chain |
| - | [Run an archive node](jobs/archive.md) (after rung 1) | No | No | Random historical queries answered |

A collator cannot move anyone's funds. The worst a bad one can do is miss or censor its own
slots, and removing it takes another referendum. That is why the plain node comes first: two weeks
of a node that stays up and stays synced costs you little, risks nothing and tells holders
something real when the seat goes to a vote.

## Pay

Nothing on this board is paid yet. Kabocha's holders have not voted an operator budget.

What is being proposed: each job paid per measured job, monthly in arrears, budgeted in pounds and
settled in KAB, inside a monthly cap that holders vote. Collators first. RPC endpoints and the
archive node join the budget after a quarter of clean collator payouts. Hardware is paid per job
and labour per operator. The working figures are on each card and are assumptions until operators
tell us what the work really costs. If you run one of these jobs, that is the most useful thing
you can tell us.

Running a node before a budget passes builds the record a paid seat would need. It does not
create a claim to back pay.

## Files

| File | What |
| --- | --- |
| `board.json` | The board as data: jobs, rungs, status and who is on which rung. The page and the app read it |
| `jobs/*.md` | One page per job: what it is, the machine, the test, the steps |
| `.github/ISSUE_TEMPLATE/offer.yml` | The offer form |

The board changes by pull request or by Birdbrain after an offer is accepted, so its history is
this repository's history.

## Talk to us

The Kabocha Matrix room, `#kabocha.watercooler:matrix.org` (bridged to Telegram), or an issue here.
The node kit: [kabocha-rpc.birdbrain.wtf/node/SETUP.md](https://kabocha-rpc.birdbrain.wtf/node/SETUP.md).

# Rung 3: hold a collator seat

**Open to anyone with a rung 1 record. The seat itself needs a holders' vote.**

Collators make Kabocha's blocks and hand them to Kusama's validators. Birdbrain runs the only one
today. Kabocha needs at least three, run by different people on different machines.

## The machine

The plain node from rung 1, on its own machine. Never run two collators on one machine, and never
run one session key on two machines at once.

## Steps

1. Finish rung 1.
2. Steps 5 and 6 of [SETUP.md](https://kabocha-rpc.birdbrain.wtf/node/SETUP.md): make the session
   key on the server, then sign `session.setKeys` from your own wallet. The wallet's secret phrase
   never goes on the server and never goes to an agent.
3. Tell us your account address on your offer. We put it to Kabocha's holders in a referendum, with
   your rung 1 record attached.
4. Once it passes and a new session starts, your node signs its share of blocks with no change on
   the server.

Open candidate registration is switched off on Kabocha, so seats are added by referendum only.
The next runtime upgrade (spec 28 to 100) goes to holders from about late November and also sets
the collator seats. How a new seat is added after it will be written here before that vote.

## How we check it

Blocks authored by your account in each session, read on chain, against the slots it was due.
The board shows the last 30 days.

## Pay (proposed, not voted)

| | Per month | Basis |
| --- | --- | --- |
| Hardware | £7 to £36 | Fact for the range ends: a Hetzner CPX32 is €41.99, an OVH VPS-2 is £7.40 |
| Labour, per operator | £100 to £250 | Assumption. Collators are not slashed and need no overnight on-call. To be confirmed by operators |

Collators are the first job in the operator budget once holders vote one. Birdbrain's own collator
is either not paid from that budget or its payment is declared.

## What a collator cannot do

Move anyone's funds. The worst a collator can do is miss or censor its own slots. Removing one
takes another referendum.

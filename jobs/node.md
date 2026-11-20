# Rung 1: run a plain node for 14 days

**Open now.** No key, no vote, nothing at risk.

A plain Kabocha node follows the chain and talks to other nodes. It cannot make blocks. Running one
for two weeks shows that your machine stays up and keeps up, which is what holders want to know
before a collator seat goes to a vote.

## The machine

- x86_64 Linux, Debian 12 tested
- 4 vCPU, 8 GB RAM, 100 GB SSD (about 20 GB used today)
- A public IPv4 address with inbound TCP 30333 and 30334 open
- Its own machine, on a hosting company Kabocha does not already use if you can

## Steps

Steps 1 to 4 of the node kit: [kabocha-rpc.birdbrain.wtf/node/SETUP.md](https://kabocha-rpc.birdbrain.wtf/node/SETUP.md).
Stop after step 4. Do not make a session key yet.

Then [open an offer](../../../issues/new?template=offer.yml) with:

- the node's peer ID, from its log: `Local node identity is: 12D3KooW...`
- its public address and p2p port, so we can check it from outside
- the `NODE_NAME` you chose

## How we check it

Every ten minutes Birdbrain's box checks that your node's p2p port answers. The record shows on
the board as the share of checks answered since you started. Checking that the node is also synced
to the head, by finding your peer ID among our nodes' peers, is being set up. Until then, post the
two `Idle` lines from your log in your offer once a week.

Fourteen days with nineteen checks in twenty answered moves you to rung 2 or straight to a
collator ask.

## Pay

None. This rung is how a record starts.

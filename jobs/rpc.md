# Rung 2: run a public RPC endpoint

**Open to anyone who has finished rung 1.**

Wallets, explorers and the holders' page need somewhere to read Kabocha from. Today they read mostly
from Birdbrain's endpoint (`wss://kabocha-rpc.birdbrain.wtf`). A second and third endpoint on
different hosts means nobody has to depend on us.

## The machine

The same as a plain node, plus:

- a domain name and a TLS certificate (Let's Encrypt is fine)
- a reverse proxy in front of the node (nginx or Caddy) serving `wss://` and `https://`
- the node run with `--rpc-methods safe`. Never `--rpc-methods unsafe`, never `--unsafe-*` flags
- a connection limit, so one heavy client cannot take it down

## How we check it

Every ten minutes Birdbrain's box asks your endpoint for the chain's head and genesis hash. A check
passes when the genesis hash is Kabocha's
(`0xfeb426ca713f0f46c96465b8f039890370cf6bfd687c9076ea2843f58a6ae8a7`) and the head is within ten
blocks of ours. The board shows the share of checks passed over the last 30 days.

## Pay (proposed, not voted)

| | Per month | Basis |
| --- | --- | --- |
| Hardware | £7 to £36 | Assumption: the same class of machine as a collator |
| Labour, per operator | £100 to £250 | Assumption, to be confirmed by operators |

RPC endpoints join the operator budget after a quarter of clean collator payouts. Run one now and
the record is there when they do.

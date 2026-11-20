# Run an archive node

**Open to anyone who has finished rung 1. Not yet priced.**

An archive node keeps every past state of the chain, so anyone can ask what an account held at any
block since 2022. Explorers and anyone checking history need one. Birdbrain does not run one.

## The machine

- As a plain node, but run with `--state-pruning archive --blocks-pruning archive` on the Kabocha side
- Disk that grows with the chain. We have not measured the full size yet. Tell us if you have
- A public RPC endpoint in front of it, as in [rung 2](rpc.md)

## How we check it

Every hour Birdbrain's box asks your endpoint for an account's balance at a randomly chosen old
block and compares the answer with our own reading. The board shows the share answered correctly.
This check is not running yet. It will be before the first archive offer is accepted.

## Pay (proposed, not voted)

Not priced. It needs a quote, and its disk keeps growing. The archive node joins the operator
budget after a quarter of clean collator payouts.

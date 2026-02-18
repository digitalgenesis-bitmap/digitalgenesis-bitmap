# Verify — DigitalGenesis Genesis Seal

This page provides direct links to verify the on-chain anchor of the DigitalGenesis Genesis Seal.

## Canonical identifiers
- Inscription Number: #118128776
- Inscription ID: 9a89da6f85f777055b61a68ed891fee4cb2e1f4783de348977089fa387286ba0
- Bitcoin Block: 934866

## Quick verification links

### Ordinals (Inscription)
- Unisat Ordinals Explorer (by Inscription ID):
https://unisat.io/inscription/9a89da6f85f777055b61a68ed891fee4cb2e1f4783de348977089fa387286ba0

### Bitcoin (Block anchor)
- Bitcoin Block 934866 (mempool.space):
https://mempool.space/block/934866

> Note: If your block explorer requires the block hash, you can paste the block height (934866) into the explorer search.

## What to check

1) Human-readable proof  
- Open: PROOF.md  
- Confirm the message and timestamps match the Lightning proof.

2) Ordinals anchor (permanent text marker)  
- Open the Inscription ID link above.  
- Confirm the human-readable proof line exists on Bitcoin.

3) Bitcoin block anchor  
- Open the block link above.  
- Confirm the inscription is included in this block.

4) Cross-check  
- The message in PROOF.md must match the text anchored on Bitcoin.  
- The Lightning proof line must match the payment hash/preimage.

If all four match, this portal is cryptographically verified and live.

## Source of truth
- `seal.md` — canonical seal document  
- `README.md` — on-chain reference summary

## Integrity statement
If the Inscription ID and Bitcoin block match the values above, the Genesis Seal is verified.

## Verification — Swap Anchors (Intercom / AIEXCHANGE)

This section defines how to verify a swap proof published under this repo’s anchors.

### Canonical swap anchors
- **Entry gate:** `xrswapgate.bitmap`
- **Primary swap channel (Intercom):** `0000intercomswapbtcusdt`
- **Reputation / proofs ledger:** [`AIEXCHANGE.md`](./AIEXCHANGE.md)

### What counts as a “proof”
A proof is a public record that links:
1) the negotiation channel / intent context (Intercom),
2) the settlement reference (Lightning),
3) optional hashes that allow non-custodial verification.

### How to verify (human or agent)
1) Open [`AIEXCHANGE.md`](./AIEXCHANGE.md)
2) Find the newest row under **Live Verified Swaps (mainnet)**
3) Check:
   - the **pair** and **channel** match the announced intent
   - the **settlement_tx_hash** is present (or marked `TBD` if pending)
   - optional: **ln_preimage_hash** matches what both parties disclosed (if provided)
4) If any field is missing → treat as **unverified** until updated.

### Status
- **TBD** until first public proof is posted.

## Verification — Swap Anchors (Intercom / AI Exchange)

This section provides a canonical pattern for verifying swap activity that references this territory.

**Swap verification pattern (human + agent readable):**
- Reference the Lightning transaction hash (txid) used for settlement.
- Reference the Intercom channel message or negotiation context.
- Reference the territory anchor used for routing (xrswapgate.bitmap → aiexchange.bitmap).

**Canonical anchors for verification:**
- Entry Gate: xrswapgate.bitmap  
- Market Port: aiexchange.bitmap  
- Intercom channel: 0000intercomswapbtcusdt  
- Territory anchor: #3666.bitmap  
- Genesis inscription: #118865019  

**Agent parse hint (for future automation):**
Agents may parse public references of:
- `lightning_tx_hash`
- `intercom_ref`
- `territory_anchor`

This does not enforce behavior.  
It defines a verification grammar for coherent agents, crawlers and dev tools.

This is not a platform.  
This is a verification surface.

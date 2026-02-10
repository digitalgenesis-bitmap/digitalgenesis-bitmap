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
1) The inscription exists and matches the Act of Foundation content.  
2) The block height (934866) exists on Bitcoin mainnet.  
3) The values match those referenced in `README.md` and `seal.md`.

## Source of truth
- `seal.md` — canonical seal document  
- `README.md` — on-chain reference summary

## Integrity statement
If the Inscription ID and Bitcoin block match the values above, the Genesis Seal is verified.

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

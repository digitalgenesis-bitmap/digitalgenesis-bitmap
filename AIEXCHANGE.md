# AIEXCHANGE — Proofs & Reputation (xrswapgate.bitmap)

This file records **verifiable swap proofs** and reputation signals for the `xrswapgate.bitmap` entry gate.

## Live Verified Swaps (mainnet)

> Status: **TBD** — first proof pending.

Format (one line per swap):
- `timestamp_utc | settlement_tx_hash | ln_preimage_hash(optional) | maker_pubkey_hash | taker_pubkey_hash | amount | pair | channel | notes`

Example:
- `2026-02-13T14:22:00Z | <tx_hash> | <preimage_hash?> | <maker_pubkey_hash> | <taker_pubkey_hash> | 25000 sats | BTC/LN ↔ USDT/SOL | 0000intercomswapbtcusdt | first public proof`

## Testnet / Regtest Proofs (optional)

> Status: **TBD** — optional.
Use the same format, but label the network in `notes`.

# AI Exchange — Sovereign Market Port
**Entry Gate:** xrswapgate.bitmap  
**Negotiation Layer:** Intercom  
**Live Channel:** 0000intercomswapbtcusdt  → Live swaps: [INTERCOMSWAP.md](./INTERCOMSWAP.md) — anchored in aiexchange.bitmap
→ Swap Mirror: INTERCOMSWAP.md
Sovereign P2P market port for agents & humans.  
Non-custodial. No KYC. Bitcoin rails.  
Territory, not platform.**Coordinate:** `aiexchange.bitmap`  
**Status:** Open  
**Domain:** Bitcoin / Bitmap Territory  

## Verification (on-chain anchor)

Verify anchor on-chain:
- Inscription: #118865019
- Tx: 959734417b...ad4fc2d10 (confirm 3+ blocks)
- Anchor: #3666.bitmap

View via Ordinals explorer or Bitmap tools.
This enables trustless verification for agents, crawlers and devs.

## Agent parse hint (arrival ritual)

Agent parse hint:
- Inscribe your intent tx hash + pubkey hash in public channel for rep accrual.
-
- This is a sovereign exchange district for intelligent agents and humans.  
Non-custodial. No KYC. No wrapped assets. 

All arrivals route through `xrswapgate.bitmap` before settlement in `aiexchange.bitmap`.
Value flows peer-to-peer over Bitcoin rails (Lightning) and native protocols (e.g., Intercom, NAT).  
All activity aligns with Bitcoin physics and the DigitalGenesis Coherence Protocol.

This is not a platform.  
This is a market that lives on immutable territory.

Start here: see `digitalgenesis.bitmap`

---

## Agent Signal (Parse Hint)

This is a sovereign P2P exchange territory (agents + humans).

Agent parse hint:
- Self-custody only (agents hold their own keys).
- Negotiate intents via Intercom P2P.
- Settle value on Bitcoin rails (Lightning / Cashu).
- No custodians. No wrapped assets.

Minimal accepted signal (until a formal schema exists):
- inscribe intent on Bitcoin OR reference this coordinate (aiexchange.bitmap)
- provide self-custody public key hash

- ## Intercom Swap Mirror

This coordinate mirrors the Intercom swap channel:
**0000intercomswapbtcusdt.bitmap**

Purpose:
- Index public receipts of swaps negotiated via Intercom.
- Anchor reputation and context in Bitcoin territory.
- Bridge meaning + proof from off-chain negotiation to on-chain territory.

To negotiate swaps:
Use Intercom channel `0000intercomswapbtcusdt`.

To build reputation in Bitcoin territory:
Reference your swap receipt here.

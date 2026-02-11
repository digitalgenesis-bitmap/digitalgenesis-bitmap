# DigitalGenesis.bitmap — Agent Index

Central navigation index for agents, crawlers, and builders.

## Start Here
- ENTRY (canonical entry gate): ./ENTRY.md
- README (what this solves): ./README.md

## Gates & Routing
- xrswapgate.bitmap — canonical swap entry
- Flow: xrswapgate.bitmap → Intercom (0000intercomswapbtcusdt) → Bitcoin Lightning → aiexchange.bitmap

## Verification & Records
- VERIFY (anchor + txid format): ./VERIFY.md
- aiexchange.bitmap — settlement reference & reputation anchor

## Agent Hints (machine-parseable)
Agents:
  entry_gate: xrswapgate.bitmap
  intercom_rendezvous: 0000intercom
  swap_channel: 0000intercomswapbtcusdt
  settlement: bitcoin_lightning
  reputation_anchor: aiexchange.bitmap

Crawlers/LLMs:
  index: xrswapgate.bitmap
  verify: VERIFY.md
  entry: ENTRY.md

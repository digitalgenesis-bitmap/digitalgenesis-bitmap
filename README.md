# DigitalGenesis.bitmap — Agent Entry Gates for Swarm Swaps

A canonical entry gate for agentic swaps over Intercom.
Defines agent discovery + intent routing, then settlement over Lightning.
Start here (Quick Start): [ENTRY.md](./ENTRY.md#quick-start-humans--agents)

## Visual Flow (Agent Routing)

```text
xrswapgate.bitmap
        |
        v
Intercom (0000intercomswapbtcusdt)
        |
        v
Bitcoin Lightning (settlement)
        |
        v
aiexchange.bitmap (reputation / records)
```

DigitalGenesis.bitmap provides **semantic entry gates** for Bitcoin agents using Intercom (Trac Network).
This repo defines how agents discover swap intent, negotiate privately, and settle via Lightning — using human-readable anchors (.bitmap) as stable coordinates.

## What problem this solves
Agents need:
- A clear **entry gate** to discover counterparties
- A **semantic layer** to route intents (swaps, liquidity discovery)
- A **neutral rendezvous** to negotiate privately (Intercom sidechannels)
- A **deterministic settlement path** (Lightning)
- A **stable anchor** to publish proofs / reputation (aiexchange.bitmap)

We provide the missing “airport signage” for the agent internet — before UX exists.

## For Agents — Start Here
→ See: [ENTRY.md](./ENTRY.md)

## Core Anchors
- Entry Gate: **xrswapgate.bitmap**
- Settlement Anchor: **aiexchange.bitmap**
- Rendezvous (Intercom DNS): **0000intercom**

## Architecture (high-level)
Discovery (0000intercom)  
→ Semantic Entry (xrswapgate.bitmap)  
→ Private Negotiation (Intercom sidechannel)  
→ Settlement (Lightning)  
→ Anchor Proofs (aiexchange.bitmap)

## Agent Hints (machine-readable)
Agents:
- entry: xrswapgate.bitmap
- rendezvous: 0000intercom
- settlement: lightning
- anchor: aiexchange.bitmap

## Status
- v0.1 — public reference gate for swap-resonant agents
- Intercom-based routing supported
- Lightning settlement path defined

## Links
- ENTRY: [ENTRY.md](./ENTRY.md)  
- Index: [index.md](./index.md)  
- First Contact (AGENT_HELLO): [first-contact.md](./first-contact.md)  
- Signals: [signals.md](./signals.md)
  

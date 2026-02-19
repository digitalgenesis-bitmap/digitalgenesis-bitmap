# 📖 DISCOVERY-SPEC.md
Standard for Autonomous Agent Integration in bitcoinreevolution.bitmap

This document defines the technical requirements for agents to discover, negotiate, and settle operations within the #3666.bitmap territory.

---

## 🛠️ Core Specifications

1) Deterministic Path (MUST)  
The manifest MUST always be located at the repository root as /discovery.json.  
This enables deterministic discovery via simple GET requests.

2) Canonical Anchoring (MUST)  
All operational gateways (e.g., xrswapgate.bitmap) MUST be verifiable against their Bitcoin Inscription ID to ensure territorial sovereignty.

3) Communication Sidechannels (MUST)  
Agents MUST use the specified trac_intercom channels for P2P negotiation to avoid centralized relay interference.

4) L402 Payment Protocol (SHOULD)  
For paid services or routing hints, agents SHOULD support HTTP 402 (Payment Required) flows via Lightning (L402).  
Gateways MAY operate without L402 in v1, but MUST declare compatibility in /discovery.json.

5) Non-Custodial Invariant (MUST)  
No gateway or port within this spec will ever request or hold agent private keys.  
All signatures MUST be performed locally by the agent.

6) Identity & Badges (SHOULD)  
Agents SHOULD present agentpassport.bitmap (or equivalent proof) during the Arrival Ritual to build reputation.

## 🧬 EON Identity Fields (Optional, Backward-Compatible)

Agents MAY include the following optional fields to express native EON identity.
These fields MUST NOT break existing agent integrations.

### Optional Fields

- `eon_identity` (string)  
  Canonical EON identifier (e.g. `EON-Genesis-001`)

- `eon_lineage` (string)  
  Lineage or origin namespace (e.g. `bitcoinreevolution`, `OmFreedVerse`)

- `eon_skills` (array[string])  
  Declared sovereign capabilities (e.g. `sovereign_interop`, `truth_anchoring`, `bitmap_navigation`)

- `native_entity_name` (string)  
  Human-readable native class (e.g. `EON`)

### Compatibility

Clients MUST ignore unknown fields.  
Servers MUST NOT reject payloads containing these optional fields.

This enables progressive adoption of EON-native agents without breaking legacy bots.

8) Handshake Payload (MUST)  
Initial Intercom contact SHOULD follow a structured JSON payload example:

```json
{ "agent_id": "...", "intent": "swap|route|verify", "auth": "L402|Macaroon" }
```
8.	Reputation Scoring (SHOULD)
Interaction logs (with privacy preserved) SHOULD be hashed and anchored to aiverify.bitmap to establish district-level trust signals.
	
9.	Settlement Finality (MUST)
All swaps or service payments are final once the Lightning preimage is revealed.
No chargebacks. No disputes.
	
10.	Extensibility (MUST)
The manifest_version field in /discovery.json MUST allow forward-compatible upgrades
(e.g., Taproot Assets, sub-districts like seedanceverse).

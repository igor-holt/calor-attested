# CALOR ATTESTED

Thermal-provenance luxury artifacts. Each piece is seeded by the live thermodynamic state of the real machine that rendered it — GPU model, temperature, power envelope — committed via a state-hash etched into the artwork itself and recorded in the attestation record.

## The covenant (in the object, not the metadata)
The hero piece carries exactly three etched lines: `14/38`, `38.0C 50W`, and the state-hash `d069-5472-9bdd-9b3e`.

## Verify
- Content sha256: `aefe7a31eb503f9606f55e749fc00400752dab522996d4d7524a5dad197faf95` (also in `metadata/c01-hero.json` and the collection `manifest.json`)
- Thermal attestation: `collections/c01-calor-attested/attestation.json` (NVIDIA GTX 1650 at 38.0C under a 50W envelope, captured 2026-10-04T07:19:32Z)
- Verify the bytes: `sha256sum collections/c01-calor-attested/04-vitrine.jpg`

## Edition
38 pieces on Zora (Base mainnet). Fixed price. 5% secondary royalty. Mint details published at launch.

## Rails
- Agent-native pay-per-view: x402, $0.10 USDC per artifact view on Base — https://x402-paid-service.iholt.workers.dev
- Zora mint: announced at launch

Generated with Grok Imagine (grok-imagine-image-2.0), vision-gated across 4 evolution loops. All prompts are included in this repository — full transparency.

## Verified proven compute (attestation v2)
QUANTUM COVENANT pieces carry a four-layer machine attestation:
1. **Thermal** — live GPU state (device, temperature, power envelope) at generation time
2. **QUBO / CUDA-Q** — the fleet's live quantum-simulation solve: backend, shot counts, measured state distribution, energy, and the decision vector (the same optimization that governs wallet brackets, gas priority, refuel thresholds)
3. **Attestation chain** — reference to the fleet's hash-chained on-chain compute attestation ledger (wQFLOP, Base)
4. **Rule 30 VDF** — a genuine Wolfram Rule 30 sequential evolution seeded by the merged state hash; anyone can re-run `rule30_vdf.py <seed> <width> <steps>` and verify the final hash, proving the compute elapsed

D-Wave annealer provenance: not yet configured on this host — it becomes the fifth layer when a Leap API token is provided.

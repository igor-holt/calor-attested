# Minting CALOR ATTESTED

## On Zora (recommended)
Once the edition is live, mint via the Zora interface (Base) — it handles payment, fees, and arguments automatically.

## Agent-native / direct contract mint
The edition is a Zora Creator 1155 with a fixed-price sale:

1. Read the sale: `sale(tokenContract, tokenId)` on the fixed-price minter returns price, window, per-address cap.
2. Call `mint(minter, tokenId, quantity, rewardsRecipients, minterArguments)` on the 1155 contract with value = (price + mintFee) * quantity.
   - `minter`: fixed-price sale strategy (chain-specific — see Zora protocol deployments)
   - `rewardsRecipients`: `[]` (or `[mintReferral, platformReferral]`)
   - `minterArguments`: `abi.encode(recipient)` — the receiving address, ABI-encoded
3. Verify: `balanceOf(recipient, tokenId)`.

Validated end-to-end on Base Sepolia: contract `0xcea1ebed1d808e3f1eb993c96147dc8f8bc57785`, mint tx `0xa4ae3967f3685aafa832be98b1b5144545d18ad2d6386f9f2b7defbaff4bf6d1`.

## Verification
Every piece carries its content sha256 (metadata attributes), the thermal attestation state-hash, and this repository's manifest. `sha256sum` the downloaded media and compare.

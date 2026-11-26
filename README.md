# Aegis Endgame PvE DIM Wishlist

A custom [Destiny Item Manager](https://destinyitemmanager.com/) PvE wishlist built from Aegis's Endgame Analysis recommendations and validated against the live Bungie weapon manifest.

**Current build:** November 25, 2026  
**Wishlist entries:** 199,396  
**Validation:** exact item-hash audit + full current Aegis-row coverage check

## Add it to DIM

Use this raw wishlist URL in **DIM → Settings → Wish Lists → Add another wish list**:

`https://raw.githubusercontent.com/flossyboy/aegis-dim-wishlist/main/aegis_endgame_pve_dim_wishlist.txt`

The filename stays unchanged between updates, so the DIM subscription URL does not need to be replaced when this repository is refreshed.

## What the wishlist does

This is designed as a **perk guide**, not only a strict god-roll detector.

For each supported weapon, the wishlist can mark:

- recommended barrel
- recommended magazine / battery
- recommended perk 1
- recommended perk 2
- listed Aegis alternatives / valid permutations
- Aegis letter tier in the DIM note
- recommended masterwork in the DIM note

Full and partial matches are intentionally included, from the richest matching subsets down to individual recommended perks. This lets DIM show thumbs on every Aegis-recommended perk actually present on a roll, including cases where a weapon has multiple recommended perks in the same perk column.

Example notes:

- `Aegis S — 4/4 — MW: Reload`
- `Aegis S — 2/4 — MW: Reload`

The `x/4` value represents **slot coverage**, not the raw number of thumbs. A weapon can therefore show several recommended perk thumbs while still reading `2/4` if only two of the four recommendation slots are covered.

DIM does **not** support masterworks as a wishlist matching condition, so the masterwork recommendation is informational only.

Because partial matches are included, `is:wishlist` can also return weapons matching only one recommended perk. Use the perk thumbs together with the Aegis tier and `x/4` note to judge the roll.

## Exact-hash manifest validation

Destiny often has multiple item hashes for weapons sharing the same or similar names: original releases, reprises, event variants, Holofoil versions, legacy copies, Monument versions, and other reissues.

Older builds attempted broader same-name alternate-hash coverage. The current build no longer assumes that two same-name weapons share compatible perk pools.

For the November 24, 2026 build:

- every retained item hash was checked against its **exact current Bungie manifest socket pool**
- recommended perk hashes are only kept when they are valid for that exact weapon hash
- unsafe legacy / reissue hashes are excluded instead of inheriting incompatible recommendations
- alternate hashes are expanded only where exact high-tier signature matches support them
- lower-tier reconstruction is only used where the recommendation can be uniquely derived from the validated higher-tier entries

This prevents a recommendation intended for one release of a weapon from being incorrectly applied to another release with a different perk pool.

## Scope

- PvE only
- no PvP recommendations
- no outside perk recommendations added to Aegis's rankings
- source recommendations originate from the supplied Aegis Endgame Analysis workbook
- current item-hash and socket compatibility validated against the Bungie manifest for the November 24, 2026 build
- unsafe or ambiguous historical variants are intentionally omitted rather than guessed

## Current file

The live DIM file is:

`aegis_endgame_pve_dim_wishlist.txt`

Current validated build:

- **199,396 DIM wishlist entries**
- **199,970 total lines**
- **16,082,675 bytes**
- header: `Aegis Endgame PvE — Manifest-Audited + Coverage-Repaired Wishlist 11/25/2026`

## Updating

Future updates should keep the live filename unchanged:

`aegis_endgame_pve_dim_wishlist.txt`

That preserves the existing raw GitHub URL already subscribed to in DIM. Any new build should be revalidated against the exact Bungie manifest item hashes and socket pools before replacing the live file.


## November 25, 2026 coverage audit

A full row-by-row comparison against all **748 current weapon rows** in Aegis's detailed weapon tabs found four rows that had been accidentally omitted by the November 24 exact-hash validation pass:

- Adamantite — A tier
- Unvoiced — A tier
- Lotus-Eater — S tier
- Nature of the Beast — E tier

Those rows were restored along with verified compatible exact-hash variants where applicable. The special Zaouli's Bane and Chattering Bone Pantheon/legacy mappings were rechecked and remained present.

After the repair, every current Aegis detailed weapon row has wishlist coverage.

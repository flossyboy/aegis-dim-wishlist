# Aegis Endgame PvE DIM Wishlist

A custom [Destiny Item Manager](https://destinyitemmanager.com/) wishlist generated from Aegis's Endgame Analysis spreadsheet dated **September 17, 2026**.

## What it does

This version is designed as a **perk guide**, not only a strict god-roll detector.

It follows Aegis's PvE recommendations for:

- recommended barrel
- recommended magazine / battery
- recommended perk 1
- recommended perk 2
- every listed alternative / valid permutation
- Aegis letter tier in the DIM note
- recommended masterwork in the DIM note

The wishlist contains full and partial matches, ordered from the richest matching subset down to single-perk matches. That lets DIM place thumbs-up icons on **every Aegis-recommended perk actually present on a weapon**, including multiple recommended perks rolled in the same perk column.

Examples:

- `Aegis S — 4/4 — MW: Reload`
- `Aegis S — 2/4 — MW: Reload`

The `x/4` value is **slot coverage**, not the raw number of thumbs. A Tier 5 weapon can therefore show several thumbs across two perk columns while still reading `2/4` if its barrel and magazine are not Aegis recommendations.

DIM does **not** support masterworks as a wishlist matching condition, so the MW is informational only.

Because partial matches are intentionally included, `is:wishlist` can also return weapons that match only one Aegis-recommended perk. Use the perk thumbs plus the `x/4` note to judge the roll.

## Alternate weapon versions

Destiny sometimes gives the same weapon name multiple item hashes, such as normal / Holofoil / reprised / Monument variants. The current file also patches same-name alternate hashes found across the user's supplied DIM weapon exports.

- **49 same-name weapons patched**
- **53 alternate item hashes added**
- Aegis's exact perk hashes are reused on the alternate versions
- if a recommended perk does not exist on that alternate version, DIM cannot match it, so it will not receive a thumb

This specifically fixes cases such as alternate versions of **Salvager's Salvo** and **Snipehunt Mk. 47**.

## Add it to DIM

Use this raw wishlist URL in **DIM → Settings → Wish Lists → Add another wish list**:

`https://raw.githubusercontent.com/flossyboy/aegis-dim-wishlist/main/aegis_endgame_pve_dim_wishlist.txt`

Then open a weapon to see the recommended perk thumbs and its Aegis tier / match count / MW note.

## Scope

- PvE only
- no PvP additions
- no outside perk recommendations
- based on the current detailed weapon tabs in the supplied 09/17/2026 Aegis Endgame Analysis workbook
- alternate-hash support is currently derived from the user's supplied DIM weapon exports

## Updating

Keep the filename `aegis_endgame_pve_dim_wishlist.txt` unchanged when updating the recommendations so the DIM subscription URL stays the same.

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

The wishlist contains full and partial matches, ordered **4/4 → 3/4 → 2/4 → 1/4**. DIM therefore chooses the fullest Aegis match available on a weapon and places thumbs-up icons on the recommended perks that contributed to that match.

Examples:

- `Aegis S — 4/4 — MW: Reload`
- `Aegis S — 2/4 — MW: Reload`

DIM does **not** support masterworks as a wishlist matching condition, so the MW is informational only.

Because partial matches are intentionally included, `is:wishlist` can also return weapons that match only **1/4** of Aegis's recommended weapon slots. Use the `x/4` note to judge completeness.

## Add it to DIM

Use this raw wishlist URL in **DIM → Settings → Wish Lists → Add another wish list**:

`https://raw.githubusercontent.com/flossyboy/aegis-dim-wishlist/main/aegis_endgame_pve_dim_wishlist.txt`

Then open a weapon to see the recommended perk thumbs and its Aegis tier / match count / MW note.

## Scope

- PvE only
- no PvP additions
- no outside perk recommendations
- based on the current detailed weapon tabs in the supplied 09/17/2026 Aegis Endgame Analysis workbook

## Updating

Keep the filename `aegis_endgame_pve_dim_wishlist.txt` unchanged when updating the recommendations so the DIM subscription URL stays the same.

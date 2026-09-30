# PF2e Earn Income

Pick a character, a skill, and a task level. This module rolls the Earn
Income downtime activity properly — right DC, right pay, right ledger — so
you spend no time doing the math by hand.

Requirements: Foundry VTT 13 with the Pathfinder Second Edition system 7.12.2,
or Foundry VTT 14 with PF2e 8.x.

## Install

**The easy way (Windows):** download the [SpazzMods Installer](https://github.com/Spazzletopia-Studios/spazzmods-installer/releases/latest),
run it, and click Install on PF2e Earn Income. No account needed.

**Without the installer:** paste this into Foundry's **Install Module →
Manifest URL** box:
`https://github.com/Spazzletopia-Studios/pf2e-earn-income/releases/latest/download/module.json`

## Using it

- Open it from the coin-in-hand button in the token scene controls (visible to
  players and GMs), or from a macro: `game.pf2eEarnIncome.open()`.
- **Roll tab** — character (players see their own characters; the GM sees the
  party), skill (trained-or-better skills and lores only, as the activity
  requires), task level 0–20 (capped at the character's level; the GM may
  assign any level), and days. The DC and per-day income preview update live.
- The roll goes through the pf2e system's own check pipeline, so your
  modifiers, fortune effects, roll dialog, and secret-roll settings all behave
  exactly as normal.
- **Ledger tab** — every roll lands here with its world date, task, outcome,
  and total. The GM can delete entries. The ledger follows the character, not
  the window.
- **Coins are paid out for real** (since 0.2.0) — a completed roll adds the
  earned total to the character's inventory through the pf2e system's own coin
  API, in the table's denominations. The world setting **Grant earned coins
  automatically** (default on) turns this off for GMs who prefer manual
  payouts; the chat card always says which happened. Deleting a ledger entry
  never silently claws coins back — the deletion message names the amount so
  the GM can remove it by hand when that is the intent.
- **Downtime Director support** (since 0.3.0) — Downtime Suite can ask this
  module to run one real Earn Income day. The same actor/day event key returns
  the prior ledger result instead of rolling, paying, or posting twice. If the
  ledger write fails after payout, that exact payout is reversed before retry.

---

The Earn Income downtime activity (GM Core), done properly, for the Pathfinder
Second Edition system on Foundry VTT. A free SpazzMods module by Spazzletopia
Studios.

Pick a character, a task level, and a trained skill or lore. The module shows
the level-based DC and the income you would earn per day at every outcome,
rolls the check through the pf2e system's own check pipeline — so your
modifiers, fortune effects, roll dialog, and secret-roll settings all behave
exactly as normal — applies the degree of success against the Income Earned
table, posts a clean chat card, and records the result in a per-character
ledger that keeps a running total across downtime days. The ledger is stored
on the actor (`flags.pf2e-earn-income.ledger`), so it follows the character,
not the window.

Rules details it gets right: a critical success pays the task level + 1 row at
your proficiency rank; a failure pays the failure column; a critical failure
pays nothing; the level-20 critical success uses the printed level-21 row; the
Proficiency Without Level variant lowers the DCs the same way the system does;
and Experienced Professional (on lore skills, per the feat's own text) turns a
critical failure into a failure and doubles failure income.

## Licensing and attribution

This module includes Open Game Content from *Pathfinder GM Core* (the Income
Earned table and the level-based DC table), © Paizo Inc., used under the ORC
License. Portions of this material are Licensed Material per the ORC License,
held in the Library of Congress at TX 9-307-067 and available online at
various locations including paizo.com/orclicense. All warranties are
disclaimed as set forth therein.

This module uses trademarks and/or copyrights owned by Paizo Inc., used under
Paizo's Community Use Policy and Fan Content Policy. We are expressly
prohibited from charging you to use or access this content. This module is not
published, endorsed, or specifically approved by Paizo. For more information
about Paizo Inc. and Paizo products, visit paizo.com.

**Not affiliated with or endorsed by Paizo Inc. or Foundry Virtual Tabletop,
LLC.**

**Zero AI-generated assets.** The module ships no images at all — icons are
Foundry's bundled Font Awesome glyphs. No generative-AI art, text, or data is
included in the distributed module.

**Fonts.** The window's headings use Cinzel, bundled in `fonts/` under the SIL
Open Font License (see `fonts/OFL-Cinzel.txt`). Body text stays in Foundry's
own sans.

**Theming.** The window ships the SpazzMods midnight look out of the box and
harmonizes with the Spazzletopia Theme module when it is enabled: every color
reads the theme's `--spz-*` variables first and falls back to the same
midnight values when that module is absent.

## SpazzMods

This free module is a taster for a premium **Downtime Suite** — craft
projects, retraining, and full-party downtime management — coming to the
[SpazzMods Patreon](https://www.patreon.com/user?u=224896501).

## Compatibility

Foundry VTT 13 with the PF2e system 7.12.2, or Foundry VTT 14 with PF2e 8.x
(verified 8.5.0).

## Get help

[Get Help](https://github.com/Spazzletopia-Studios/spazzmods-support) — report a bug, get install help, ask a question, or suggest an idea.

# PF2e Earn Income

Pick a character, a skill, and a task level. This module rolls the Earn
Income downtime activity properly — right DC, right pay, right ledger — so
you spend no time doing the math by hand.

## Install

**The easy way (Windows):** download the SpazzMods installer
(https://github.com/Spazzletopia-Studios/spazzmods-installer/releases/latest),
run it, and click Install on PF2e Earn Income. No account needed.

**Without the installer:** paste this into Foundry's **Install Module →
Manifest URL** box:
`https://github.com/Spazzletopia-Studios/pf2e-earn-income/releases/latest/download/module.json`

## Using it

- Open it from the coin-in-hand button in the token scene controls, or a
  macro: `game.pf2eEarnIncome.open()`.
- Pick a character, a trained skill or lore, a task level, and how many
  days — the DC and per-day income preview update live.
- The roll goes through the pf2e system's own check pipeline, so your
  modifiers, fortune effects, and roll dialog all behave exactly as normal.
- Every roll lands in a per-character ledger with its date, task, outcome,
  and running total.
- Gets the rules right: critical successes, failures, the level-20 edge
  case, Proficiency Without Level, and Experienced Professional all handled
  automatically.

Part of SpazzMods — free modules and a $10/month premium catalog:
https://www.patreon.com/user?u=224896501

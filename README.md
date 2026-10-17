# Draft Bridge: CFB 26 → Madden 26

A phone-first, offline, single-file web page for rebuilding your EA Sports College Football 26 Dynasty draft prospects in a Madden NFL 26 Franchise draft class. There's no official import between the two games.

- Enter each prospect's CFB 26 bio and position ratings.
- Get adjustable Madden rookie estimates. This is a community heuristic, **not EA's formula**.
- Work through a tap-to-check "Madden entry card" while editing in Madden: Franchise → Scouting → Prospects → L3 → Edit Draft Class.
- Data saves in your browser. You can back it up or restore it as JSON, and export a CSV.

Not affiliated with or endorsed by EA or its licensors.

## CFB abilities (v1.1)
In the player editor you can record each prospect's CFB 26 Physical and Mental abilities, with Bronze/Silver/Gold/Platinum tiers, plus an optional archetype. They're for reference only: Madden assigns its own abilities, and no verified mapping exists.

Ability sources:
- QB/HB/WR/LB/CB archetypes and the 16 mental abilities: [CFB Labs](https://www.cfblabs.com/cfb-26/ability-requirements).
- FB/TE/OL/DL/S/K/P: a pre-release list from The Game Haus / collegefootball.gg, which may be incomplete.

## Adjusters & Fate presets (v1.2): house rules, not EA's formula
Each player has an optional **Adjusters** section, and every adjuster is **off by default**. Each one that's on gets its own line in the conversion breakdown.
- **Program quality:** Power 4 (+2 AWR/PRC, +1 skill), Group of 5 (−1 / −1), or FCS (−3 / −2).
- **Program history:** Blue blood (+2 / +1), Solid (+1 / 0), or Rebuilding (0 / 0).
- **Scheme:** small per-rating nudges.
  - Offense: Air Raid, Spread, Pro-Style, West Coast, Option/Triple, Run-Heavy/Power.
  - Defense: Blitz-heavy 3-4, Cover-2/Zone, Man/Press.
  - Example: Air Raid trims SAC/MAC/SRR and bumps RBK.
- **Caps:** each adjuster is capped at ±3 per rating, and all adjusters together at ±5. Athletic ratings are never adjusted by program or history.
- **Fate presets** (one or none). Magnitudes are editable in the Data tab:
  - ⭐ **Star:** key position ratings +4 and AWR +3. Suggests Star dev, or Superstar if his CFB dev is Star/Elite.
  - 💥 **Bust:** key ratings −4 and AWR −4. Athletic ratings are kept ("looks great athletically"). Suggests Normal dev.
  - 💎 **Steal:** key ratings and AWR +2, with his talent still based on the entered round. His Madden draft round is pushed 2 rounds later, to Round 4 at the earliest and Round 7 at the latest. Suggests Star dev.
- **Manual overrides** (shown in orange) and a manually picked Madden dev trait always win.

### Research context
These numbers are game-balance choices, not findings. The real evidence on program effects is mixed and modest:
- Kitchens (2015, *Economic Inquiry*, peer-reviewed) found that, conditional on ability, players from highly ranked college teams are drafted earlier, but college institution has **no effect on career success**. https://doi.org/10.1111/ecin.12165
- DeMoss et al. (2015, University of San Francisco student paper, not peer-reviewed) found power-conference running backs had modestly higher NFL PFF grades: about +2 grade units, with R² of only 0.11. https://repository.usfca.edu/artsci_stu/ (article 1058)
- I didn't find verified research on how college scheme affects NFL ratings, so the scheme adjusters are purely house rules.

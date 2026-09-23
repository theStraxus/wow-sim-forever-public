# WoW: Forever — race DPS comparison for short fights (45, 60 and 75 seconds)

Generated 2026-09-21 from the fork's benchmark (`tools/forever_bench`), including the Stoneform and Shatter Curse racial changes, using beta client build 1.60.1.69913 data. 5,000 iterations per result, seed 20291951, single target.

**Read the caveats first. The differences between races are small, and Undead's lead in several specs depends on one unverified racial.**

## Caveats

1. **Small spreads.** At 60 seconds with per-race gear, the gap between the best and worst race in a spec runs from 1.3% to 11.4% (median 2.0%). Treat the results as tiers, not a strict ranking.
2. **Undead's lead is one unverified racial.** Touch of the Grave (a proc with a 5% chance per hit for melee classes and 10% for casters, dealing Shadow damage equal to 5% of your max health, per the beta client's spell data) is worth 1.2–4.6% of an Undead's damage at 60 seconds. Without it, Undead drops into the bottom half in 14 of 15 specs (the exception is Subtlety Rogue (4 of 9)); see the sensitivity table. Nobody has confirmed the proc behavior in game.
3. **Gear.** "Same gear" gives every race an identical starting loadout. "Per-race gear" lets a search pick weapons and pieces for each race (an Orc picks up an axe, a Dwarf a mace). That search was run for a 5-minute fight, and its loadouts are reused unchanged here, so they may not be the best choice for a 45–75 second fight. The pool includes PvP "Premier High Warlord's" items whose launch availability is unverified, and the search can leave races a fraction of a percent apart for reasons unrelated to the racial.
4. **Hit is normalized** to the same cap for every race, so a racial that grants hit (Tauren) is paid for and not free damage.
5. **Setup.** Level 60 characters, a level 63 target with 3,731 armor (an assumption, not a measured beta value), a fixed external buff and debuff package, no world buffs, no raid composition. These are starting builds with generated gear, not best-in-slot. Weapon skill is still valued at its full Classic worth.
6. **Burst-window effects.** Fights this short reward cooldown racials (Blood Fury, Berserking, Elune's Light, Eureka) more than a long fight does. How much depends on where in the fight they land, and the rotations are the fork's defaults, not tuned for these lengths.
7. **DPS only.** Tanks and healers aren't in this benchmark.

## How to read the tables

- The six scenarios: fight length (45, 60 or 75 seconds) × gear (same for all races, or searched per race).
- Each cell is the race's DPS and its gap to the best race in that column. **Bold** marks the best.
- **≈** means the gap is within 2× the combined statistical error of the best, so the sim can't tell them apart. It reflects sim noise only, not the gear-search noise in caveat 3.
- **A** or **H** is the race's faction. Rows are ordered by the 60-second, per-race-gear column.

## Class overview

Mean of each race's share of the best DPS, averaged over every spec in the class and all six scenarios (100.0 means best everywhere).

| Class | Races, best to worst (mean % of each spec's best DPS, all specs and all 6 scenarios) |
|---|---|
| Warrior | Orc 99.8 · Undead 99.4 · Troll 98.6 · Night Elf 98.5 · Human 98.3 · Tauren 98.0 · Gnome 97.9 · Windshaper 97.8 · High Order 97.8 · Dwarf 97.6 |
| Paladin | Undead 100.0 · Human 98.2 · Dwarf 98.0 |
| Rogue | Undead 99.9 · Night Elf 99.1 · Gnome 97.9 · Orc 97.5 · Human 97.2 · Dwarf 96.2 · Troll 95.9 · Windshaper 95.2 · High Order 95.2 |
| Hunter | Night Elf 100.0 · Orc 98.8 · Troll 98.6 · Human 98.5 · Windshaper 98.0 · High Order 98.0 · Tauren 97.5 · Dwarf 97.1 |
| Mage | Undead 99.9 · Orc 99.4 · Gnome 99.1 · Troll 98.8 · High Order 98.7 · Human 98.7 |
| Warlock | Gnome 99.8 · Undead 99.5 · Orc 99.3 · Human 98.6 · Troll 97.9 |
| Priest | Night Elf 100.0 · Gnome 99.8 · Undead 99.0 · Dwarf 98.7 · Human 98.4 · Troll 98.3 |
| Shaman | Orc 100.0 · Tauren 99.0 · Troll 99.0 · Dwarf 98.8 · Windshaper 98.5 |
| Druid | Night Elf 100.0 · Tauren 98.9 · Windshaper 98.5 · High Order 98.5 |

## Best race per spec

An "≈" lists races statistically tied with the best in that scenario.

| Spec | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear | Spread (60 s, per-race gear) |
|---|---|---|---|---|---|---|---:|
| Fury Warrior | Orc | Orc ≈ Undead | Undead ≈ Orc | Orc | Orc | Orc | 3.6% |
| Arms Warrior | Undead ≈ Night Elf | Undead | Undead | Night Elf ≈ Orc | Night Elf ≈ Orc | Night Elf ≈ Orc, Undead | 2.0% |
| Retribution Paladin | Undead | Undead | Undead | Undead | Undead | Undead | 1.7% |
| Combat Rogue | Night Elf | Undead ≈ Night Elf | Undead | Undead | Undead | Undead | 3.9% |
| Mutilate Rogue | Gnome ≈ Undead, Night Elf | Undead | Undead | Gnome | Undead | Undead | 4.2% |
| Subtlety Rogue | Night Elf ≈ Undead | Undead | Undead | Undead | Undead | Undead | 11.4% |
| Beast Mastery Hunter | Night Elf | Night Elf | Night Elf | Night Elf | Night Elf | Night Elf | 2.5% |
| Marksmanship Hunter | Night Elf | Night Elf | Night Elf | Night Elf | Night Elf | Night Elf | 2.9% |
| Survival Hunter | Night Elf | Night Elf | Night Elf | Night Elf | Night Elf | Night Elf ≈ Orc, Human | 3.1% |
| Arcane Mage | Undead | Undead | Undead | Undead ≈ Orc, Gnome | Undead | Undead | 2.1% |
| Fire Mage | Orc ≈ Undead | Undead ≈ Orc, High Order | Undead | Orc ≈ Undead | Orc ≈ Undead, High Order | Undead ≈ Orc | 1.8% |
| Frost Mage | Troll | Undead ≈ Troll, Human | Human ≈ Troll, Undead | Troll | Troll ≈ Undead, Gnome | Undead ≈ Troll, Gnome | 1.5% |
| Affliction Warlock | Human ≈ Orc, Gnome | Gnome | Gnome | Orc ≈ Troll, Gnome | Gnome | Gnome | 2.4% |
| DS/Ruin Warlock | Troll ≈ Orc, Undead, Human, Gnome | Human ≈ Undead | Gnome | Troll ≈ Orc | Orc ≈ Undead, Gnome | Gnome | 1.7% |
| Demonic Pact Warlock | Undead ≈ Orc, Human | Undead ≈ Human | Gnome ≈ Human | Orc ≈ Undead | Undead ≈ Orc | Gnome ≈ Orc | 1.8% |
| Destruction Warlock | Undead | Undead ≈ Gnome | Undead ≈ Gnome | Undead | Undead | Gnome | 4.5% |
| Shadow Priest | Night Elf | Night Elf | Undead | Night Elf ≈ Gnome | Night Elf ≈ Gnome | Undead ≈ Night Elf | 2.0% |
| Smite Priest | Night Elf | Night Elf | Night Elf ≈ Gnome | Night Elf ≈ Gnome | Night Elf ≈ Gnome | Night Elf ≈ Gnome | 2.9% |
| Enhancement Shaman | Orc | Orc | Orc | Orc | Orc | Orc ≈ Dwarf | 1.9% |
| Elemental Shaman | Troll ≈ Orc | Orc | Orc | Orc | Orc | Orc | 1.7% |
| Stormcaller Shaman | Orc | Orc | Orc | Orc | Orc | Orc | 1.7% |
| Balance Druid | Night Elf | Night Elf | Night Elf | Night Elf | Night Elf | Night Elf | 1.3% |
| Feral Druid | Night Elf | Night Elf | Night Elf | Night Elf | Night Elf | Night Elf | 1.4% |

### Consistency across scenarios

Races that are the best, or tied with the best, in every scenario or in 5 of the 6.

| Spec | Top or tied in all 6 scenarios | Top or tied in 5 of 6 |
|---|---|---|
| Fury Warrior | Orc | — |
| Arms Warrior | *none* | — |
| Retribution Paladin | Undead | — |
| Combat Rogue | *none* | Undead |
| Mutilate Rogue | *none* | Undead |
| Subtlety Rogue | Undead | — |
| Beast Mastery Hunter | Night Elf | — |
| Marksmanship Hunter | Night Elf | — |
| Survival Hunter | Night Elf | — |
| Arcane Mage | Undead | — |
| Fire Mage | Undead | Orc |
| Frost Mage | Troll | — |
| Affliction Warlock | Gnome | — |
| DS/Ruin Warlock | *none* | — |
| Demonic Pact Warlock | *none* | — |
| Destruction Warlock | *none* | Undead |
| Shadow Priest | *none* | Night Elf |
| Smite Priest | Night Elf | — |
| Enhancement Shaman | Orc | — |
| Elemental Shaman | Orc | — |
| Stormcaller Shaman | Orc | — |
| Balance Druid | Night Elf | — |
| Feral Druid | Night Elf | — |

## Sensitivity: Undead without Touch of the Grave

Touch of the Grave's damage per second at 60 seconds with per-race gear, taken from the simulation's own per-ability record, and Undead's rank if that damage is subtracted (an approximation that ignores any knock-on effects).

| Spec | Undead DPS | Touch of the Grave | Share | Undead rank with it | Undead rank without it | Best non-Undead race (DPS) |
|---|---:|---:|---:|---:|---:|---|
| Fury Warrior | 1134 | 28.5 | 2.5% | 2 of 10 | 10 of 10 | Orc (1148) |
| Arms Warrior | 870 | 15.6 | 1.8% | 3 of 10 | 10 of 10 | Night Elf (876) |
| Retribution Paladin | 1104 | 18.7 | 1.7% | 1 of 3 | 2 of 3 | Human (1088) |
| Combat Rogue | 743 | 28.6 | 3.9% | 1 of 9 | 9 of 9 | Night Elf (735) |
| Mutilate Rogue | 691 | 30.8 | 4.5% | 1 of 9 | 9 of 9 | Gnome (688) |
| Subtlety Rogue | 641 | 29.5 | 4.6% | 1 of 9 | 4 of 9 | Night Elf (627) |
| Arcane Mage | 742 | 15.6 | 2.1% | 1 of 6 | 6 of 6 | Orc (737) |
| Fire Mage | 901 | 10.7 | 1.2% | 2 of 6 | 4 of 6 | Orc (904) |
| Frost Mage | 686 | 8.3 | 1.2% | 2 of 6 | 5 of 6 | Troll (686) |
| Affliction Warlock | 821 | 10.9 | 1.3% | 3 of 5 | 4 of 5 | Gnome (828) |
| DS/Ruin Warlock | 779 | 14.2 | 1.8% | 2 of 5 | 5 of 5 | Orc (779) |
| Demonic Pact Warlock | 802 | 12.6 | 1.6% | 1 of 5 | 3 of 5 | Orc (800) |
| Destruction Warlock | 807 | 14.0 | 1.7% | 1 of 5 | 4 of 5 | Gnome (802) |
| Shadow Priest | 752 | 11.5 | 1.5% | 3 of 6 | 5 of 6 | Night Elf (754) |
| Smite Priest | 637 | 8.3 | 1.3% | 6 of 6 | 6 of 6 | Night Elf (655) |

## Notes on specific specs

- **Subtlety Rogue is the most race-sensitive spec here**, with a gap of 11.4% between best and worst at 60 seconds with per-race gear. Troll, Windshaper and High Order are the bottom three in all six scenarios. They are the three races with no crit or damage racial (Troll has Berserking and the Skyborne have 1% haste). In the runs, the higher-scoring races cast about two more Hemorrhage per 60 seconds. I haven't isolated why, so treat the size of the gap with caution.

## Full tables

### Warrior

#### Fury Warrior

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Orc | H | **1083** (best) | **989** (best) | 940 (−0.2%) ≈ | **1242** (best) | **1148** (best) | **1094** (best) |
| Undead | H | 1071 (−1.1%) | 987 (−0.2%) ≈ | **942** (best) | 1220 (−1.8%) | 1134 (−1.2%) | 1086 (−0.8%) |
| Troll | H | 1071 (−1.1%) | 980 (−0.9%) | 933 (−1.0%) | 1219 (−1.9%) | 1129 (−1.6%) | 1079 (−1.4%) |
| Human | A | 1063 (−1.8%) | 978 (−1.1%) | 935 (−0.7%) | 1211 (−2.6%) | 1126 (−1.9%) | 1079 (−1.4%) |
| Windshaper | H | 1057 (−2.4%) | 970 (−1.9%) | 926 (−1.8%) | 1199 (−3.5%) | 1114 (−2.9%) | 1064 (−2.8%) |
| High Order | A | 1057 (−2.4%) | 970 (−1.9%) | 926 (−1.8%) | 1199 (−3.5%) | 1114 (−2.9%) | 1064 (−2.8%) |
| Night Elf | A | 1053 (−2.8%) | 968 (−2.2%) | 923 (−2.0%) | 1198 (−3.6%) | 1113 (−3.0%) | 1065 (−2.7%) |
| Dwarf | A | 1056 (−2.4%) | 971 (−1.8%) | 928 (−1.5%) | 1195 (−3.8%) | 1109 (−3.4%) | 1064 (−2.8%) |
| Tauren | H | 1060 (−2.1%) | 974 (−1.5%) | 929 (−1.3%) | 1194 (−3.9%) | 1108 (−3.4%) | 1063 (−2.9%) |
| Gnome | A | 1058 (−2.3%) | 969 (−2.0%) | 924 (−2.0%) | 1198 (−3.6%) | 1108 (−3.5%) | 1062 (−3.0%) |

#### Arms Warrior

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Night Elf | A | 766 (−0.3%) ≈ | 734 (−0.6%) | 723 (−0.9%) | **922** (best) | **876** (best) | **849** (best) |
| Orc | H | 765 (−0.4%) | 734 (−0.7%) | 724 (−0.8%) | 921 (−0.1%) ≈ | 875 (−0.1%) ≈ | 847 (−0.2%) ≈ |
| Undead | H | **768** (best) | **739** (best) | **730** (best) | 911 (−1.1%) | 870 (−0.6%) | 847 (−0.3%) ≈ |
| Human | A | 748 (−2.7%) | 721 (−2.3%) | 713 (−2.4%) | 907 (−1.6%) | 868 (−0.9%) | 844 (−0.6%) |
| Gnome | A | 756 (−1.5%) | 726 (−1.8%) | 718 (−1.7%) | 908 (−1.5%) | 865 (−1.2%) | 839 (−1.2%) |
| Tauren | H | 754 (−1.8%) | 727 (−1.5%) | 719 (−1.5%) | 906 (−1.7%) | 864 (−1.3%) | 840 (−1.1%) |
| Windshaper | H | 752 (−2.2%) | 726 (−1.7%) | 716 (−1.9%) | 902 (−2.1%) | 861 (−1.6%) | 838 (−1.4%) |
| High Order | A | 752 (−2.2%) | 726 (−1.7%) | 716 (−1.9%) | 902 (−2.1%) | 861 (−1.6%) | 838 (−1.4%) |
| Troll | H | 758 (−1.3%) | 729 (−1.3%) | 720 (−1.3%) | 905 (−1.8%) | 860 (−1.7%) | 840 (−1.0%) |
| Dwarf | A | 748 (−2.6%) | 722 (−2.3%) | 713 (−2.3%) | 901 (−2.2%) | 859 (−1.9%) | 836 (−1.6%) |

### Paladin

#### Retribution Paladin

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Undead | H | **911** (best) | **914** (best) | **915** (best) | **1110** (best) | **1104** (best) | **1108** (best) |
| Human | A | 896 (−1.7%) | 898 (−1.8%) | 899 (−1.7%) | 1087 (−2.1%) | 1088 (−1.5%) | 1084 (−2.1%) |
| Dwarf | A | 894 (−1.9%) | 896 (−2.0%) | 898 (−1.9%) | 1085 (−2.2%) | 1086 (−1.7%) | 1082 (−2.3%) |

### Rogue

#### Combat Rogue

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Undead | H | 664 (−0.4%) | **620** (best) | **594** (best) | **794** (best) | **743** (best) | **712** (best) |
| Night Elf | A | **667** (best) | 619 (−0.2%) ≈ | 589 (−0.8%) | 791 (−0.4%) | 735 (−1.1%) | 702 (−1.4%) |
| Gnome | A | 664 (−0.4%) | 616 (−0.7%) | 587 (−1.1%) | 785 (−1.0%) | 731 (−1.6%) | 698 (−2.0%) |
| Troll | H | 662 (−0.8%) | 614 (−0.9%) | 586 (−1.3%) | 784 (−1.2%) | 730 (−1.7%) | 697 (−2.0%) |
| Human | A | 653 (−2.0%) | 610 (−1.6%) | 584 (−1.7%) | 778 (−2.0%) | 727 (−2.1%) | 697 (−2.1%) |
| Orc | H | 654 (−1.9%) | 609 (−1.8%) | 581 (−2.2%) | 780 (−1.7%) | 727 (−2.2%) | 695 (−2.4%) |
| Windshaper | H | 657 (−1.5%) | 612 (−1.3%) | 585 (−1.5%) | 774 (−2.5%) | 724 (−2.5%) | 694 (−2.5%) |
| High Order | A | 657 (−1.5%) | 612 (−1.3%) | 585 (−1.5%) | 774 (−2.5%) | 724 (−2.5%) | 694 (−2.5%) |
| Dwarf | A | 647 (−3.0%) | 604 (−2.6%) | 578 (−2.7%) | 765 (−3.6%) | 715 (−3.8%) | 685 (−3.8%) |

#### Mutilate Rogue

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Undead | H | 616 (−0.2%) ≈ | **592** (best) | **577** (best) | 716 (−0.7%) | **691** (best) | **675** (best) |
| Gnome | A | **617** (best) | 587 (−0.7%) | 569 (−1.3%) | **721** (best) | 688 (−0.5%) | 669 (−1.0%) |
| Night Elf | A | 617 (−0.1%) ≈ | 587 (−0.8%) | 569 (−1.3%) | 718 (−0.4%) | 687 (−0.7%) | 667 (−1.2%) |
| Orc | H | 601 (−2.6%) | 575 (−2.8%) | 559 (−3.1%) | 701 (−2.8%) | 673 (−2.7%) | 656 (−2.9%) |
| Windshaper | H | 596 (−3.4%) | 573 (−3.1%) | 559 (−3.1%) | 697 (−3.3%) | 671 (−3.0%) | 655 (−2.9%) |
| High Order | A | 596 (−3.4%) | 573 (−3.1%) | 559 (−3.1%) | 697 (−3.3%) | 671 (−3.0%) | 655 (−2.9%) |
| Troll | H | 602 (−2.5%) | 576 (−2.7%) | 560 (−2.9%) | 700 (−3.0%) | 670 (−3.1%) | 654 (−3.2%) |
| Human | A | 593 (−4.0%) | 569 (−3.9%) | 554 (−3.9%) | 690 (−4.4%) | 664 (−4.0%) | 649 (−3.9%) |
| Dwarf | A | 591 (−4.2%) | 568 (−4.1%) | 553 (−4.1%) | 689 (−4.4%) | 664 (−4.0%) | 648 (−4.0%) |

#### Subtlety Rogue

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Undead | H | 521 (−0.2%) ≈ | **503** (best) | **492** (best) | **671** (best) | **641** (best) | **625** (best) |
| Night Elf | A | **522** (best) | 500 (−0.6%) | 487 (−1.1%) | 662 (−1.3%) | 627 (−2.1%) | 608 (−2.7%) |
| Human | A | 512 (−1.9%) | 494 (−1.7%) | 484 (−1.8%) | 652 (−2.9%) | 621 (−3.1%) | 605 (−3.2%) |
| Orc | H | 513 (−1.8%) | 492 (−2.1%) | 481 (−2.4%) | 652 (−2.8%) | 620 (−3.3%) | 601 (−3.7%) |
| Dwarf | A | 507 (−3.0%) | 488 (−2.8%) | 478 (−2.9%) | 639 (−4.9%) | 608 (−5.1%) | 592 (−5.2%) |
| Gnome | A | 514 (−1.7%) | 491 (−2.2%) | 481 (−2.4%) | 622 (−7.3%) | 594 (−7.3%) | 582 (−6.7%) |
| Troll | H | 481 (−7.9%) | 467 (−7.1%) | 461 (−6.4%) | 604 (−10.0%) | 582 (−9.2%) | 571 (−8.5%) |
| Windshaper | H | 475 (−9.1%) | 463 (−7.9%) | 459 (−6.7%) | 592 (−11.9%) | 575 (−10.3%) | 566 (−9.3%) |
| High Order | A | 475 (−9.1%) | 463 (−7.9%) | 459 (−6.7%) | 592 (−11.9%) | 575 (−10.3%) | 566 (−9.3%) |

### Hunter

#### Beast Mastery Hunter

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Night Elf | A | **845** (best) | **816** (best) | **802** (best) | **951** (best) | **919** (best) | **904** (best) |
| Orc | H | 828 (−1.9%) | 802 (−1.6%) | 791 (−1.4%) | 943 (−0.9%) | 913 (−0.6%) | 900 (−0.5%) |
| Human | A | 820 (−2.9%) | 797 (−2.3%) | 786 (−2.0%) | 938 (−1.3%) | 912 (−0.8%) | 901 (−0.4%) |
| Troll | H | 828 (−2.0%) | 803 (−1.6%) | 792 (−1.3%) | 938 (−1.4%) | 909 (−1.0%) | 899 (−0.5%) |
| Windshaper | H | 824 (−2.5%) | 800 (−1.9%) | 789 (−1.6%) | 929 (−2.3%) | 903 (−1.7%) | 895 (−1.0%) |
| High Order | A | 824 (−2.5%) | 800 (−1.9%) | 789 (−1.6%) | 929 (−2.3%) | 903 (−1.7%) | 895 (−1.0%) |
| Tauren | H | 821 (−2.8%) | 798 (−2.2%) | 787 (−1.8%) | 925 (−2.7%) | 899 (−2.2%) | 888 (−1.8%) |
| Dwarf | A | 818 (−3.1%) | 795 (−2.6%) | 785 (−2.2%) | 923 (−3.0%) | 896 (−2.4%) | 886 (−2.1%) |

#### Marksmanship Hunter

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Night Elf | A | **796** (best) | **772** (best) | **759** (best) | **910** (best) | **883** (best) | **869** (best) |
| Orc | H | 779 (−2.2%) | 758 (−1.8%) | 747 (−1.6%) | 901 (−1.0%) | 877 (−0.7%) | 865 (−0.5%) |
| Human | A | 769 (−3.3%) | 752 (−2.7%) | 742 (−2.2%) | 895 (−1.6%) | 875 (−0.9%) | 865 (−0.5%) |
| Troll | H | 778 (−2.3%) | 759 (−1.8%) | 748 (−1.5%) | 895 (−1.7%) | 874 (−1.0%) | 861 (−1.0%) |
| Windshaper | H | 773 (−2.8%) | 756 (−2.1%) | 746 (−1.8%) | 887 (−2.5%) | 868 (−1.8%) | 857 (−1.5%) |
| High Order | A | 773 (−2.8%) | 756 (−2.1%) | 746 (−1.8%) | 887 (−2.5%) | 868 (−1.8%) | 857 (−1.5%) |
| Tauren | H | 770 (−3.2%) | 753 (−2.5%) | 743 (−2.1%) | 882 (−3.1%) | 861 (−2.5%) | 852 (−2.0%) |
| Dwarf | A | 767 (−3.6%) | 750 (−2.9%) | 740 (−2.5%) | 879 (−3.4%) | 859 (−2.8%) | 849 (−2.4%) |

#### Survival Hunter

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Night Elf | A | **725** (best) | **704** (best) | **695** (best) | **852** (best) | **829** (best) | **818** (best) |
| Orc | H | 709 (−2.2%) | 692 (−1.8%) | 684 (−1.5%) | 846 (−0.7%) | 825 (−0.5%) | 815 (−0.3%) ≈ |
| Human | A | 711 (−1.9%) | 697 (−1.0%) | 691 (−0.5%) | 841 (−1.3%) | 824 (−0.6%) | 817 (−0.1%) ≈ |
| Troll | H | 708 (−2.3%) | 692 (−1.7%) | 684 (−1.5%) | 841 (−1.3%) | 821 (−0.9%) | 811 (−0.8%) |
| Windshaper | H | 701 (−3.4%) | 687 (−2.4%) | 681 (−2.0%) | 832 (−2.3%) | 817 (−1.5%) | 809 (−1.0%) |
| High Order | A | 701 (−3.4%) | 687 (−2.4%) | 681 (−2.0%) | 832 (−2.3%) | 817 (−1.5%) | 809 (−1.0%) |
| Tauren | H | 699 (−3.6%) | 685 (−2.8%) | 679 (−2.2%) | 824 (−3.2%) | 808 (−2.5%) | 801 (−2.1%) |
| Dwarf | A | 695 (−4.1%) | 681 (−3.3%) | 676 (−2.7%) | 820 (−3.7%) | 804 (−3.0%) | 797 (−2.6%) |

### Mage

#### Arcane Mage

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Undead | H | **615** (best) | **605** (best) | **600** (best) | **756** (best) | **742** (best) | **735** (best) |
| Orc | H | 609 (−1.0%) | 597 (−1.4%) | 589 (−1.8%) | 754 (−0.3%) ≈ | 737 (−0.7%) | 726 (−1.1%) |
| Gnome | A | 611 (−0.7%) | 598 (−1.1%) | 591 (−1.5%) | 753 (−0.3%) ≈ | 737 (−0.7%) | 727 (−1.1%) |
| Troll | H | 604 (−1.8%) | 593 (−2.0%) | 586 (−2.3%) | 745 (−1.4%) | 730 (−1.6%) | 721 (−1.9%) |
| High Order | A | 602 (−2.1%) | 592 (−2.2%) | 586 (−2.2%) | 742 (−1.8%) | 729 (−1.9%) | 721 (−1.8%) |
| Human | A | 610 (−0.9%) | 600 (−0.9%) | 593 (−1.1%) | 740 (−2.1%) | 727 (−2.1%) | 718 (−2.2%) |

#### Fire Mage

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Orc | H | **754** (best) | 737 (−0.2%) ≈ | 743 (−0.5%) | **920** (best) | **904** (best) | 914 (−0.1%) ≈ |
| Undead | H | 754 (−0.0%) ≈ | **739** (best) | **747** (best) | 916 (−0.4%) ≈ | 901 (−0.2%) ≈ | **915** (best) |
| High Order | A | 744 (−1.3%) | 736 (−0.5%) ≈ | 741 (−0.8%) | 906 (−1.6%) | 899 (−0.5%) ≈ | 907 (−0.8%) |
| Human | A | 744 (−1.3%) | 730 (−1.2%) | 738 (−1.3%) | 904 (−1.7%) | 891 (−1.4%) | 901 (−1.5%) |
| Gnome | A | 750 (−0.6%) | 729 (−1.4%) | 738 (−1.3%) | 907 (−1.5%) | 890 (−1.5%) | 898 (−1.8%) |
| Troll | H | 743 (−1.5%) | 729 (−1.3%) | 737 (−1.3%) | 900 (−2.2%) | 888 (−1.7%) | 897 (−1.9%) |

#### Frost Mage

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Troll | H | **554** (best) | 559 (−0.1%) ≈ | 563 (−0.2%) ≈ | **681** (best) | **686** (best) | 690 (−0.1%) ≈ |
| Undead | H | 550 (−0.8%) | **559** (best) | 564 (−0.0%) ≈ | 676 (−0.7%) | 686 (−0.0%) ≈ | **691** (best) |
| Gnome | A | 550 (−0.7%) | 556 (−0.5%) | 561 (−0.5%) | 677 (−0.6%) | 684 (−0.4%) ≈ | 688 (−0.3%) ≈ |
| Orc | H | 550 (−0.9%) | 556 (−0.7%) | 560 (−0.8%) | 677 (−0.6%) | 683 (−0.4%) | 687 (−0.5%) |
| High Order | A | 547 (−1.4%) | 555 (−0.8%) | 561 (−0.6%) | 673 (−1.3%) | 681 (−0.7%) | 688 (−0.4%) |
| Human | A | 551 (−0.6%) | 559 (−0.1%) ≈ | **564** (best) | 668 (−1.9%) | 676 (−1.4%) | 682 (−1.3%) |

### Warlock

#### Affliction Warlock

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Gnome | A | 645 (−0.2%) ≈ | **651** (best) | **658** (best) | 819 (−0.2%) ≈ | **828** (best) | **841** (best) |
| Orc | H | 645 (−0.2%) ≈ | 641 (−1.7%) | 646 (−1.8%) | **821** (best) | 821 (−0.8%) | 828 (−1.5%) |
| Undead | H | 644 (−0.4%) | 642 (−1.4%) | 648 (−1.6%) | 816 (−0.6%) | 821 (−0.9%) | 826 (−1.7%) |
| Human | A | **647** (best) | 645 (−1.0%) | 651 (−1.1%) | 805 (−1.9%) | 811 (−2.1%) | 817 (−2.9%) |
| Troll | H | 644 (−0.4%) | 634 (−2.7%) | 641 (−2.6%) | 819 (−0.2%) ≈ | 809 (−2.3%) | 821 (−2.3%) |

#### DS/Ruin Warlock

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Orc | H | 584 (−0.3%) ≈ | 591 (−0.7%) | 604 (−1.4%) | 770 (−0.4%) ≈ | **779** (best) | 800 (−1.4%) |
| Undead | H | 585 (−0.2%) ≈ | 595 (−0.0%) ≈ | 607 (−0.9%) | 764 (−1.1%) | 779 (−0.0%) ≈ | 798 (−1.6%) |
| Gnome | A | 585 (−0.2%) ≈ | 592 (−0.5%) | **613** (best) | 768 (−0.6%) | 778 (−0.1%) ≈ | **811** (best) |
| Troll | H | **586** (best) | 588 (−1.2%) | 595 (−2.9%) | **773** (best) | 776 (−0.4%) | 788 (−2.8%) |
| Human | A | 585 (−0.1%) ≈ | **595** (best) | 608 (−0.8%) | 753 (−2.6%) | 766 (−1.6%) | 786 (−3.1%) |

#### Demonic Pact Warlock

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Undead | H | **624** (best) | **640** (best) | 671 (−0.7%) | 780 (−0.3%) ≈ | **802** (best) | 842 (−0.5%) |
| Orc | H | 623 (−0.2%) ≈ | 635 (−0.7%) | 671 (−0.7%) | **783** (best) | 800 (−0.3%) ≈ | 845 (−0.2%) ≈ |
| Gnome | A | 621 (−0.4%) | 635 (−0.8%) | **676** (best) | 780 (−0.3%) | 798 (−0.5%) | **847** (best) |
| Troll | H | 611 (−1.9%) | 627 (−2.0%) | 660 (−2.3%) | 769 (−1.8%) | 789 (−1.6%) | 830 (−2.0%) |
| Human | A | 622 (−0.3%) ≈ | 638 (−0.2%) ≈ | 675 (−0.1%) ≈ | 767 (−2.1%) | 788 (−1.7%) | 832 (−1.7%) |

#### Destruction Warlock

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Undead | H | **669** (best) | **662** (best) | **661** (best) | **810** (best) | **807** (best) | 799 (−0.3%) |
| Gnome | A | 665 (−0.6%) | 661 (−0.1%) ≈ | 660 (−0.2%) ≈ | 808 (−0.3%) | 802 (−0.6%) | **802** (best) |
| Orc | H | 665 (−0.6%) | 655 (−1.0%) | 657 (−0.6%) | 802 (−0.9%) | 796 (−1.3%) | 791 (−1.4%) |
| Human | A | 656 (−1.9%) | 649 (−1.9%) | 650 (−1.7%) | 797 (−1.6%) | 793 (−1.7%) | 785 (−2.1%) |
| Troll | H | 636 (−4.9%) | 636 (−3.8%) | 647 (−2.1%) | 772 (−4.7%) | 772 (−4.3%) | 787 (−1.9%) |

### Priest

#### Shadow Priest

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Night Elf | A | **653** (best) | **631** (best) | 645 (−0.2%) | **780** (best) | **754** (best) | 770 (−0.1%) ≈ |
| Gnome | A | 651 (−0.4%) | 629 (−0.3%) | 643 (−0.4%) | 780 (−0.1%) ≈ | 753 (−0.1%) ≈ | 770 (−0.2%) |
| Undead | H | 648 (−0.8%) | 629 (−0.3%) | **646** (best) | 775 (−0.7%) | 752 (−0.3%) | **771** (best) |
| Human | A | 637 (−2.5%) | 619 (−2.0%) | 635 (−1.7%) | 763 (−2.2%) | 741 (−1.7%) | 760 (−1.5%) |
| Dwarf | A | 642 (−1.7%) | 624 (−1.1%) | 640 (−0.9%) | 763 (−2.2%) | 741 (−1.7%) | 760 (−1.5%) |
| Troll | H | 635 (−2.8%) | 617 (−2.2%) | 634 (−1.9%) | 761 (−2.5%) | 739 (−2.0%) | 758 (−1.7%) |

#### Smite Priest

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Night Elf | A | **536** (best) | **523** (best) | **515** (best) | **672** (best) | **655** (best) | **645** (best) |
| Gnome | A | 534 (−0.2%) | 522 (−0.2%) | 514 (−0.1%) ≈ | 671 (−0.1%) ≈ | 655 (−0.1%) ≈ | 645 (−0.1%) ≈ |
| Human | A | 527 (−1.7%) | 516 (−1.3%) | 509 (−1.0%) | 661 (−1.6%) | 647 (−1.2%) | 639 (−1.0%) |
| Dwarf | A | 529 (−1.2%) | 518 (−0.9%) | 511 (−0.6%) | 661 (−1.6%) | 647 (−1.2%) | 638 (−1.0%) |
| Troll | H | 527 (−1.6%) | 516 (−1.2%) | 510 (−1.0%) | 661 (−1.6%) | 647 (−1.3%) | 638 (−1.0%) |
| Undead | H | 533 (−0.4%) | 509 (−2.6%) | 505 (−1.8%) | 669 (−0.5%) | 637 (−2.8%) | 632 (−2.0%) |

### Shaman

#### Enhancement Shaman

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Orc | H | **654** (best) | **636** (best) | **625** (best) | **777** (best) | **758** (best) | **745** (best) |
| Dwarf | A | 636 (−2.8%) | 620 (−2.4%) | 612 (−2.1%) | 772 (−0.7%) | 754 (−0.5%) | 743 (−0.3%) ≈ |
| Tauren | H | 639 (−2.3%) | 623 (−1.9%) | 615 (−1.6%) | 766 (−1.4%) | 749 (−1.2%) | 740 (−0.7%) |
| Windshaper | H | 639 (−2.3%) | 624 (−1.9%) | 615 (−1.6%) | 769 (−1.0%) | 748 (−1.2%) | 738 (−0.9%) |
| Troll | H | 645 (−1.4%) | 626 (−1.4%) | 617 (−1.2%) | 763 (−1.8%) | 744 (−1.9%) | 734 (−1.6%) |

#### Elemental Shaman

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Orc | H | 430 (−0.1%) ≈ | **428** (best) | **429** (best) | **543** (best) | **535** (best) | **537** (best) |
| Troll | H | **431** (best) | 424 (−0.8%) | 427 (−0.6%) | 539 (−0.8%) | 531 (−0.7%) | 533 (−0.7%) |
| Tauren | H | 426 (−1.1%) | 426 (−0.5%) | 428 (−0.2%) | 536 (−1.2%) | 531 (−0.7%) | 535 (−0.4%) |
| Dwarf | A | 426 (−1.1%) | 426 (−0.5%) | 428 (−0.3%) | 532 (−1.9%) | 527 (−1.5%) | 530 (−1.1%) |
| Windshaper | H | 422 (−1.9%) | 422 (−1.5%) | 427 (−0.6%) | 532 (−2.1%) | 526 (−1.7%) | 530 (−1.2%) |

#### Stormcaller Shaman

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Orc | H | **450** (best) | **445** (best) | **447** (best) | **562** (best) | **556** (best) | **556** (best) |
| Tauren | H | 446 (−1.1%) | 442 (−0.6%) | 445 (−0.3%) | 555 (−1.2%) | 551 (−0.8%) | 554 (−0.5%) |
| Troll | H | 447 (−0.8%) | 440 (−1.1%) | 443 (−0.8%) | 558 (−0.8%) | 549 (−1.1%) | 551 (−0.8%) |
| Dwarf | A | 446 (−1.0%) | 442 (−0.6%) | 446 (−0.3%) | 551 (−1.9%) | 548 (−1.4%) | 550 (−1.1%) |
| Windshaper | H | 442 (−1.9%) | 438 (−1.5%) | 443 (−0.7%) | 550 (−2.2%) | 546 (−1.7%) | 553 (−0.6%) |

### Druid

#### Balance Druid

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Night Elf | A | **457** (best) | **455** (best) | **456** (best) | **585** (best) | **594** (best) | **593** (best) |
| Tauren | H | 448 (−2.0%) | 448 (−1.5%) | 451 (−1.1%) | 575 (−1.7%) | 588 (−1.1%) | 588 (−0.7%) |
| Windshaper | H | 447 (−2.4%) | 448 (−1.4%) | 451 (−1.3%) | 573 (−2.1%) | 587 (−1.3%) | 587 (−1.0%) |
| High Order | A | 447 (−2.4%) | 448 (−1.4%) | 451 (−1.3%) | 573 (−2.1%) | 587 (−1.3%) | 587 (−1.0%) |

#### Feral Druid

| Race | Side | 45 s, same gear | 60 s, same gear | 75 s, same gear | 45 s, per-race gear | 60 s, per-race gear | 75 s, per-race gear |
|---|---|---:|---:|---:|---:|---:|---:|
| Night Elf | A | **614** (best) | **593** (best) | **571** (best) | **681** (best) | **661** (best) | **638** (best) |
| Tauren | H | 608 (−1.0%) | 589 (−0.7%) | 569 (−0.5%) | 672 (−1.3%) | 655 (−0.9%) | 634 (−0.7%) |
| Windshaper | H | 601 (−2.1%) | 587 (−1.1%) | 565 (−1.1%) | 665 (−2.3%) | 652 (−1.3%) | 630 (−1.3%) |
| High Order | A | 601 (−2.1%) | 587 (−1.1%) | 565 (−1.1%) | 665 (−2.3%) | 652 (−1.3%) | 630 (−1.3%) |


## Reproducing this

From the repository root, with Go (1.23 or newer) and the repository checked out, for each duration D in 45, 60 and 75:

```sh
go build -buildvcs=false -tags with_db -o forever-bench ./tools/forever_bench
./forever-bench -duration D -iterations 5000 -seed 20291951 -output sameD
./forever-bench -duration D -iterations 5000 -seed 20291951 -baseline-results artifacts/forever_dps_5min.json -output optD
```

The second command replays the fork's saved per-race loadouts (found for a 5-minute fight). Replaying them at 5 minutes reproduced the committed results exactly (0.000% difference across all 147 rows).

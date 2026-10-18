TOWER SURVIVOR — MOBILE ARMORY UPDATE

Upload index.html, manifest.json, and sw.js to the ROOT of your GitHub repository, replacing the previous versions, then publish via Settings > Pages > Deploy from a branch > main > /(root).

Latest changes:
- Compact app-style layout designed to fit on a phone screen without page scrolling.
- Four tower cards arranged left-to-right; four support cards directly below, also left-to-right.
- Tower and support purchase cards share consistent sizing. Purchased offer tiles become empty until the next reroll or refresh.
- Unique styled tower emblems; icon colors correspond to the primary damage type, with elemental accent colors.
- Tower cards display Damage, Damage Type, Attack Type, Range, and Ability.
- Rare support upgrades are weighted less frequently, especially during the first five rounds until income has increased.
- Base income remains 50 gold per second, paid in 2-second increments.
- Purchase costs are deducted from gold; purchases trigger a small gold-colored “$ Upgrade Name $” toast.
- A progress bar and countdown show the next shop refresh.
- Removed the reroll-discount support upgrade.

Existing rules retained:
- Start with 5,000 gold.
- Rarity costs: Common 500, Uncommon 2,000, Rare 5,000, Epic 10,000 gold.
- Epic towers are unavailable before level 6 (after round 5) and at most one Epic tower can appear per tower offer refresh.
- Manual rerolls cost gold after free rerolls are used; their timer is at least 15 seconds or the time remaining to the scheduled refresh, whichever is greater.
- No range-increase upgrades.
- Island map and medieval stone keep remain.

To update an existing iPhone home-screen install, upload/commit all three files, wait for GitHub Pages to deploy, then close and reopen the game. The service worker cache version was incremented to encourage the new build to load.

Latest small-layout and reroll update:
- Reduced card padding, icon size, and text size for more compact tower/support tiles.
- Removed the 'Tower options' and 'Support options' labels while keeping each reroll button.
- Free rerolls are available only before the first purchase. Any unspent free rerolls expire when the first tower or support is bought.
- After the first purchase, each reroll costs gold and increases by 100 gold per paid reroll (100g, 200g, 300g, etc.), capped at 1,000g.
- Service worker cache version incremented to v5 to help refresh the installed game.


Damage and Income trackers (v6): Damage is the sum of owned towers' damage per hit, with global damage and expected critical bonuses, divided by 1,000. Income is passive gold per second (base + income upgrades + compounding income), plus average extra bounty gold earned per second, divided by 100. The trackers are normalized scores intended to compare investment direction, not DPS or total lifetime earnings.


Creep rewards and variety update (v7):
- Fixed kill gold so normal creeps continue paying after the one-time Clear is used.
- Regular creeps award at least 100 gold at round 1; reward scales by round, creep type, and bounty percentage.
- Manual Clear awards the same kill rewards; emergency Clear removes creeps without rewards, but future kills still pay normally.
- Every round has a rotating three-unit roster: a light unit, a medium-armored unit, and a heavy-armored unit. Spawn mix is about 70% light, 22% medium, and 8% heavy, creating many small creeps with occasional tougher enemies.
- Creep archetypes have different health, movement speed, attack damage, bounty, silhouette, and armor type. Piercing, Siege, Magic, Spikes, and Chaos attacks interact differently with armor.
- Income tracker now includes actual average gold earned from kills and the boss reward.


Layout and tower rarity balance update (v8):
- Supply Armory is constrained to about one-third of the screen, giving the island/creep play area more room.
- Removed the Repair button. The bottom controls are Speed, Clear, and Pause, with Clear centered and Pause beside the speed control.
- Tower base hit damage scales by rarity: Common 1.0×, Uncommon 1.5×, Rare 2.25×, Epic 3.375× (each rarity tier is 50% higher than the previous tier for a comparable tower). The displayed damage reflects the rarity multiplier.
- Service worker cache incremented to v8.

Latest visual update:
- Supply Armory no longer shows a title or explanatory subtitle. Its compact top strip contains only the refresh countdown/bar and separate tower/support reroll buttons; the two four-card rows fill the remaining armory height.
- Creeps now render as small illustrated canvas sprites rather than simple colored geometric markers: footmen, scouts, rangers, warlocks, shieldbearers, ogre brutes, and a distinct boss. Armor outlines, health bars, and elemental status rings remain visible.
- Purchase notifications now appear over the playfield just above the central keep instead of at the top edge of the screen.
- Service-worker cache version bumped to v9.

2026-10-16 SHOP + SUPPORT UPDATE
Tap anywhere on a tower/support card to purchase; no Buy button or rarity text. Thick rarity borders; Tower and Support reroll labels. Seven new supports: Vitality Growth (+1000 HP and +10 max HP/s), Growing Treasury (+10 gold/s and +1 gold/s every 10s), Royal Bounty (+200% bounty and +100% current passive income), Prosperity Pact (+100% bounty and +50% current passive income), Arcane Reservoir (+2000 shield and +10 max shield/s), Aegis Barrier (+2000 shield and 25% multiplicative incoming damage reduction), Titanic Vitality (+2000 HP and +50 max HP/s). Passive income starts at 50 gold/s. Damage counter = sum of owned tower hit damage x (1+damage bonus) x (1+critical chance), divided by 1000. Income counter = (passive gold/s + lifetime kill gold / elapsed seconds) divided by 100.

Mana shield update:
- Shield meter is hidden until max shield becomes positive; then stays visible even at zero.
- Shield regenerates at 5% of maximum capacity per second, plus flat regeneration bonuses.
- Aegis Barrier grants 25% damage reduction only when shield is positive at the moment of an attack; this reduction ends at zero shield.
- Arcane Renewal (Uncommon): +2,000 maximum/current shield and +50 shield regeneration per second.
- Arcane Siphon Barrage (Uncommon Magic): +10 maximum shield per enemy struck by its barrage. This increases capacity, not current shield; passive regeneration fills it.

Max HP and mana shield capacity increases now grant the same amount of current HP or shield, including ongoing per-second growth and Arcane Siphon Barrage hits. This preserves the absolute deficit rather than introducing a percentage loss due to capacity growth.


RANGE / TOWER BALANCE UPDATE
- Tower range tiers: 300, 600, 900, and 1200. Range 1200 maps to roughly 260 canvas pixels, approximately the grassy island edge from the central keep.
- Close range receives higher damage AND attack speed: 300 = 2.30x base hit and 1.65x base speed; 600 = 1.65x hit and 1.30x speed; 900 = 1.22x hit and 1.12x speed; 1200 = 1.00x hit and speed. Existing rarity multipliers (1x, 1.5x, 2.25x, 3.375x) still stack.
- Range-300 Area towers hit all nearby enemies around the keep. Range-300 Single Target, Splash, and Bounce towers additionally fire a 0.8x-damage spell at a distant enemy within range 900 every 3 seconds.
- Tower cards get 4/7 of shop height; support cards get 3/7. Shortened tower stat labels.


BALANCE UPDATE:
- Damage and Income counters share one stats block, including when mana shield appears.
- Creeps stop at the keep and attack repeatedly until killed or game ends.
- Common Mana Shield provides +1,000 maximum and current shield.
- Support Rare weights reduced to 1.45 from up to 2.6; economy support weights multiplied by 0.48.
- New damage supports: Common +5% all, Common +10% each primary type, Uncommon +10% all, Rare +25% each primary type, Epic +50% all. Type-specific and universal damage bonuses combine multiplicatively.

UI update: Damage and Income labels and values are centered within their respective halves of the combined stats block.

WALLS, RANGED CREEPS & RESERVED SHIELD SLOT (v14)
- Mana Shield stat slot is always reserved but invisible until shield capacity is acquired; the other stats do not move.
- Enemies stop outside the keep walls (49 canvas units plus unit radius) and remain there attacking until killed or the game ends.
- Rangers attack from 100-200 world range; Warlocks from 200-300 world range. Other units and the boss are melee.
- Enemies are rendered in front of the keep, with attack glints and ranged projectile streaks, plus extra stone and armor detailing.

Visual combat update: fixed castle-mounted color-coded turrets replace orbiting attachments; splash/area rings, bounce chains, elemental creep glows/particles, and floating gold rewards for kills (including manual Clear).

Bounty balance update: All creep kill payouts, including manual Clear rewards, are reduced by 50% via creepGold(). The fixed 1,500 gold boss victory bonus remains unchanged. Passive gold income and shop prices are unchanged.

WC3-INSPIRED VISUAL UPDATE (v17): Richer grass/stone terrain, blue-roofed castle, corner towers, heraldic banner, torches, varied mounted weapon silhouettes and improved creep armor/weapon details. Procedural original browser art inspired by the genre, not extracted Warcraft III copyrighted assets. Purchase notification moved higher in playfield (27.5% from top). Creep bounty reduced by a further 25% from prior 50%-reduced level (now 37.5% of original); passive income and fixed boss bonus unchanged.


OWNED TOWER INVENTORY / CREEP HP (v18)
- All regular creep and boss starting/max HP values are increased by 25%. Damage, armor, speed and gold rewards are unchanged.
- A translucent castle icon at the top-right of the battlefield displays the number of distinct owned tower types.
- Tap the icon to toggle a pinned list; touch and hold for 350 ms to show it temporarily, releasing to close.
- List updates after each tower purchase or level upgrade. Towers are grouped by range (1200, 900, 600, 300).
- Each entry shows its icon, name, level, damage type, attack pattern, damage and special ability.
- The inventory is a scrollable overlay over the battlefield and does not resize or move the gameplay/shop layout.


Rarity/range and Spikes rework (v19):
- Common towers: only single-target, 600 or 900 range, lowest damage scaling.
- Uncommon, Rare and Epic non-Spikes towers: 300/600/900/1200 range; close-range gains modest DPS advantage.
- Spikes towers: no range or projectile. Each owned Spikes tower reflects damage to a creep whenever its attack causes HP loss; a shield-only hit does not trigger retaliation. Shield-breaking overflow that damages HP does trigger retaliation. Normal damage bonuses and Spikes-specific damage bonuses apply.
- Vital Siphon Barrage: Uncommon Magic Barrage, 600 range, 114 base damage, 3.12 attacks/s, +10 maximum and current HP per enemy hit, including lethal hits.
- Arcane Siphon Barrage retains the same stats and grants +10 maximum and current shield per hit, including lethal hits.

SIPHON & LEECH UPDATE (v20)
- Arcane Siphon Barrage and Vital Siphon Barrage now have 900 range; other combat stats unchanged.
- Arcane Leech: Rare Magic, 1200 range, single-target, 300 base damage, 0.8 attacks/sec. Restores mana shield by 30% of actual enemy HP damage dealt, capped at max shield. Does nothing to shield before a shield upgrade unlocks capacity.
- Chaos Leech: Rare Chaos, 1200 range, single-target, 300 base damage, 0.8 attacks/sec. Restores tower HP by 30% of actual enemy HP damage dealt, capped at max HP.
- Leech restores current HP/shield only; it does not increase max capacity. Damage includes armor interactions and purchased damage upgrades; overkill is excluded.

BOUNCE & MANA SIPHON UPDATE (v21)
- Bounce chains hit up to five unique enemies total (initial hit plus four bounces). Each successive target must be within 300 displayed range of the previous target; no map-wide jumps.
- Arcane Siphon Barrage renamed Mana Siphon Barrage. It always deals normal attack damage, but gains maximum/current mana shield from hits only after shield capacity has been unlocked by a support purchase.
- Existing AoE radii: Splash 48 canvas-world units (~222 displayed range); Area 55 (~254); 300-range Area towers pulse around castle in a 300 displayed-range radius.


AoE rebalance (v22): Splash hits a 300 displayed-range-unit DIAMETER (150 radius) around the impact, dealing 70% hit damage to each target. Area attacks cover a 600 displayed-range-unit RADIUS (1200 diameter) around the impact, or around the castle for 300-range Area towers; that is approximately one-quarter the surface area of a circular island with 1200-unit radius. Area deals 25% hit damage to each affected target (before armor and modifiers). Area towers can apply Frost, Fire or Poison to every enemy hit. Magic Area and Siege Area were assigned Poison; other existing elemental Area towers retain their effects. A tower's firing range still determines whether it can initiate an attack.


RANGE BALANCE UPDATE (v23)
- Area towers may target at 600 or 900 displayed range only; their damage AoE stays 1200 diameter (600 radius), with 25% hit damage per affected creep.
- Splash towers have 300/600/900 attack range only; their damage AoE stays 300 diameter (150 radius), with 70% hit damage per affected creep.
- Commons remain single-target at 600 or 900; Spikes reflect HP-damaging attacks without a range.
- Existing short-range DPS adjustment is applied using the actual assigned range after restrictions.


DPS BALANCE PASS (v24, October 17, 2026)
- Both Siphon Barrages now gain +7 max AND current HP/shield per qualifying hit (30% less than +10). Mana Siphon still deals damage without shield, but only harvests shield when unlocked.
- Common towers: ~70 unmodified single-target raw DPS, adjusted for attack speed, with 600/900 ranges.
- Epic towers: targeted ~420 effective DPS at 900 range, with a range bonus at 300/600 and penalty at 1200, modified for type and elemental utility.
- For multihit damage balance, approximate expected targets per shot: Splash 1.55, Bounce 2.15 (chain cap 5), Barrage 2.15, Area 3.8. Splash damage multiplier is 70%; Barrage 62%; Area 25%; Bounce successive hits 72% of previous. These are design assumptions, not measured in-game averages.
- Elemental slow/DoT and favorable armor matchups reduce raw damage budget modestly; DoT remains flat 11 Fire or 18 Poison HP/s in the combat engine, so its relative power changes across rounds.
- Spikes have no range or attack speed. Per qualifying HP-damaging enemy hit: Common 14, Uncommon 24, Rare 43, Epic 80 base reflected damage before damage bonuses and armor. Reflections do not trigger when mana shield fully absorbs an attack.
- Other rarities receive a smooth damage curve between Common and Epic; special Leech and Siphon towers retain their bespoke attack damage stats.
- Real balance depends on spawn density, crowding at the keep, survivability, and actual hit counts; values should be playtested.

Starting castle health: 2,500 / 2,500 HP (changed from 10,000).


V26: CHAOS / MAGIC SIPHON, UI AND DIFFICULTY
- Vital Siphon Barrage is now Chaos type (HP growth); Mana Siphon Barrage stays Magic (mana shield growth). Chaos Leech remains Chaos.
- Gold purchase notification has no box or border; translucent coin-gold letters float upward and fade within 0.85 seconds.
- Damage and Income tracker display values are multiplied by 10. Underlying damage and gold income are NOT changed by the tracker display adjustment.
- New wave scaling: base HP before creep-type multiplier and existing 1.25 HP factor is 175 at level 1, 250 at level 2, 295 at level 3, and 295*1.12^(level-3) afterward. Boss HP unchanged.
- Spawn interval: max(0.48, 1.28-0.085*(level-1)) seconds. Creep roles/armor/multipliers, rewards, and creep attack damage unchanged.
- Intended early wave balance: a single Uncommon will leak, Uncommon+Common or ~3 Commons can control level 1; 2 Commons+Uncommon or ~4 Commons for level 2; a single Rare is powerful but begins leaking near level 3. These are targets, not proven guarantees: target availability, range, damage type and luck vary.
- Levels 4-30 increase both spawn density and HP. Area/Bounce/Splash effectiveness grows with crowding, while single target remains useful against heavier creeps.

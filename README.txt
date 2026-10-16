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

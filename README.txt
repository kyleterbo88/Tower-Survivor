Tower Survivor v132 — GitHub Pages deployment
Upload index.html, sw.js, manifest.json, README.txt to your published branch.
Approved sounds are embedded directly into index.html and work offline.
Menu Open: Menu_Select_00; Menu Close: Inventory_Open_00; Purchase: Pickup_Gold_00.
Master and Interface volume settings in Menu; quick mute near Menu button.
Original source WAVs are not redistributed in this update ZIP.
Source license and rights should be verified before public commercial release.

Tower Survivor v131 — result panel controls and critical tracker display

Extract index.html, sw.js, manifest.json and README.txt to the root of the GitHub Pages repository.

v131: small top-right × dismiss on VICTORY/DEFEATED, direct Restart button, and a note about inspecting the battlefield before restarting through Menu. Critical Hit bonus is displayed as a simple percentage like Attack Speed. No combat or economy changes.

Tower Survivor v130
Deploy index.html, sw.js, manifest.json, and README.txt to GitHub Pages repository root.

v130: Critical Hit Chance purchased/effective display in Owned Towers; Mana Shield Damage Reduction purchased/effective display in Castle Status. No combat changes.

v128 — End-of-run battlefield banners and unlimited stackable Ankhs. Restart via Menu. No balance changes.

v126 — Tower ability descriptions audited against combat logic. Iron Thorns now shows Block 10 damage; missing special mechanics and incorrect stun duration corrected. No combat changes.

v126: Offline, expandable Patch Notes menu with available v31–v126 history. Verified Dread Knight announcement is DREAD KNIGHT APPROACHES. No balance changes.

v124: Owned Towers groups sort by combined effective damage (descending) within each damage type, refreshed on menu open. Floating castle bars are translucent, rounded and match HUD HP/Mana fill colors. No balance changes.

v124 — How to Play now explains the clickable Central Castle, Owned Towers icon, Income HUD, and Menu, listing the information each opens. Detailed game rules remain in Game Mechanics. No balance changes.

v121 — Single Target ability labels now depend only on rarity: Common Direct Hit, Uncommon Focused Hit, Rare Heavy Hit, Epic Devastating Hit. Applies to every damage type, including Chaos. No combat balance changes.

v120 — Tower description clarity: Area 25% is damage per target, not hit chance or a secondary effect. Area deals an additional 30% of that applied damage over 2 seconds. Splash 70%, Barrage 62%, Bounce 72% decay. Primary → secondary → special. Frost now lists exact slow mechanics; names identify elemental effects; compact tower tiles. No combat balance changes.

v120 — Consistent tower ability wording: use imperative verbs Reflect, Block, Heal, Apply, Stun, Restore, Damage, Chain and Cast across Spikes and other towers. No combat changes.

Tower Survivor v118 — HUD center alignment and consistent Spikes descriptions.
HUD labels and values are centered in their boxes; Owned Towers count centered below title; Spikes descriptions use current base reflect damage after damage upgrades, with concise blocks and unique effects. No combat balance changes.

Tower Survivor v117 — Hotfix: automatic refresh could freeze game simulation.
Fixed undefined dt reference inside refreshAll(), which raised ReferenceError when an automatic 30-second refresh occurred. Removed unrelated announcement decay and castle-panel rendering from refreshAll; both are already handled in update(dt). No gameplay balance changes.

Tower Survivor v116 — Ankh description and mechanics documentation
- Shortened Ankh item and badge description by removing emergency Clear sentence.
- Game Mechanics explicitly documents Ankh activation before automatic emergency Clear.
- No gameplay mechanics changed.

Tower Survivor v115 — HUD and popup polish
- Magic damage-type color adjusted to a more purple lavender (#B59BFF). Rarity colors unchanged.
- Ankh of Resurrection descriptions shorten “maximum” to “max” and “triple” to “3X”.
- Owned Towers attack-speed and critical-hit badges slightly smaller.
- Owned Towers title enlarged and emphasized.
- Gold HUD number enlarged and given more visual emphasis while keeping within its stat tile.
- No gameplay balance changes.

Tower Survivor v114: Castle combat telemetry — landed attacks, evaded attacks, total incoming damage, damage prevented by armor/evasion/thorn flat block/shield barrier, damage absorbed by Mana Shield, and damage reaching castle HP. Statistics reset each run. Shield absorption counted once; reflected damage remains tower damage.

Tower Survivor v113

- First-time-per-run new creep spawn announcements: Cultist, Berserker, Necromancer, Dread Knight.
- White bold 86%-opacity text with dark shadow, floating toward the side the enemy spawned; 2.2 seconds. Triggered on actual spawn.
- Every Hero miniboss and the final boss trigger their own announcement.
- Tap the central castle to view Armor, damage reduction, Evasion, HP regeneration, current/max HP, Mana Shield and Shield regeneration.
- Toggle extra green HP and blue Mana Shield percentage meters above the castle. Original UI meters remain unchanged.
- Toggle state retained on a new run within the same page session. Default OFF.
- No creep, tower, economy or armor balance changes.

Tower Survivor v112 — Progressive creep roster expansion

Four new creeps: Cultist (Unarmored, level 5+), Berserker (Medium, level 5+), Necromancer (Unarmored ranged, level 10+), Dread Knight (Heavy, level 15+).
All new creeps have substantial HP rather than being glass cannons. Armor counters, movement, range and frequency distinguish them.
New-variant share within its armor category: levels 1–4 0%, 5–9 6%, 10–14 14%, 15–19 25%, 20–24 38%, 25–30 50%.
When an armor category has two unlocked new variants, its new-variant share is split evenly. Armor category distribution remains 20/40/30/10.
Level Details lists every possible creep this level, actual scaled HP and exact spawn probability per creep.
Miniboss HP is 115% of the highest-HP regular creep eligible in that level, including new variants.
No tower damage, armor matchup, shop, or economy changes.

Tower Survivor v111 — Five armor types and Hero minibosses

Damage matchup multipliers updated to approved 75%–125% table. Chaos is 85% vs Unarmored and 125% vs Hero.
Existing creep armor reassigned: Warlock Unarmored, Scout/Ranger Light, Footman Medium, Shieldbearer/Ogre Brute Heavy. No new regular creep models added yet.
Regular spawn weights: 20% Unarmored / 40% Light / 30% Medium / 10% Heavy.
One Hero-armored miniboss at midpoint of levels 5, 10, 15, 20 and 25; HP = 115% of the highest-HP regular creep selected for the level. Level 30 final boss uses Hero armor.
Level Details shows all five armor columns, four selected creeps, distribution and miniboss HP.

Tower Survivor v110 — Damage-type color update

Magic: #9355DC → #A5B4FC (Celestial Purple).
Piercing: #FFD84D → #FFE45C (brighter yellow).
Chaos: #CC5500 → #E87524 (lighter orange).
Magic and Chaos spell-effect highlight colors adjusted to match. No rarity-color or gameplay-balance changes.

Tower Survivor v109 — Ankh of Resurrection

Replaces Epic Mythic Warcraft with Epic Ankh of Resurrection (10,000 gold). One purchase per run. On lethal castle damage, Ankh triggers before emergency Clear, restores castle to 10% maximum HP (capped at maximum HP), and triples HP regeneration for 5 seconds. The regeneration boost includes HP-growth healing. Emergency Clear remains available afterward.

All v92 gameplay and income-dashboard changes otherwise preserved.

Level details: Expected Creeps, Creep Types (armor and full HP), Spawn Interval, and Spawn Distribution.


v109: Stun diminishing returns per enemy. Successive stun applications have 100%, 90%, 80%, ... 10% minimum duration (no stun immunity). Bounce chain falloff and boss stun resistance remain unchanged.


v109: Reroll button shows how many rerolls remain in the current level. Count refreshes with the shop each level.


v109: Owned Towers shows attack speed buff and Tower/Towers counts.


v109: Normal damage color changed to neutral gray #A8ADB5; Chaos damage changed to burnt orange #CC5500. Chaos secondary glow adjusted to matching orange. Rarity colors and game balance unchanged.


v109: Crown of Thorns 450 base and poison stacks on retaliation; Wrath of Roots 150 base; Thorn Ward Uncommon and 40 block; Bulwark 200 base + 40 block + 10% enemy max HP reflection; Iron Bastion heals 25 per retaliation; Mending Thorns heals 25 per retaliation.


v109: Owned Towers panel now uses the same position, width and scrolling height as the Crown Challenges panel, below both top-right icons.


v109: Owned Towers and Crown Challenges popups are shifted up and left, centered in the unobstructed battlefield space beneath Clear and left of both top-right icons. Popup scrolling preserved.


v109: Level Details now displays exact armor matchups for Light, Medium, and Heavy armor, including damage bonuses and penalties by damage type. Normal/unlisted types remain neutral.


v109: HUD Income Details and Level Details both freeze game simulation while open and automatically resume on close. Existing manual pause state is preserved. Owned Towers and Crown Challenges do not auto-pause.


v109: Owned Towers attack-speed buff now appears as a bold, highlighted gold badge with a larger percentage; responsive on narrow screens. Gameplay unchanged.


v109: Ankh possession appears as a clickable Epic icon at the bottom right of the battlefield. Tap to open a shop-tile-style description; the icon disappears when the one-use Ankh activates. No automatic pause.


v109: Level Details title shows current level, creep types and accurate HP before armor matchup table and spawn distribution; types selected at level start. Owned Towers now shows a highlighted Critical Hit Chance tracker below Attack Speed.


v109: Ankh inventory icon uses a silver/gray metallic ankh silhouette inspired by the classic Warcraft III Ankh of Reincarnation. Inventory badge and detail card icon updated; functionality unchanged.

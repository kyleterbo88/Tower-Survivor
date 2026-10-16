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

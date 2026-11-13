WOBBLE CUP - CrazyGames build
==============================

HOW TO SUBMIT
1. Create a developer account: https://developer.crazygames.com
2. Add a new game -> upload THIS ZIP (index.html is at the zip root).
3. Fill in title, description, tags, and upload the cover images the portal asks for
   (use real screenshots of the game; sizes are listed in the portal).
4. Use the portal's QA / preview tool to test the build. Ads only appear for real on CrazyGames.
5. Submit for review. Earnings come from CrazyGames' ad revenue share once the game is live.

WHAT IS ALREADY DONE (SDK v3)
- SDK script in index.html, SDK.init() with a safe fallback when the SDK is missing (game still plays).
- gameplayStart / gameplayStop on match start, pause, menu, goal choice and results.
- Midgame ad: shown at a natural break, when you start the next match after finishing one.
- Rewarded ads (only after the player taps): "Free coins" (+60), "1 ad = 10 coins" (+10), "Double coins" after a match, and an extra Lucky Spin.
- The ad buttons wait for SDK.init() to finish, so a quick tap never fails. If no ad is available the player gets a message and no coins.
- Audio is muted and the game paused during ads. The game pauses when the tab is hidden.
- No external links, no ads of our own.

NOTES
- Controls: P1 = A/D + W (jump) + S (tackle). P2 = arrow keys. P / Esc = pause. Touch controls on phones.
- Google Fonts is loaded for the title font; if QA objects, delete the <link> line in index.html (the game falls back to Impact).
- Progress is stored in localStorage.

ENGAGEMENT: player levels + XP, daily login rewards (7-day streak), daily Lucky Spin, daily missions, win streak bonus, lucky chests.

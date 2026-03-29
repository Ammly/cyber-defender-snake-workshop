# 04 — Threats, Defenses & Lesson Cards

## Step 1 — Load lessons.json

Add this at the top of `game.js`, before anything else:

```javascript
let CURRICULUM = [];
fetch('lessons.json')
  .then(r => r.json())
  .then(data => { CURRICULUM = data; });
```

This loads all 14 threat/defense pairs from the file you copied into your project.

---

## Step 2 — Add Threats to the Game

Paste into Copilot Chat with `game.js` open:

> *"Update game.js to include a threat and defense system. Add `threat: null, defense: null, activeCurriculum: null` to the game state. Implement a `spawnThreat()` function that selects a random entry from CURRICULUM, placing a threat node and a defense node at available grid coordinates. In the draw() function, render nodes as 36x36 rounded square chips using roundRect: defense nodes with a light green fill (rgba(0,166,81,0.1)) and border (rgba(0,166,81,0.5)), and threats with a light red fill (rgba(239,68,68,0.1)) and border (rgba(239,68,68,0.5)). Add a small text label below each chip. Draw a thin dashed line (rgba(0,0,0,0.15)) as a tether between them that animates its dashOffset over time. Call spawnThreat() with a 35% chance when the snake eats a packet, and implement collision detection in move() for both types."*

Paste the additions into `game.js`. Save and verify threats and defenses appear on the grid after collecting a few packets.

---

## Step 3 — Add Lesson Cards

Add this HTML just before `</body>` in `index.html`:

```html
<div id="lessonCard" style="display:none; position:fixed; inset:0; background:rgba(255,255,255,0.6); backdrop-filter:blur(8px); z-index:100; align-items:center; justify-content:center;">
  <div id="cardInner" style="background:white; border-top:4px solid #00A651; border-radius:12px; padding:2rem; max-width:480px; width:92vw; box-shadow:0 20px 25px -5px rgba(0,0,0,0.1); position:relative; overflow:hidden; font-family:'Inter',sans-serif;">
    <div id="timerBar" style="position:absolute; top:0; left:0; height:4px; background:#00A651; width:100%; transition:width 0.1s linear;"></div>
    <div style="display:flex; justify-content:space-between; align-items:flex-start; margin-bottom:1.5rem;">
      <div style="display:flex; gap:12px; align-items:center;">
        <div id="typeIcon" style="width:40px; height:40px; border-radius:8px; display:flex; align-items:center; justify-content:center; background:rgba(0,166,81,0.1); color:#00A651; font-size:20px;">🛡️</div>
        <div>
          <div id="cardBadge" style="font-size:11px; font-weight:700; color:#6b7280; letter-spacing:.05em; text-transform:uppercase;">DEFENSE DEPLOYED</div>
          <h2 id="cardTitle" style="font-size:1.25rem; font-weight:800; color:#111827; margin:0;">MFA Implementation</h2>
        </div>
      </div>
      <div style="text-align:right;">
        <div style="font-size:11px; font-weight:700; color:#6b7280;">RESUME IN</div>
        <div id="cardTimer" style="font-size:1.5rem; font-weight:800; color:#111827;">19s</div>
      </div>
    </div>
    <div id="threatBlock" style="border-left:3px solid #E31937; padding-left:1rem; margin-bottom:1.5rem;">
      <div style="font-size:11px; font-weight:800; color:#E31937; margin-bottom:4px;">THREAT: <span id="threatName">BRUTE FORCE</span></div>
      <div id="cardThreat" style="font-size:14px; color:#4b5563; line-height:1.5;">Attempting to guess credentials by systematically trying all possible combinations.</div>
    </div>
    <div id="defenseBlock" style="border-left:3px solid #00A651; padding-left:1rem; margin-bottom:2rem;">
      <div style="font-size:11px; font-weight:800; color:#00A651; margin-bottom:4px;">DEFENSE: <span id="defenseName">MULTI-FACTOR AUTH</span></div>
      <div id="cardDefense" style="font-size:14px; color:#4b5563; line-height:1.5;">Requires multiple forms of verification to gain access, significantly reducing risk.</div>
    </div>
    <div style="display:flex; gap:12px;">
      <button id="extendBtn" onclick="extendTimer()" style="padding:12px 24px; background:#f3f4f6; border:none; border-radius:999px; color:#4b5563; font-weight:700; cursor:pointer; font-family:inherit;">+10S</button>
      <button id="continueBtn" onclick="dismissCard()" style="flex:1; padding:12px 24px; background:#00A651; border:none; border-radius:999px; color:white; font-weight:700; cursor:pointer; font-family:inherit;">CONTINUE (+1000 PTS) [SPACE]</button>
    </div>
  </div>
</div>
```

Now paste this into Copilot Chat with `game.js` open:

> *"Define `triggerLesson(entry)`, `triggerRisk(entry)`, and `dismissCard()` functions in game.js. triggerLesson: pause the game, set status to 'lesson', add 1000 to the score, and show the #lessonCard overlay with a green top border and a checkmark icon. Content should show entry.defense.name as the title, entry.threat.name in the threat block, and the curriculum lesson text in the defense block. triggerRisk: same pause and overlay but with a red top border, a warning icon, and no score bonus. Both functions should start a 20-second countdown that updates the #cardTimer text and depletes the absolute-positioned #timerBar width from 100% to 0%. dismissCard(): hide the overlay, clear the current threat/defense state, and resume the game loop. Ensure the Space key also dismisses the card when the game is paused for a lesson."*

---

## ✅ Final Check

- [ ] After collecting a few packets, a red + green node pair appears
- [ ] A dashed animated tether connects them
- [ ] Collecting the green node shows a lesson card with the correct content
- [ ] Hitting the red node shows a risk card
- [ ] Timer bar counts down
- [ ] Space or Continue button resumes the game
- [ ] Score updates correctly

**You're done. 🎉 Share your screen.**
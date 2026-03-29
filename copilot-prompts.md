# Copilot Rescue Prompts

Stuck? Paste the prompt for your current step directly into Copilot Chat or [claude.ai](https://claude.ai).

---

## Step 03A — HTML Shell

```
Create an HTML5 page for a cybersecurity snake game called CyberDefenderSnake.
Include: a full-page dark background (#040a04), a header showing 'CYBERDEFENDER SNAKE'
in green (#00A651) left and score display right, a centered canvas id='gameCanvas'
width='480' height='480', and a log panel id='log' below the canvas.
Link to style.css and defer game.js. Use JetBrains Mono from Google Fonts.
```

## Step 03B — CSS

```
Write CSS for a dark cybersecurity terminal game. Background #040a04,
text #e0ffe0, font JetBrains Mono. Style: header with green (#00A651)
bottom border and flex layout; canvas with 2px green border, centered,
green glow box-shadow; #log panel below — dark bg, monospace, 120px tall,
scrollable, small font. Add scanlines via body::after with
repeating-linear-gradient semi-transparent black lines every 4px.
```

## Step 03C — Snake Logic

```
Build a complete vanilla JS snake game on a 480x480 canvas id='gameCanvas'.
20x20 grid (CELL=24px). State object: snake array, direction, nextDirection,
dataPacket coords, score, speed=140, status='idle'/'playing'/'gameover'.
Functions: getRandomCoord() avoiding the snake; draw() — faint green grid,
green snake (#00A651) head with white eye dots facing direction of travel,
fading body, gold (#FFB612) pulsing data packet; move() — wall death,
self-collision death, eat packet to grow +10 score, spawn new packet,
speed += 2 per packet (min 55ms); handleKey() arrow+WASD no 180 reversal;
startGame() resets and starts setInterval. Show PRESS SPACE TO START at idle.
Update element id='score' each tick.
```

## Step 04A — Threat Spawning

```
Add threat/defense system to the existing snake game.js. Add to state:
threat:null, defense:null, activeCurriculum:null. Add spawnThreat() that picks
random entry from global CURRICULUM array, places threat at random unoccupied
coord and defense at different random coord, stores both with their curriculum
entry. Call spawnThreat() with 35% chance on each packet eat if no threat active.
In draw() if threat exists: draw red pulsing circle (sin pulse radius 10-14px,
shadowBlur=20, shadowColor='#E31937') at threat; green pulsing circle
(shadowBlur=15, shadowColor='#00A651') at defense; animated dashed line between
them (setLineDash([6,4]), lineDashOffset=-Date.now()/60). In move() detect head
landing on state.threat (call triggerRisk) or state.defense (call triggerLesson).
Leave triggerRisk/triggerLesson as empty stubs.
```

## Step 04B — Lesson Card Logic

```
Implement triggerLesson(entry), triggerRisk(entry), dismissCard() for the snake
game. triggerLesson: clearInterval game loop, status='lesson', score+=500,
update score display, show #lessonCard (display:flex), set #cardBadge to
'✅ DEFENSE DEPLOYED' in green, #cardTitle to entry.defense.name, #cardThreat to
threat name + description from entry.lesson, #cardDefense to defense name +
entry.lesson, #continueBtn background #00A651 text 'CONTINUE (+500 PTS) [SPACE]'.
triggerRisk: same but no score bonus, badge '⚠ THREAT ENCOUNTERED' in red
#E31937, continueBtn red. Both start 20s countdown animating #timerBar width
100%→0% via setInterval 50ms, auto-dismiss on complete. dismissCard(): hide card,
clear state.threat and defense, restart setInterval(move, state.speed),
status='playing'. Space key calls dismissCard when status==='lesson'.
extendTimer() adds 10s to countdown.
```

## Debugging — Snake Not Moving

```
Here is my game.js. The snake does not move when I press Space.
Find the bug and fix it only, do not rewrite the whole file.
[paste your game.js here]
```

## Debugging — Threats Not Appearing

```
Here is my game.js. The threat and defense nodes never appear during gameplay.
CURRICULUM is loaded from lessons.json via fetch at the top.
Find why spawnThreat() is not being called or not working and fix it.
[paste your game.js here]
```
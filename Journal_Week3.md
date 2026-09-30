# Journal Entry of week 3

Team **BEACH**, Bianca, Emma, Alexandre, Cheuk and Hubert (me), has contacted Jonathan Lessard (client)

We took some key notes in our meeting. 

Under here, it is a compilation of our notes that will be important for us


============================================

# Meeting Notes Summary — CART 415 Project with Jonathan Lessard


## Core Concept

A **large-screen exhibition game** where many visitors play collectively using their phones:

1. Player sits down / approaches
2. Visitor sees a sign → scans a QR code
3. Opens a webpage on their phone (simple Nintendo-style controller interface)
4. Controls an avatar on a large projected screen amongst many others

**Key constraint:** Onboard visitors quickly and easily — no 30-minute setup. Simple controls (left/right, button presses — avoid drag/move due to latency).

---

## Design Problems to Explore

### Player Experience
- 20–30 players at a time
- Short engagement, players popping in and out continuously
- Probable latency in inputs/outputs — must be considered
- Simple controls: left/right, simple button presses (not drag/move)

### Multiplayer / Game Structure
- **Asynchronous interaction** — persistent game, permanent game space
- **No traditional lobby** (or a persistent lobby)
- Pop-in / pop-out players
- Leaderboard (always present — what is the score? How do you get it?)
- Turn-based concept, but not necessarily traditional turns
- Possible team split (two teams) — more players = faster progress
- Gameplay could be ~5 minutes, or an infinite/ongoing game

### Open Questions
- If the player presses left, does the character move left?
- How do we create many characters? (Base body + variations?)
- How do players know what is happening?
- What happens when players leave? (Disappear? Become part of an "army"? Body becomes dead to be consumed?)
- Does the character stay or disappear?
- What is the player trying to do, and how do they know they did it well?
- Need a goal or achievement to encourage participation
- Could players log in again and continue playing?
- Need to define what the score represents

### No-Player Situation
- What does the experience do when no one is playing?
- Projector screen could continue showing something
- Avoid simply having a menu
- Tutorial could remain on the phone (not on main screen — don't distract others)
- Possible livestream / chat board
- Non-blocking information
- Unity scene camera could continue displaying the game world

---

## Game Idea / Concept Mentioned by Jonathan

**Abstract dot concept:**
- You are dots; multiple dots appear, but you don't know who you are
- Move to figure out who you are
- Goal: all dots reach the middle (or a target)
- Asynchronous — don't all need to play at the same time
- Start from very abstract representation, discuss gameplay at that level before deciding final visual direction
- 0001 / numbers — move left/right, up/down, change the number, reach a target

**References:**
- Baba is You
- Sokoban (possible template/reference for gameplay structure — someone pushing stuff)

---

## Visual / Art Direction (Second Stage)

- Keep things simple and broken down initially
- Possible use of:
  - Colour coding
  - Different character bodies / variations
  - Sound
  - Phone feedback (vibration — e.g., notify when you left the game / someone killed you — give a reason to come back)
  - Notifications
  - Feedback when a player loses
- Consider how the game looks when there are more players
- Mapping between player input and game could be 1-to-1
- One-screen game: What do we see? What is on screen vs. outside? 2D? Front view? Top-down view?
- Art direction can be explored in second stage

---

## Technical Direction

- Technical decisions come after first meeting / concept exploration
- First focus on:
  - What the game could be
  - How the interaction works
  - What problems need to be solved
- Technical implementation discussed later; suggestions can be provided
- Jonathan has a server (multiplayer, asynchronous, persistent game)
- **Stack questions:**
  - What's the engine?
  - What hardware is it run on?
  - What manages phone connections and input transmissions?
  - How to keep it relatively simple and manageable?
- Keyboard controls could be used for some prototypes
- "Blue sky" possibilities: sound, phone feedback, notifications
- Accurate / responsive player control

---

## Methodology / Approach

- **De-risk it** — remove the most risk first
- Play the game in the mind first → avoid unnecessary risks
- Develop ideas through: Paper prototypes, Wireframes, Pre-production, Technical prototypes
- Explore potential issues first
- Not necessarily aiming to deliver a fully finished game immediately
- Map out all the problems and solutions
- Develop different ideas and let Jonathan choose between them
- Provide a screen / visual prototype
- One full project managed as a producer; whole class works on same project
- Saves time with dead ends, weeding out things, potential approaches
- Wireframe is the main aspect; prototype mainly
- The game is always there; 20–30 avatars of people there

---

## Expected Outcome (from Question for Jonathan)

- Propositions of different fidelity for all questions — from "pitches" to mockups
- Ideally a "proof of concept" prototype (very minimal: people connect with phone to a link, press buttons, see something happening on shared screen — even just dots moving)
- Start CART 415 with significant foundations and get moving relatively fast

---

## Key Constraints & Principles

- **AVOID LOBBY** — permanent; if there is a stage, the other is automatic (not need)
- **No host, always on**
- **Static screen makes more sense** (fixed, so no one can get out of the screen; if not, needs to be thought through)
- **Simple is beautiful** — UI should not be too complicated
- **Tutorial on phone** (before controller) — don't want it on main screen (not distract others)
- **Projector screen** (better)
- **Leaderboard always present** — need to define score
- **One-screen game** — what do we see, what is on screen, what is outside?
- **Don't have to be more than 3 PowerPoint slides**
- **At least 5 minutes of interaction** (doesn't mean 5 minutes of game)
- **Something needs to be achieved**
- **Random level and think about reset**
- **It can be many games or levels, but one version also works**
- **Explore the body and not just the phone**
- **Character can be a solution or prototype** for variety


============================================




## Concept 1: "The Swarm" — Collective Dot Movement

Core Idea:
Everyone is a dot on screen. You don't know which dot is yours until you move. The goal is for all dots to gather in the center (or a target zone) simultaneously.

How It Works:

· Player scans QR → phone becomes a simple D-pad (left/right/up/down)
· Player presses a direction → their dot moves on screen
· Player discovers which dot is theirs through movement
· Goal: all dots reach the center at the same time
· When a player leaves, their dot remains as a static obstacle or slowly drifts

Pros:

· Extremely simple to understand and prototype
· Asynchronous by nature (dots persist)
· No tutorial needed — move to figure out who you are
· Visually striking with 20–30 dots moving

Cons:

· May lack long-term engagement
· "All reach center" goal may be frustrating with random players
· Needs a strong feedback loop to feel rewarding

Exhibition Twist:

· When no one plays, dots slowly drift and form patterns
· Leaderboard: who reached center fastest? Who helped most?

---

## Concept 2: "Territory Paint" — Team Color War

Core Idea:
Two teams (Red vs. Blue). Players move their avatars around a grid-based screen. Wherever they walk, they paint the tile their color. Team with the most tiles at the end of a 5-minute round wins.

How It Works:

· Phone: left/right/up/down controls
· Each player is a colored square/dot on a grid
· Moving over a tile claims it for your team
· Opponents can overwrite your tiles by walking over them
· Rounds last 5 minutes, then reset with a winner announcement
· Players can join mid-round (pop-in)

Pros:

· Immediately readable — everyone understands color war
· Team play creates emergent cooperation
· Short rounds = frequent wins/losses = engagement
· Easy to prototype (grid + colors)

Cons:

· Team balance issues if one side has more players
· Needs a reset mechanic that doesn't feel punishing
· May need a "no-player" state where tiles slowly decay

Exhibition Twist:

· When no players, the board slowly fades to neutral
· Leaderboard: individual tiles claimed, team wins

---

## Concept 3: "The Tower" — Collective Stacking

Core Idea:
A tower grows in the center of the screen. Each player contributes blocks by pressing buttons on their phone. The tower must be built high enough to reach a goal before time runs out — but it can also collapse if too many players add blocks too fast.

How It Works:

· Phone: one button (ADD BLOCK) and left/right (to choose side)
· Each press adds a block to the tower
· If the tower becomes unbalanced (too many blocks on one side), it collapses
· Players must coordinate — add evenly, communicate through movement
· Goal: reach a target height within 10 minutes
· When players leave, their contributions remain

Pros:

· Creates natural tension and cooperation
· Simple one-button interaction (great for latency)
· Visual spectacle — a giant tower growing on screen
· Asynchronous — tower persists between sessions

Cons:

· May be too simple without additional mechanics
· Collapse mechanic could feel punishing
· Needs clear feedback on balance

Exhibition Twist:

· When no players, the tower stands silently
· Leaderboard: total height achieved, most blocks contributed

---

## Concept 4: "Ecosystem" — Predator & Prey

Core Idea:
Players are creatures in a simple ecosystem. Some are predators (bigger dots), some are prey (smaller dots). Predators eat prey to grow; prey eat food pellets to survive. The goal is to survive as long as possible or reach the top of the food chain.

How It Works:

· Phone: D-pad to move
· Players start as prey (small dots)
· Eating food pellets → grow → become predator
· Predators eat prey → grow larger
· If eaten, you respawn as prey after a short delay
· Persistent world — creatures stay when players leave (become AI-controlled?)
· Leaderboard: longest survival, most prey eaten

Pros:

· Emergent gameplay — different roles create variety
· Asynchronous — world persists
· Visual clarity: size = power
· Pop-in/pop-out works naturally

Cons:

· More complex to balance
· May need AI for abandoned creatures
· Could be frustrating for new players (immediately eaten)

Exhibition Twist:

· When no players, creatures wander as AI
· New players see a living world before joining

---

## Concept 5: "Signal" — Cooperative Puzzle Solving

Core Idea:
The screen shows a giant grid of nodes (like a circuit board). Players are "signals" that must travel from one side to the other. Each player controls one signal. The catch: signals can only pass through nodes that are activated by other players standing on them. Cooperation is mandatory.

How It Works:

· Phone: D-pad to move your signal
· Screen: grid of nodes, some active, some inactive
· Players must position themselves on inactive nodes to activate them for others
· Goal: get as many signals as possible to the other side within 5 minutes
· If a player leaves, their signal becomes a static node
· New players join as new signals

Pros:

· Deep cooperation — players must work together
· Asynchronous — nodes persist
· Puzzle-like, satisfying when solved
· Visually interesting (circuit board aesthetic)

Cons:

· May be too complex for quick onboarding
· Requires communication (hard in exhibition)
· Needs careful level design

Exhibition Twist:

· When no players, the grid slowly pulses with light
· Leaderboard: signals delivered, nodes activated

- **Design problem:** does my character stay there or disappear? (find all the problems)
- **We can have ideas for games** (what is the story?). Is it a team game or team vs. team?
- **What is the player trying to do, and how does the player know he did it well?**

---


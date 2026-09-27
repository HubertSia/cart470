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
- **Design problem:** does my character stay there or disappear? (find all the problems)
- **We can have ideas for games** (what is the story?). Is it a team game or team vs. team?
- **What is the player trying to do, and how does the player know he did it well?**

---


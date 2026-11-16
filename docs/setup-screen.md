# Starting (Setup) Screen

The screen shown when the app opens and after **New Game**. It collects everything needed to start a round, and **🐺 Start Round** at the bottom begins play. The bottom tab bar is hidden here and appears once the round starts (see [Bottom Tabs](bottom-tabs.md)).

At the top right, **🗂 History** opens past rounds.

**Round in Progress banner** – if a round was saved on this device and not finished, a banner appears above Round Info:
- **▶ Resume Round** – continue where you left off (goes to the Hole screen, or the Scoreboard if the round was already finished).
- **Discard & Start New** – deletes the saved round after a confirmation. This cannot be undone.

Sections, top to bottom:

1. [Round Info](#1-round-info)
2. [Hole Handicap Ratings](#2-hole-handicap-ratings)
3. [Number of Players](#3-number-of-players)
4. [Starting Hole](#4-starting-hole)
5. [Player Names / HCP / Tee](#5-player-names--hcp--tee)
6. [Configuration](#6-configuration)
7. [Point Multipliers](#7-point-multipliers)

---

## 1. Round Info

| Field | What it does |
|-------|--------------|
| **Course** | Pick from the courses in your library. **Required** to start. |
| **⚙** (next to Course) | Opens the **Courses** library so you can search for a course, add one manually, or edit/delete saved ones. **← Back** returns here with the list refreshed. |
| **Tee** | The tee set used for the round, listed with its yardage, for example *Blue (6,420 yds)*. **Required** to start. Available once a course is chosen. |
| **Date** | Defaults to today. It appears on the Scoreboard, Scorecard and History. |

Choosing a tee loads that tee's hole handicap ratings and pars (next section) and sets the default tee for every player.

---

## 2. Hole Handicap Ratings

Appears after a course **and** tee are selected. The chip says **1 = hardest**.

- A grid of **H1–H18**, split into **Front 9** and **Back 9**, shows each hole's handicap rating (stroke index). They are filled in from the selected tee and can be edited by hand.
- **Hide Ratings** collapses the section (the values are still used).
- **Clear** resets every hole to its own number (H1 = 1, H2 = 2 … H18 = 18). This is a plain default, not a blank, so it is a reasonable choice if the course's ratings are unknown.

**How handicaps become strokes**
- The app uses the **difference from the lowest handicap in the group**. The lowest-handicap player plays scratch, and everyone else receives strokes equal to their handicap minus that player's.
- A player receives a stroke on every hole whose rating is **less than or equal to** their stroke count (a difference of 18 or more gives a stroke on every hole, with the extra strokes starting again from the hardest hole).
- If no handicaps are entered, no strokes are given and the ratings have no effect.
- If a player is on a different tee (section 5), that player's own tee ratings are used for them.

Strokes show as dots on the score-entry rows and the Scorecard.

---

## 3. Number of Players

A drop-down: **4, 5, 6 or 7 players**.

Changing it:
- adds or removes player rows (names, handicaps and tee choices already entered are kept),
- resets the **Configuration** values to the defaults for that group size (see section 6), so make any manual changes to those *after* choosing the number of players,
- highlights that group size's column in the multiplier table.

The player count also decides how many partners the Wolf can pick. With the default multipliers that is up to 1 for 4 players, 2 for 5–6, and 3 for 7. The limit follows which *Picks* rows have a multiplier for that group size (section 7).

---

## 4. Starting Hole

**Start on hole** – a number from 1 to 18 (default 1), for shotgun starts or when you begin on the back nine.

A note beside the box shows the play order, for example:

| Start | Note |
|-------|------|
| 1 | Plays 1 → 18 |
| 12 | Plays 12 → 18, then 1 → 11 (first 9 end at hole 2) |
| 10 | Plays 10 → 18, then 1 → 9 |

Holes are always played in this order, wrapping from 18 to 1. "First 9" means the first nine holes *played*, which is when the front-points rate changes to the back-points rate. It is not the course's front and back nine.

Changing the starting hole updates **Wolf Hole Number** in Configuration to the default for the new start.

---

## 5. Player Names / HCP / Tee

The chip says **in tee-off order**. Each player has a numbered row:

| Part | What it does |
|------|--------------|
| **Number (1–7)** | Tee-off position. **Player 1 is the first Wolf**, then the Wolf rotates in this order. |
| **Name** | Shows *Player N* as a placeholder; leaving it blank uses that placeholder as the name. |
| **HCP** | Course handicap, 0–36. Blank counts as 0. Used for strokes (see section 2). |
| **Tee** | That player's tee. It defaults to the Round Info tee and follows it if you change it, until you pick a different tee for that player. After that the player's choice is kept. It is disabled until a course is selected. |

Per-player tees mean golfers playing from different tees each get their own hole handicap ratings.

---

## 6. Configuration

A **Setting / Value** table. Values are set automatically from the number of players and starting hole, and can be overridden.

| Setting | Meaning | Defaults (4 / 5 / 6 / 7 players) |
|---------|---------|----------------------------------|
| **Wolf Hole Number** | The **actual hole on the course** where the "Lowest Player Wolf" holes begin. From that hole through the end of the round, the Wolf is whoever has the fewest points. | 4 players: the 17th hole played. 5, 6, 7 players: the 16th hole played. For a start on hole 1 that is hole 17 / 16 / 16 / 16. For a start on hole 12 with 5 players it shows hole 9. |
| **Points Holes Played 1-8** | Base points per hole for the first eight holes played. | 2 / 3 / 2 / 3 |
| **Points Holes Played 9-Wolf Hole** | Base points per hole from the 9th hole played up to the hole before the Wolf holes begin. | 4 / 3 / 4 / 3 |

Notes:
- Both point settings count holes **in play order**, not course hole numbers.
- Base points for the Wolf holes are not set here. They are entered hole by hole during play (it suggests half of what the Wolf owes, rounded up).
- Pushed holes carry their base points to the next hole, except into Wolf holes.
- These can be changed later in the **Settings** tab, which recalculates completed holes.

---

## 7. Point Multipliers

A **Decision × group size** grid. The stake for a hole is the hole's base points (plus any carryover) multiplied by the multiplier for the decision and group size, and by 2 for each double.

| Decision | 4P | 5P | 6P | 7P |
|----------|----|----|----|----|
| Lone Wolf (after tee) | 3 | 4 | 4 | 5 |
| Lone Wolf (after all) | 2 | 3 | 3 | 4 |
| Picks 1 | 1 | 2 | 2 | 3 |
| Picks 2 | — | 1 | 1 | 2 |
| Picks 3 | — | — | — | 1 |

- Boxes are editable. Enter a whole number of 1 or more. A blank or invalid entry is treated as no value.
- A dash (—) means the decision isn't available for that group size, so it can't be edited.
- A **Solo** player uses the *Lone Wolf (after all)* multiplier.
- The column for the group size you picked is shaded.
- **Reset to defaults** restores the table above.
- The values in force when you tap **Start Round** are saved with the round, so later changes to the defaults don't affect it. You can still adjust them in the **Settings** tab during play.

---

## Start Round

**🐺 Start Round** checks that:
- a **course** is selected ("Select a course before starting the round"), and
- a **tee** is selected ("Select a tee before starting the round").

It then saves the round, shows the bottom tab bar, and opens hole 1 of play (the starting hole).

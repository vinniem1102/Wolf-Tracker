# Bottom Tabs

> Setup screen: see [Starting Screen](setup-screen.md).

Once a round has been started (or resumed from the banner on the Setup screen), a six-button bar appears at the bottom of the app. It is hidden on the Setup screen and comes back after **Start Round** or **Resume**.

| Tab | Icon | Screen | Purpose |
|-----|------|--------|---------|
| Hole | ⛳ | Hole | Play the current hole: team, score entry, result |
| Scores | 📋 | Scoreboard | Running totals, hole-by-hole log, edit past holes, final ledger |
| Card | 📊 | Scorecard | Full 18-hole grid of scores, roles and running $ |
| Settings | ⚙️ | Settings | Mid-round adjustments and recalculation |
| Courses | 🏌 | Course Library | Search, add, edit and delete saved courses and tees |
| History | 🗂 | History | Finished rounds saved on this device |

The active tab is highlighted. After the final hole is finished and **View Final Scores** is tapped, the Hole tab is hidden because there is nothing left to play.

---

## ⛳ Hole

The working screen for the hole currently being played. The header shows **Hole N of 18**, and a **Scores ↗** shortcut jumps to the Scoreboard.

**Hole banner**
- The hole number (large), the **Wolf** for this hole, and the points at stake (⬡ pts).
- A **+ N carry** badge appears when a pushed hole has carried points over. Carryover never applies on Wolf holes.

**Who is the Wolf**
- Before the Wolf holes begin, the Wolf rotates through the players in the order you set up (Player 1 on the first hole played, and so on).
- On Wolf holes, the Wolf is the player with the fewest points. Ties are broken randomly.

**Wolf hole points** (Wolf holes only)
- A **Wolf hole – update manually** box with **Points this hole**.
- It starts at half of what the Wolf currently owes, rounded up (8 if the Wolf owes nothing). Type over it to change it; the stake updates as you type.

**Step 1 – Wolf Decision**
- **Lone Wolf – after my tee shot** or **after all tee shots**, or
- pick partners from the tee-order list (the number of partners available depends on the player count), then tap **Confirm Team →**.
- Each non-Wolf player in the list also has a **Solo** button, for a player who declares they are playing alone against everyone else.

**Step 2 – Enter Scores**
- The confirmed team is shown, then one score box per player with their handicap strokes. Entry auto-advances to the next player after one digit.
- **Number of Doubles** and the **Stake** are shown above the score boxes. Each double multiplies the stake by 2, and the stake can also be typed in directly. A manually entered stake overrides the calculated one.
- **Calculate Result →** works out the payout.

**Result**
- Shows who won, the stake, and each player's gain or loss.
- **Next Hole** moves on in play order. On the last hole of the round the button becomes **🏁 View Final Scores**.

---

## 📋 Scores (Scoreboard)

- **Running Totals** – every player sorted from most to fewest points, with **Points** and **This Hole** (the change from the last hole). A dot marks the player who is Wolf on the current hole, until the Wolf holes begin.
- **Hole-by-Hole Log** – one row per hole played: result (Wolf wins / Opponents win / Solo / Push), the Wolf, the decision, the stake and any doubles. Wolf holes are labelled **Wolf hole**.
  - **Edit** on a row reopens that hole to change the scores, the Wolf decision or partners, the doubles, the stake and (on Wolf holes) **Points this hole**. **Recalculate Preview** shows the new result, then **Save & Return** applies it and recalculates every later hole. Edit is disabled for the hole currently in progress; finish it with **Next Hole** first.
- **Back to Current Hole** returns to the Hole tab.
- After **View Final Scores**:
  - a **Final Ledger** shows who pays whom,
  - **🖨 Print Results** and **New Game** appear,
  - the round is saved to History automatically.

---

## 📊 Card (Scorecard)

A traditional 18-hole card, always laid out in course order (holes 1–9, **Out**, 10–18, **In**, **Tot**), regardless of the starting hole.

- **Stake** and **Doubles** rows across the top.
- For each player:
  - a name row showing their role on each hole – 🐺 Wolf, **P** Partner, ★ Solo,
  - a **Score** row (gross) with a dot for each handicap stroke; a hole won by that player has its score circled,
  - a **Wolf $** row showing the running money total after each hole (— on pushed holes).
- 🖨 in the header prints the card.

---

## ⚙️ Settings

Mid-round adjustments. **Cancel** returns to the Hole tab without changes; **Save & Recalculate →** applies them.

- **Appearance** – theme: **System** or forced **☀️ Light** (useful outdoors).
- **Course & Tee** – starting hole, course name, load from library, search, add manually, and tee. These lock after the first hole is played (the chip shows *locked after first hole*).
- **Players & Handicaps** – rename players and change handicaps.
- **Point Values**
  - **Wolf Hole Number** – the actual hole on the course where Wolf holes begin. It follows the starting hole; for example, 5 players starting on hole 12 default to hole 9.
  - **Points Holes Played 1-8** and **Points Holes Played 9-Wolf Hole** – base points per hole. These count holes in play order, not course numbers.
- **Point Multipliers** – the multiplier for each decision type (Lone Wolf, Picks, Solo, and so on) at 4, 5, 6 and 7 players.

When handicaps, point values or multipliers change, all completed holes are recalculated. The Wolf hole point values you entered by hand are kept.

---

## 🏌 Courses (Course Library)

The saved course and tee data used on the Setup and Settings screens. **← Back** returns to the screen you came from.

- **Search Courses** – looks up clubs and courses on GolfCourseAPI (through the app's proxy). Results show the club and course name so multi-course clubs are distinguishable; choose one to save its tees, yardages, hole handicap ratings and pars.
- **+ Manually Add New Course** – enter a course name and one or more tee sets (name, yardage, per-hole handicap ratings and pars).
- **Saved Courses** – each course lists its tees, with **Edit** and **Del** buttons.

---

## 🗂 History

Finished rounds, saved on this device only (up to 100). **← Back** returns to Setup.

- Each entry shows the course, date, time saved and number of players.
- **View** opens a read-only copy of the round: **Final Ledger**, **Scorecard**, **Hole-by-Hole Log**, with a **🖨 Print Results** button.
- **Del** removes a round (asks for confirmation; it cannot be undone).
- A round only appears here once it has been finished with **View Final Scores**.
- Rounds that are still being played are not listed. They are saved automatically and offered as **Resume** on the Setup screen.

---

## Notes

- Everything is stored in the browser on the device (round in progress, history, saved courses, theme). Clearing site data removes it.
- The app is a single static page; reloading it, or reopening the home-screen icon, picks up new versions. On iPhone you may need to force a fresh load (for example by adding `?v=2` to the address) after an update.


# Soccer Match Simulation in R

### Author: Levi Makwei  
### Date: 03/28/2022  
### Output: HTML Document  

---

## 📋 Overview

This R script simulates a simplified 90-minute soccer match between two teams using randomized player actions and probability-based outcomes. It models ball movement, possession changes, passing, shooting, and scoring in a sector-based virtual field.

---

## ⚽ Simulation Design

- The pitch is divided into **4 sectors**, with players distributed across them.
- Each team has players assigned to specific sectors, which impact scoring and possession battles.
- The game begins with a **coin toss** to determine initial possession and ball sector.
- The ball moves based on successful **passes** and **shots**.
- Each minute of play is simulated with randomized outcomes based on:
  - Offensive and defensive player "scores"
  - Probability of long shots, offsides, and successful goalie passes
- Scores are updated in real time, and match results are printed at the end.

---

## 🔁 Core Functions

- `start()`: Initializes the match with a coin toss and sets possession and position.
- `updatePlayer()`: Randomly selects a player in possession from the current sector.
- `scoreCalc(players)`: Generates a performance score based on involved players.
- `pass(team)`: Simulates a pass based on offensive vs defensive strength.
- `shot(minute, score)`: Simulates a shot on goal and updates the score if successful.
- `longShot(minute)`: Attempts a long-distance shot.
- `goalie()`: Determines how a goalie distributes the ball on possession start.
- `round(minute)`: Main engine of the match that runs every game minute.

---

## 🧠 Probabilities

- `pLongShot`: 30% chance a long shot is taken.
- `pOffsides`: 15% chance of an offside when in attacking sector.
- `pGoalieTo2`: 60% chance the goalie passes to the next sector instead of a long clearance.

---

## 📈 Output

The simulation prints out key events such as:

- Coin toss results  
- Shot attempts and goals  
- Changes in possession  
- Offsides and interceptions  
- Final score and match outcome

---

## ✅ How to Run

This script is written in **R Markdown** and outputs an **HTML document**. To run:

1. Open the `.Rmd` file in RStudio.
2. Click `Knit` to generate the simulation output as an HTML report.
3. Review the printed play-by-play in the resulting document.

---

## 📝 Notes

- The game is purely probabilistic and for educational/demo purposes.
- Player numbers and performance are simplified for simulation logic.

---

Feel free to reach out if you'd like to extend the logic with more complexity (e.g. substitutions, fouls, cards, or player stamina).

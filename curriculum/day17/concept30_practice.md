# 🛠️ Concept 30 Practice: Map Building Data (2D Grids)

### 🚀 The 20-Problem Challenge Menu
*Note: Today we build the worlds our characters walk in!*

#### 🟢 Group A: The Grid Builders (Warmups)
1.  **Simple 2D List:** Create a 2x2 grid with numbers. Print the whole thing.
2.  **Access the Corner:** Print the item at `[0][0]`.
3.  **The Bottom Right:** Print the item in the last slot of the last row.
4.  **Count the Rows:** Use `len()` to see how many rows are in your grid.
5.  **Multi-Print:** Define a grid and print only the 1st row.

#### 🟡 Group B: Map Management
6.  **The Wall Builder:** Change an empty space `" "` to a Wall `"W"` at `[1][1]`.
7.  **The Player Move:** Move a `"P"` from `[0][0]` to `[0][1]` by updating the values.
8.  **Row Loop:** Use a `for` loop to print every row on its own line.
9.  **The Score Matrix:** Create a grid of points. Add up all the points in the first row.
10. **The Seat Checker:** In a `[["X", " "]]` grid, print "Available" if `[0][1]` is `" "`.

#### 🔴 Group C: The Bug Squasher (Fix the Coordinates)
11. **Single Bracket:** `grid[0,1]` (Fix it!).
12. **Out of Range:** Trying to access `grid[5][0]` in a grid with only 3 rows.
13. **Mismatched Rows:** A 2D list where one row has 3 items and the other has only 1 (Fix the imbalance!).
14. **The Variable Mistake:** Using `row` when you meant `col` inside the brackets.
15. **The Spelling Trap:** `greed = [[]]` (Fix the typo!).

#### 💎 Group D: The AI Whisperer (Gemini Missions)
16. **The Tic-Tac-Toe Pro:** Ask Gemini: "Write a 3x3 Tic-Tac-Toe board in Python and a function that checks if there is an 'X' in the middle."
17. **The Maze Maker:** Ask Gemini: "Give me a 5x5 ASCII art maze using a list of lists. Use '#' for walls and ' ' for paths."
18. **The Random Grid:** Ask Gemini: "How do I use `random.randint()` and a `for` loop to fill a 10x10 grid with random 0s and 1s?"
19. **The Real-World Modeler:** Ask Gemini: "How does a game like **Among Us** know when the 'Impostor' is in the same room as a 'Crewmate' using grid coordinates?"
20. **The Challenge:** Ask Gemini: "Give me a challenge where I have to print a grid but replace all the 0s with 🟢 and all the 1s with 🔴!"

---

### 🌟 Stretch Goal for "Flash" Students
Build a **"Treasure Hunter 2D"**! 
1. Create a 4x4 grid filled with `" . "`.
2. Hide a `" X "` at a random coordinate `[row][col]`.
3. Use a `while` loop to ask the user: "Select a Row (0-3)" and "Select a Col (0-3)".
4. If their guess matches your hidden coordinate, they find the Gold!
 Riverside

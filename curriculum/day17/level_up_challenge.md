# 🏆 Day 17 Project: The Haunted House Builder 🏰

**Goal:** Use 2D Lists and File Saving to build a custom "Spooky Map" that your friends can play through.

---

### 📋 The Mission
You are the architect of a haunted mansion. You need to design a map made of different rooms (Library, Kitchen, Ghost Room) and save that map to a file so it can be "Loaded" later.

### 🛠️ Step 1: The Blueprint (2D List)
Create a 3x3 grid called `mansion`.
Fill it with different room names:
- `mansion = [["Library", "Lobby", "Kitchen"], ["Armor Room", "Ghost Room", "Dining"], ["Basement", "Secret Hall", "Exit"]]`

### 🛠️ Step 2: The Player Controller
1. Create `row = 1` and `col = 1` variables (The starting spot).
2. Use a `while` loop to say: `f"You are currently in the {mansion[row][col]}."`
3. Ask the user for their move: "N, S, E, W" (North, South, East, West).

### 🛠️ Step 3: Navigation Logic
- **IF North:** `row -= 1`
- **IF South:** `row += 1`
- **IF East:** `col += 1`
- **IF West:** `col -= 1`
*HINT: Use a `try/except` block to catch the error if the player tries to walk off the edge of the map!*

### 🛠️ Step 4: Saving the Blueprint
When the player reaches the "Exit," use `with open("map_save.txt", "w")` to save the final `mansion` grid to a file.

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "I am building a 2D map game. How do I make it so that if a player enters the 'Ghost Room', they lose 10 health? Show me the if-statement logic for checking the grid value!"

### 🌟 The "Real World" Mission
Add a **"Fog of War"** feature. 
Create a second 3x3 grid called `discovered` filled with `False`. 
Every time the player moves to a new room, set that spot to `True`.
When they "Check Map," only show them the rooms they have already visited!
*This is how professional games like **Diablo** or **Starcraft** hide the map from the player until they explore it!*

---

### 🕵️ Why are we doing this?
In the professional world, this is called **"Level Design Data."** 
When you play a game like **Among Us** or **Minecraft**, the map isn't "Hardcoded" into the game—it’s a data file with numbers and letters that the computer reads and turns into walls and hallways. You just built the foundation of a modern level editing system!

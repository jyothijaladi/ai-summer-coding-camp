# 🏆 Day 18 Project: The Minecraft Inventory (JSON Save) ⛏️

**Goal:** Use JSON and Dictionaries to build a professional-grade inventory system that saves itself automatically.

---

### 📋 The Mission
You are building the "Backpack" system for a block-building game. You need to keep track of how many blocks of each type the player has, and make sure that data stays safe even if the computer restarts.

### 🛠️ Step 1: The Inventory Structure
Create a dictionary with keys for block types and values for their counts.
- `inventory = {"Diamond": 0, "Iron": 5, "Dirt": 64}`

### 🛠️ Step 2: The Mining Loop
1. Create a `while True:` loop.
2. Ask the user: "What do you want to do? [Mine / Check / Save / Quit]"

### 🛠️ Step 3: The Interaction
- **IF Mine:** Ask which block they found. Add 1 to that block's count in the dictionary.
- **IF Check:** Print the current inventory using a clean `for` loop.
- **IF Save:** Use `json.dump()` to save the dictionary into `inventory.json`.

### 🛠️ Step 4: The Auto-Load
At the very top of your file (before the loop), try to `json.load()` the file.
- **IF** the file exists, update your starting inventory with the saved data!
- **ELSE**, start with a fresh (empty) inventory.

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "I am building a Minecraft inventory in Python using JSON. How do I make and print the inventory in a 'Pretty' format with indents using `json.dumps()`?"

### 🌟 The "Real World" Mission
Add a **"Crafting Station"**.
1. Create a function called `craft_pickaxe()`.
2. **Check:** IF the player has 3 "Iron" and 2 "Sticks" in their JSON-loaded inventory, subtract those items and add 1 "Iron Pickaxe".
*This is the exact logic used in **Minecraft**, **Roblox**, and **Terraria** to handle recipes and crafting!*

---

### 🕵️ Why are we doing this?
In the professional world, this is called **"State Serialization."** 
When you save your world in **Minecraft**, the game is turning every block coordinate, player stat, and item count into a massive JSON-like file on your disk. You just built the backbone of the world’s most popular games!

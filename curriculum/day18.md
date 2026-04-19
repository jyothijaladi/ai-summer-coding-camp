# ⛏️ Day 18: Project - The Minecraft Inventory Clone

**Time:** 9:00 AM - 12:00 PM
**Daily Goal:** Learn about JSON—the professional way to save complex data like RPG inventories and game stats.

---

## 🕒 9:00 AM – 10:40 AM: 🛠️ Guided Build – The JSON Power-Up 💎
*Learning how to save a whole dictionary at once.*

1.  **What is JSON?** 
    - Explain that JSON is a "Universal Language" that looks exactly like a Python Dictionary.
    - `import json`
2.  **Saving the Inventory:**
    - `inventory = {"Diamonds": 5, "Sword": 1}`
    - `with open("save.json", "w") as f: json.dump(inventory, f)`
3.  **The AI Connection:**
    - Ask Gemini: "Why do game developers use JSON files instead of regular text files to save character stats?"

---

## 🕒 10:40 AM – 11:00 AM: 🥤 Mini-Break / Buffer

---

## 🕒 11:00 AM – 12:00 PM: 🏝️ The Sandbox Exploration
*Goal: Build the "Mining & Saving" System.*

**Challenges for the Students:**
1.  **The Mining Loop:** Create a `while` loop where the user can type "Mine". Every time they mine, add a random item (Wood, Cobblestone, or Iron) to their inventory dictionary.
2.  **The Auto-Saver:** Ensure that every time an item is added, the `save.json` file is updated immediately.
3.  **The AI Boss Fight:** 
    - Open Antigravity Gemini.
    - Prompt: "I have a `save.json` file. Write the Python code to LOAD that file back into a dictionary named `my_items` using `json.load()`."

---

### 🏆 Milestone:
*Test your game: Mine 5 items, close the program, then reopen it. If those 5 items are still in your inventory, you’ve mastered Game Persistence!*

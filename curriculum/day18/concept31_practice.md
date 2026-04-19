# 🛠️ Concept 31 Practice: JSON Basics (The Universal Save)

### 🚀 The 20-Problem Challenge Menu
*Note: Make sure to `import json` before you start!*

#### 🟢 Group A: The Data Strippers (Warmups)
1.  **Dict to String:** Use `json.dumps()` to turn a dictionary into a string.
2.  **String to Dict:** Use `json.loads()` to turn a JSON string back into a dictionary.
3.  **The Pretty Print:** Use `json.dumps(data, indent=4)` to make your data look professional.
4.  **Save a List:** Turn a list of strings into a JSON string and print it.
5.  **Save a Number:** Turn a single number into a JSON string.

#### 🟡 Group B: The File Manager
6.  **The High Score Save:** Save a `{"score": 100}` dictionary into a file called `save.json`.
7.  **The Hero Load:** Read `save.json` and print the score inside.
8.  **The Settings Chip:** Create a dictionary of 3 app settings and save it as JSON.
9.  **The Multi-Save:** Save a list of 5 usernames into a JSON file.
10. **The Update:** Load a JSON file, change the `health` value to 50, and save it back!

#### 🔴 Group C: The Bug Squasher (Fix the Data)
11. **The Missing Import:** Trying to use `json.dumps()` without the library.
12. **Single Quote Trap:** Writing a JSON string manually with `' '` (Fix it—needs `"`!).
13. **The Logic Error:** Trying to `.dumps()` a function (You can only save data, not code!).
14. **The Path Error:** Trying to load a `.json` file that doesn't exist.
15. **The Parse Error:** Trying to `json.loads()` a string that isn't a valid dictionary.

#### 💎 Group D: The AI Whisperer (Gemini Missions)
16. **The Game Architect:** Ask Gemini: "Write a JSON structure for a 'Minecraft' player that includes an inventory list and a current coordinate tuple."
17. **The Web Developer:** Ask Gemini: "How do websites use JSON to send messages between a front-end and a back-end?"
18. **The Storage Pro:** Ask Gemini: "What is the difference between `json.dump()` and `json.dumps()`? (Hint: The 's' stands for string!)."
19. **The Real-World Modeler:** Ask Gemini: "Write a Python script that loads a list of products from a JSON file and prints the ones that cost less than $10."
20. **The Challenge:** Ask Gemini: "Give me a hard Python challenge involving a nested JSON object with at least 3 levels of depth!"

---

### 🌟 Stretch Goal for "Flash" Students
Build a **"Loot Bag Saver"**! 
1. Create a dictionary with a `player_name` and a list called `items`.
2. Ask the user to add 3 items to the bag.
3. Save the whole dictionary to `inventory.json`.
4. Close the program and run it again.
5. **Load** the JSON and print the items. Did they stay?
 Riverside

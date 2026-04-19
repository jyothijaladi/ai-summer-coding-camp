# 🛠️ Concept 28 Practice: Saving the Game (Writing Files)

### 🚀 The 20-Problem Challenge Menu
*Teachers: This is the first time their code will leave a "Trace" on the computer!*

#### 🟢 Group A: The File Builders (Warmups)
1.  **Hello File:** Open `test.txt` in `"w"` mode and write "Hello!".
2.  **Name Saver:** Ask for the user's name and write it into `users.txt`.
3.  **The Append:** Open `test.txt` in `"a"` mode and add "How are you?".
4.  **Number Dump:** Write the number 100 into a file (Don't forget the `str()`!).
5.  **Multi-Line:** Use `\n` to write three different names on three different lines.

#### 🟡 Group B: The Game Log Manager
6.  **The Scoreboard:** Write a global `score` variable to `high_score.txt`.
7.  **The Inventory Save:** Join a list of items into one string and save it to `items.txt`.
8.  **The Battle Log:** Write "Player hit monster" to a log file.
9.  **The Settings Chip:** Save a dictionary of settings as a string into `config.txt`.
10. **The Achievement:** Write 5 random achievement names into a file using a loop.

#### 🔴 Group C: The Bug Squasher (Fix the Save)
11. **The Missing Mode:** `open("test.txt")` with no `"w"` or `"a"` (What happens? Hint: It defaults to READ mode!).
12. **The String Trap:** `f.write(500)` (Fix the error—numbers must be strings!).
13. **The Unclosed File:** Opening a file without `with` and forgetting to `.close()` it.
14. **The Overwrite Catastrophe:** Accidentally using `"w"` when you wanted to `"a"`.
15. **Path Not Found:** Trying to write to a folder that doesn't exist.

#### 💎 Group D: The AI Whisperer (Gemini Missions)
16. **The Story Save:** Ask Gemini: "Write a short Python script that takes a 3-page story and saves each page as a different text file."
17. **The CSV Guru:** Ask Gemini: "How do I save data so it can be opened in **Excel**? (Hint: The `.csv` format)."
18. **The System Pro:** Ask Gemini: "What is the difference between writing a `.txt` file and a `.json` file in Python?"
19. **The Real-World Modeler:** Ask Gemini: "Write the code for a 'Game Save' system that remembers the player's level, health, and location."
20. **The Challenge:** Ask Gemini: "Give me a challenge that uses a `for` loop to write the first 100 multiplication tables into a text file!"

---

### 🌟 Stretch Goal for "Flash" Students
Build a **"Diary App"**! 
1. Ask the user for the "Date."
2. Ask for their "Daily Thoughts."
3. Open a file named `diary.txt` in `"a"` mode.
4. Write the date and the thoughts with a nice separator between them.
5. *Bonus:* Add a function that adds a timestamp automatically!
 Riverside

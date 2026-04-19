# 🛠️ Concept 29 Practice: Loading the High Score (Reading Files)

### 🚀 The 20-Problem Challenge Menu
*Note: You must have a file already saved to practice reading it!*

#### 🟢 Group A: The First Readers (Warmups)
1.  **Read the Message:** Open `test.txt` and print everything inside it.
2.  **The Single Line:** Read only the first line of a file using `.readline()`.
3.  **The List Load:** Use `.readlines()` to turn every line of a file into a List.
4.  **Count the Characters:** Print how many letters are in a text file.
5.  **Clean Print:** Read a file and use `.strip()` to remove the extra spaces.

#### 🟡 Group B: The Game Data Loader
6.  **Load the Score:** Read a file named `score.txt` and turn it into an integer.
7.  **The Hero Finder:** Read a `names.txt` file and print "Welcome back, [Name]".
8.  **The Inventory Load:** Read a file of items and use `.split(",")` to turn them back into a Python List.
9.  **The Map Loader:** Print "Loading Map..." and then display the contents of `map.txt`.
10. **The Achievement Check:** Read an `earned.txt` file and print each achievement with a "✅" next to it.

#### 🔴 Group C: The Bug Squasher (Fix the Load)
11. **The Ghost File:** Trying to read `missing.txt` (Fix it with a `try/except` block!).
12. **The Newline Mess:** Printing lines from a file and seeing extra blank lines in between. (Fix it with `.strip()`!).
13. **The Variable Mistake:** `data = f.read` (Fix the missing parentheses `()`!).
14. **The Type Trap:** Trying to add `10` to a value you just read from a file. (Fix the `int()` conversion!).
15. **The Mode Mismatch:** Trying to `f.write()` inside a file opened with `"r"` mode.

#### 💎 Group D: The AI Whisperer (Gemini Missions)
16. **The Log Summarizer:** Ask Gemini: "Write a script that reads a 50rd log file and counts how many times the word 'ERROR' appears."
17. **The JSON Loader:** Ask Gemini: "How do I use the `json` library to read a dictionary from a file?"
18. **The Iterator:** Ask Gemini: "How do I use a `for` loop to read a file one line at a time instead of loading the whole thing at once?"
19. **The Real-World Modeler:** Ask Gemini: "Write a Python script that reads a 'Config' file and updates the game variables automatically."
20. **The Challenge:** Ask Gemini: "Give me a challenge where I have to read a file and print the lines of the file in BACKWARDS order!"

---

### 🌟 Stretch Goal for "Flash" Students
Build a **"High Score Board"**! 
1. Create a function `save_score(s)` and `load_score()`.
2. Ask the user for their score.
3. Call `load_score()` to see the current record.
4. **IF** the new score is higher, call `save_score()` to update the file!
5. Print a celebratory message if they beat the record!
 Riverside

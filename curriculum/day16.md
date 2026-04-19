# 💾 Day 16: Digital Memory (Files)

**Time:** 9:00 AM - 12:00 PM
**Daily Goal:** Learn how to save data into a `.txt` file so your program "remembers" it forever.

---

## 🕒 9:00 AM – 9:40 AM: Concept 1 – Writing to a File ✏️
*How to create a digital note.*

1.  **The `with open` Magic:** 
    - Explain that this is the safest way to open a file.
    - `with open("note.txt", "w") as file: file.write("Hello Computer!")`
    - `"w"` stands for **Write** (Warning: This wipes out the old file!).
2.  **Appending Info:**
    - Use `"a"` to **Append** (Add to the end) instead of overwriting.
3.  **The AI Connection:**
    - Ask Gemini: "What is the difference between writing 'w' and appending 'a' in Python? Give me a real-world example."

---

## 🕒 9:40 AM – 10:00 AM: 🍎 Brain Break (20 mins)

---

## 🕒 10:00 AM – 10:40 AM: Concept 2 – Reading from a File 📖
*How to load your saved secrets.*

1.  **Reading Content:**
    - `with open("note.txt", "r") as file: content = file.read()`
    - `"r"` stands for **Read**.
2.  **Safety First:**
    - Remind them to use `try/except` just in case the file doesn't exist yet!
3.  **The AI Connection:**
    - Task: Ask Gemini: "Write a short Python script that opens a file called 'diary.txt' and prints every line one by one using a `for` loop."

---

## 🕒 10:40 AM – 11:00 AM: 🥤 Mini-Break / Buffer

---

## 🕒 11:00 AM – 12:00 PM: 🏝️ The Sandbox Exploration
*Goal: Build a "Secret Messenger".*

**Challenges for the Students:**
1.  **The Message Sender:** Use `input()` to ask the user for a secret message and save it to `secret.txt`.
2.  **The Message Receiver:** Write a second script (or function) that reads `secret.txt` and prints: "You have a new message: [message]".
3.  **The AI Boss Fight:** 
    - Open Antigravity Gemini.
    - Prompt: "I want to save a list of 3 names to a file called 'friends.txt'. How do I use a `for` loop to write each name on a new line?"

---

### 💡 Teacher's Tip:
*If a student says 'I don't see my file!', tell them to look in the same folder where their Python script is. The `.txt` file will appear right next to it!*

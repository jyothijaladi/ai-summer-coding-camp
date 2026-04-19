# 🏆 Week 1 Hero Project: The AI Escape Room 🔐

**Goal:** Combine EVERYTHING from Week 1 (Print, Variables, Math, Strings, Input, and Booleans) to build a multi-room "Escape" game where the player must solve puzzles to win!

---

### 📋 The Mission
You are trapped in a high-tech "Digital Vault." To get out, you must interact with the computer's logic and solve three security challenges.

### 🛠️ Step 1: The Lobby (Setup & Input)
1. Ask the player for their name.
2. Create a variable `has_key = False`.
3. Print a welcome message: "Welcome {name} to the Vault!"

### 🛠️ Step 2: Challenge 1 – The Number Lock (Math)
The vault door needs a code. 
1. Ask the user: "What is 15 multiplied by 3?"
2. Check if their answer is `45`.
3. If they get it right, set `has_key = True`!

### 🛠️ Step 3: Challenge 2 – The Name Guess (Strings)
The "Sentinel AI" wants to know a secret word.
1. The AI says: "I am a language that slithers... what am I?"
2. Take user input.
3. If they say "Python", they pass!

### 🛠️ Step 4: The Final Door (Booleans & Logic)
1. Check the `has_key` variable.
2. **IF** `has_key == True`, print "ACCESS GRANTED! YOU ESCAPED!"
3. **ELSE**, print "The alarm sounds... GAME OVER."

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "I am finishing my Week 1 Escape Room game. Can you help me write an 'AI Antagonist' persona? Give me 3 spooky lines I can print if the player gets a question wrong!"

### 🌟 The "Real World" Mission
Add a **"Battery Meter"**.
Start with `energy = 100`. Every time the player makes a guess, subtract 10. If `energy` hits 0, they lose!
*This is how professional mobile games keep players on their toes!*

---

### 🕵️ Why are we doing this?
This project is a perfect simulation of **User Interaction Loops**.
When you play a game like **Among Us**, the code is doing exactly this:
- Waiting for input (The Task).
- Checking a condition (Is the task Done?).
- Changing a state (Is the Impostor winning?).
**You just built your first functional game engine!**

# 🔄 Day 9: The "While" Loop (Infinite Control)

**Time:** 9:00 AM - 12:00 PM
**Daily Goal:** Learn how to create loops that run as long as a condition is True.

---

## 🕒 9:00 AM – 9:40 AM: Concept 1 – The "While" Loop 🔄
*Looping until something stops you.*

1.  **The `while` Loop:** 
    - `while condition: do something`
    - Explain that this is like a repetitive `if` statement. It checks the condition, runs the code, and then checks the condition *again*.
2.  **Infinite Loops (The Danger Zone!):**
    - Show what happens when a loop has no end. (How to stop it: `Ctrl+C`).
    - *Example:* `while True: print("I'm stuck!")`
3.  **The AI Connection:**
    - Ask Gemini: "What is the main difference between a `for` loop and a `while` loop? Explain it using a video game example."

---

## 🕒 9:40 AM – 10:00 AM: 🍎 Brain Break (20 mins)

---

## 🕒 10:00 AM – 10:40 AM: Concept 2 – Breaking the Loop (`break`) 🛑
*The Emergency Exit.*

1.  **The `break` Statement:**
    - Use `break` to stop a loop immediately, even if the condition is still True.
    - *Example:* A loop that runs forever until the user types "quit".
2.  **User-Driven Loops:**
    - Use `while True` + `input()` + `if` + `break` to make interactive programs.
3.  **The AI Connection:**
    - Task: Ask Gemini: "Write a `while` loop that asks the user for their favorite color and only stops (breaks) if they type 'Rainbow'."

---

## 🕒 10:40 AM – 11:00 AM: 🥤 Mini-Break / Buffer

---

## 🕒 11:00 AM – 12:00 PM: 🏝️ The Sandbox Exploration
*Goal: Build a "Number Guessing Game".*

**Challenges for the Students:**
1.  **The Password Wall:** Create a `while` loop that asks for a password. It should keep asking until the user gets it right.
2.  **The Countdown Timer:** Set a variable `timer = 10`. Use a `while` loop to print the timer and subtract 1 each time until it hits 0.
3.  **The AI Boss Fight:** 
    - Open Antigravity Gemini.
    - Prompt: "I am making a game where a player is fighting a monster. The monster has 100 health. Write a `while` loop where the user types 'attack' to subtract 10 health from the monster. The loop should stop when health reaches 0."

---

### 💡 Teacher's Tip:
*"While" loops are where logic errors happen most. If the loop doesn't run, check the initial condition. If the loop never stops, check if you are updating the variable inside the loop! (e.g., `count = count + 1`)*

# 🏆 Day 15: Error Handling & The Boss Battle RPG

**Time:** 9:00 AM - 12:00 PM
**Daily Goal:** Learn how to stop your code from crashing (Error Handling) and build your first complex gaming system!

---

## 🕒 9:00 AM – 9:40 AM: Concept – Error Handling (`try/except`) 🐛
*Making your code "bulletproof" (or at least kid-proof).*

1.  **What is a Crash?** 
    - Show what happens when you try to convert "Pizza" into an integer. It CRASHES.
2.  **The Safety Net (`try` / `except`):**
    - Explain that `try` is like saying: "Hey Python, try to do this, but if you fail, don't scream at me!"
    ```python
    try:
        age = int(input("Enter your age: "))
    except:
        print("That's not a number! Putting 10 as default.")
    ```
3.  **The AI Connection:**
    - Ask Gemini: "Why do professional games use 'Try/Except'? Give me an example related to an internet connection."

---

## 🕒 9:40 AM – 10:00 AM: 🍎 Brain Break (20 mins)

---

## 🕒 10:00 AM – 12:00 PM: 🏆 FRIDAY HERO PROJECT: The Boss Battle RPG 🎮
*Goal: Build a turn-based combat game against a legendary Boss!*

### The Project Blueprint:
1.  **The Boss Dictionary:** Create a dictionary called `boss` with `name`, `hp` (200), and `attack` (15).
2.  **The Special Attacks (Functions):**
    - `slash(damage)`: A normal attack.
    - `heal(hp)`: A function that adds random health back to the player.
    - `ult(charge)`: An ultimate attack that only works if luck is on your side!
3.  **The Game Loop:** Use a `while` loop that runs as long as BOTH the player and the boss have HP above 0.
4.  **Error Handling:** Use `try/except` to make sure the game doesn't crash if the user accidentally types a letter instead of an attack number.
5.  **The AI Advantage:**
    - **Boss Quotes:** Ask Gemini: "I have a boss named 'The Cyber Dragon'. Give me 3 trash-talk lines he can say during the fight."
    - **Logic Check:** Ask Gemini: "How do I make a 20% chance for the boss to CRITICALLY hit the player for double damage?"

---

### 🏆 Milestone:
*Students who finish their Boss Battle can add a "Victory Speech" that uses the player's name and their remaining HP to congratulate them!*

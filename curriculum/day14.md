# 🧞 Day 14: Scope & The "Luck" Library

**Time:** 9:00 AM - 12:00 PM
**Daily Goal:** Learn about where variables live (Scope) and how to add randomness to your games using the `random` library.

---

## 🕒 9:00 AM – 9:40 AM: Concept 1 – Scope (Where does your Variable live?) 🧞
*A variable in a function is like a secret inside a house.*

1.  **Local Variables:** 
    - Variables created inside a function stay inside that function. The "Outside" world can't see them.
2.  **Global Variables:**
    - Variables created at the very top of your file can be seen by everyone.
3.  **The AI Connection:**
    - Ask Gemini: "What happens if I have a variable `x = 10` outside a function and another `x = 5` inside a function? Which one will Python use inside the function?"

---

## 🕒 9:40 AM – 10:00 AM: 🍎 Brain Break (20 mins)

---

## 🕒 10:00 AM – 10:40 AM: Concept 2 – Adding "Luck" (`random`) 🎲
*How to make games unpredictable.*

1.  **Importing Libraries:**
    - Explain that libraries are "Expansion Packs" for Python.
    - `import random`
2.  **Useful Commands:**
    - `random.randint(1, 6)` -> Rolls a 6-sided die.
    - `random.choice(list)` -> Picks a random item from a list (like a loot box!).
3.  **The AI Connection:**
    - Task: Ask Gemini: "How do I use the `random` library to pick a random winner from a list of 10 people?"

---

## 🕒 10:40 AM – 11:00 AM: 🥤 Mini-Break / Buffer

---

## 🕒 11:00 AM – 12:00 PM: 🏝️ The Sandbox Exploration
*Goal: Build a "Loot Drop Simulator".*

**Challenges for the Students:**
1.  **The Dice Roller:** Write a function called `roll_die()` that returns a random number between 1 and 20.
2.  **The Magic Bag:** Create a list of 5 items (Common, Rare, Legendary). Write a loop that picks a random item from the list 5 times.
3.  **The AI Boss Fight:** 
    - Open Antigravity Gemini.
    - Prompt: "I am making a game. I need a function that has a 50% chance of returning 'Heads' and a 50% chance of returning 'Tails'. Help me write it using `random.choice`."

---

### 💡 Teacher's Tip:
*Randomness is what makes coding fun for kids. Encourage them to use `random.randint` for everything today—damage, colors, names, everything! It makes the "Sandbox" time feel much more like a real game.*

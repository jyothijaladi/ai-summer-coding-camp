# 🛍️ Day 7: Lists & Their Frozen Cousins (Tuples)

**Time:** 9:00 AM - 12:00 PM
**Daily Goal:** Learn how to store collections of items and the difference between "Mutable" (Changeable) and "Immutable" (Unchangeable) data.

---

## 🕒 9:00 AM – 9:40 AM: Concept 1 – The Power of Lists 🛍️
*One variable, many items.*

1.  **Creating a List:** 
    - `inventory = ["Sword", "Shield", "Potion"]`
2.  **Accessing Items (Indexing):**
    - Explain that Python starts counting at **0**.
    - `inventory[0]` is the Sword!
3.  **The AI Connection:**
    - Ask Gemini: "I have a list of names. How do I print the very last name in the list, even if I don't know how long the list is?" (Introduce negative indexing: `[-1]`).

---

## 🕒 9:40 AM – 10:00 AM: 🍎 Brain Break (20 mins)

---

## 🕒 10:00 AM – 10:40 AM: Concept 2 – Unchangeable Tuples 🧊
*The "Frozen" List.*

1.  **What is a Tuple?**
    - It uses parentheses `()` instead of square brackets `[]`.
    - Once you make it, you **cannot** change it. No `append`, no `remove`.
2.  **Why use them?**
    - For things that should *never* change, like the Coordinates of a city or the RGB color of a pixel.
3.  **The AI Connection:**
    - Task: Ask Gemini: "What happens if I try to change an item in a Tuple? Write a code snippet that shows the error."

---

## 🕒 10:40 AM – 11:00 AM: 🥤 Mini-Break / Buffer

---

## 🕒 11:00 AM – 12:00 PM: 🏝️ The Sandbox Exploration
*Goal: Build an "RPG Inventory System".*

**Challenges for the Students:**
1.  **The Loot Box:** Create a list named `loot`. Add three items to it. Use `.append()` to add a "Magic Ring" at the end.
2.  **The Forbidden Scroll:** Create a tuple named `secret_coordinates` with two numbers. Try to change one of them and see the computer complain! 
3.  **The AI Boss Fight:** 
    - Open Antigravity Gemini.
    - Prompt: "I have a list `colors = ['red', 'blue', 'green']`. Write a line of code that replaces 'blue' with 'yellow'."

---

### 💡 Teacher's Tip:
*Indexing is the most confusing part of Day 7. Use a physical row of boxes or chairs to show why the first one is '0'. "Think of it as the number of steps away from the start!"*

# 📥 Day 13: Inputs & Outputs (Parameters)

**Time:** 9:00 AM - 12:00 PM
**Daily Goal:** Learn how to send information INTO a function and get an answer BACK from it.

---

## 🕒 9:00 AM – 9:40 AM: Concept 1 – Parameters (Giving the Machine Info) 📥
*A juice press needs fruit to make juice. A function needs "Parameters" to do work.*

1.  **Adding Parameters:** 
    - `def greet(name): print(f"Hello {name}!")`
    - Explain that `name` is a placeholder for whatever information we send in.
2.  **Multiple Parameters:**
    - `def add_points(score, bonus): print(score + bonus)`
3.  **The AI Connection:**
    - Ask Gemini: "I have a function `def multiply(a, b):`. How do I call this function to multiply 5 and 10?"

---

## 🕒 9:40 AM – 10:00 AM: 🍎 Brain Break (20 mins)

---

## 🕒 10:00 AM – 10:40 AM: Concept 2 – Return Values (Getting Answers) 📤
*The "Answer Slot" of the machine.*

1.  **The `return` Keyword:**
    - Explain that `print()` only shows an answer on the screen, but `return` gives the answer back to the rest of the program so we can use it later.
    - *Example:* `def double(x): return x * 2` -> `my_number = double(5)` (Now `my_number` is 10!).
2.  **Printing vs Returning:**
    - Use the "Waitress analogy": Print is the waitress shouting the order, Return is the waitress bringing the plate of food to your table.
3.  **The AI Connection:**
    - Task: Ask Gemini: "Write a function that takes two numbers and *returns* the larger one."

---

## 🕒 10:40 AM – 11:00 AM: 🥤 Mini-Break / Buffer

---

## 🕒 11:00 AM – 12:00 PM: 🏝️ The Sandbox Exploration
*Goal: Build a "Stats Calculator".*

**Challenges for the Students:**
1.  **The Age Calculator:** Write a function that takes `birth_year` and *returns* how old that person is.
2.  **The Weapon Power-UP:** Write a function called `power_up(damage, multiplier)`. It should return the new damage value.
3.  **The AI Boss Fight:** 
    - Open Antigravity Gemini.
    - Prompt: "Write a Python function that takes a list of numbers and returns the sum of all the numbers. Don't forget to use the `return` keyword!"

---

### 💡 Teacher's Tip:
*The difference between `print` and `return` is the hardest concept in Week 3. If a student says "I returned the value but nothing appeared on the screen!", explain that they now need to `print()` the result of the function call.*

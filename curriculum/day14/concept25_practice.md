# 🛠️ Concept 25 Practice: The Secret Room (Scope)

### 🚀 The 20-Problem Challenge Menu
*Teachers: This is where we learn the rules of "Variable Privacy"!*

#### 🟢 Group A: The Scope Detective (Warmups)
1.  **Inside vs Outside:** Define `x = 10` outside and `y = 5` inside a function. Print both.
2.  **The Ghost Variable:** Try to print a local variable outside its function. (Watch it fail!).
3.  **The Global View:** Create a global `name` and print it from inside a function.
4.  **Local Mastery:** Define a function that creates a variable `msg` and prints it.
5.  **Triple Lock:** Create three functions, each with a local variable named `data`. Do they crash? (No! They are in different rooms!).

#### 🟡 Group B: The Global Gearbox
6.  **The Score Adder:** Use the `global` keyword to add 10 points to a global `score` from inside a function.
7.  **The Name Changer:** Use `global` to update a `player_name` variable.
8.  **The Status Switch:** Use `global` to change `is_playing` to `False`.
9.  **The Shared List:** Create a global list and `.append()` to it from inside a function. (Hint: You don't need `global` for lists!).
10. **The Counter:** Use a function to increment a global `visit_count` every time it’s called.

#### 🔴 Group C: The Bug Squasher (Fix the Privacy)
11. **The Shadow Error:** `x = 5` outside, `x = 10` inside (Why doesn't the outside `x` change? Fix it!).
12. **The Defined Later:** Using a global variable before it has been created at the top.
13. **Missing Global:** Trying to do `score += 1` inside a function without the `global` keyword.
14. **The Indent Trap:** A local variable that isn't indented properly.
15. **The Spelling Error:** `globall score` (Fix the typo!).

#### 💎 Group D: The AI Whisperer (Gemini Missions)
16. **The Storyteller:** Ask Gemini: "Write a short Python example showing the difference between a Global and a Local variable using a 'Bank' analogy."
17. **The Security Guard:** Ask Gemini: "Why is it dangerous to make EVERY variable global in a big program?"
18. **The Parameter Link:** Ask Gemini: "Are function parameters (like `def hi(name)`) local or global variables?"
19. **The Real-World Modeler:** Ask Gemini: "How does a website like Facebook keep your 'User ID' global but your 'Temporary Draft Post' local?"
20. **The Challenge:** Ask Gemini: "Give me a 'Scope Mystery' puzzle where I have to guess which variable will be printed!"

---

### 🌟 Stretch Goal for "Flash" Students
Build a **"Multi-Level Power System"**! 
1. Create a global `total_power = 100`.
2. Define a function `use_battery()` that subtracts 10 locally but doesn't change the global total.
3. Define a function `emergency_system()` that uses the `global` keyword to subtract 50 from the total.
4. Print the `total_power` after calling both functions!
 Riverside

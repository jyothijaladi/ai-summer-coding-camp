# 🛠️ Concept 11 Practice: The Logic Maze

### 🚀 The 20-Problem Challenge Menu
*Teachers: Watch out for the "Double Indent" (8 spaces) today!*

#### 🟢 Group A: The Step-by-Step (Warmups)
1.  **The Double Shield:** If `has_power` is True, then inside check if `is_shield_on` is True.
2.  **The Safe House:** If `at_home` is True, then inside check if `is_door_locked` is False.
3.  **The Water Check:** If `glass_empty` is False, then check if `is_water` is True.
4.  **The Code Duo:** If `x > 0`, then check if `x < 10`.
5.  **The Identity Check:** Check if `name == "Alex"`, then check if `age == 12`.

#### 🟡 Group B: The Multi-Step App Logic
6.  **The Cinema:** If `has_ticket`, then check if `is_over_13`.
7.  **The Bank:** If `card_valid`, then check if `pin_match`.
8.  **The Art Studio:** If `has_paper`, then check if `has_pencil`.
9.  **The Rocket:** If `fuel_full`, then check if `engines_on`.
10. **The Library:** If `is_member`, then check if `has_late_fine == False`.

#### 🔴 Group C: The Bug Squasher (Fix the Stairs)
11. **The Flat Nest:** 
    ```python
    if x > 5:
    if y > 5: # Fix the indent!
    print("Both high!")
    ```
12. **The Missing Path:** An `if` inside an `if` that has no `print` message.
13. **The Colon Master:** Check if colons are missing on the second `if`.
14. **The Variable Ghost:** A nested `if` checking a variable that was never created.
15. **The Logic Loop:** A nested `if` that checks the exact same thing as the first `if` (Pointless!).

#### 💎 Group D: The AI Whisperer (Gemini Missions)
16. **The Story Maze:** Ask Gemini: "Write a nested `if` script where look inside a box, and *then* look inside a secret compartment."
17. **The Security Guard:** Ask Gemini: "Write a nested logic check for a 2-factor authentication system."
18. **The Code Cleaner:** Ask Gemini: "When should I use a nested `if` and when should I combine them into one line using `and`?"
19. **The Real-World Modeler:** Ask Gemini: "How does a car's computer check if 1) a person is in the seat and 2) the seatbelt is buckled before it stops beeping?"
20. **The Challenge:** Ask Gemini: "Give me a 3-layer nested `if` challenge for a master coder!"

---

### 🌟 Stretch Goal for "Flash" Students
Build a **"Treasure Hunter"** quest! 
1. Ask the user if they want to enter the cave.
2. **If Yes:** Ask if they want to light a torch.
3. **If Yes:** Ask if they want to open the chest.
4. **Each step MUST be nested.** If they say "No" at any point, the game ends immediately!

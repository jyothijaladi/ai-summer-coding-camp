# 🏆 Day 13 Level Up Challenge: The RPG Combat Engine ⚔️

**Goal:** Use Parameters to send power levels and Return Values to calculate damage in a real-time battle.

---

### 📋 The Mission
You are the lead programmer for a new "Dungeon Crawler" game. You need to build a modular combat engine that can calculate hits and update the hero's health!

### 🛠️ Step 1: The Damage Machine
Define a function named `calculate_damage(base_power, critical_hit)`.
- If `critical_hit` is `True`, return `base_power * 2`.
- Else, return just the `base_power`.

### 🛠️ Step 2: The Action
Create a `while True:` loop for your battle.
1. Ask the user: "Attack now? [Yes/No]"
2. If "Yes", call `calculate_damage(20, True)`. 
3. "Catch" the result in a variable named `final_hit`.

### 🛠️ Step 3: The Result
1. Create a `monster_hp = 100`.
2. Subtract your `final_hit` from the monster's HP.
3. Print: `f"The monster takes {final_hit} damage! It has {monster_hp} left."`

### 🛠️ Step 4: The Win Check
If `monster_hp <= 0`, print "VICTORY!" and `break` the loop.

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "I am building a combat engine. How do I make the `critical_hit` parameter **Random** (so sometimes it is True and sometimes it is False)?"

### 🌟 The "Real World" Mission
Imagine you are building **PayPal**. 
Define a function called `convert_to_euro(dollars)`. 
- Take the `dollars` as a parameter.
- Multiply by `0.9` (the exchange rate).
- **Return** the new amount.
*This is exactly how global apps handle different currencies!*

---

### 🕵️ Why are we doing this?
In the professional world, this is called **"Modular Programming."** 
When you play **Fortnite**, there is a "Damage Function" that handles every bullet shot in the game. It takes the weapon type as a parameter and returns the damage numbers you see on the screen. You just built the core logic of a world-class game engine!

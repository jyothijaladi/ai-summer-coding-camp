# 🏆 Week 3 Hero Project: The Boss Battle RPG 🐉

**Goal:** Create a professional, turn-based RPG battle that uses Functions, Parameters, Randomness, and Error Handling to build a "Boss Fight" experience.

---

### 📋 The Mission
You must defeat the "Binary Beasty" to protect the world. You’ll need a menu, special attacks, and a combat engine that won't crash if the player makes a mistake.

### 🛠️ Step 1: The Engine (Functions)
Define three functions:
1. `player_attack(power)`: Roll a random number between 1 and `power`. Return the result.
2. `boss_attack()`: Roll a random number between 10 and 30. Return the result.
3. `show_stats(p_hp, b_hp)`: Use an f-string to show both health bars nicely.

### 🛠️ Step 2: The Setup
1. `import random`
2. Set `player_hp = 100` and `boss_hp = 200`.

### 🛠️ Step 3: The Main Loop (Gameplay)
Create a `while player_hp > 0 and boss_hp > 0:` loop.
1. Ask the user: "Attack? [1] Light [2] Mega [3] Quit"
2. **USE A TRY BLOCK!** Catch any errors if the user types a letter instead of a number.

### 🛠️ Step 4: The Logic
- **IF 1:** Call `player_attack(20)`. Subtract from `boss_hp`.
- **IF 2:** Call `player_attack(60)`. HOWEVER—Mega attack has a 50% chance to fail! Use `random.random()` to check.
- **IF 3:** `break` the game.

### 🛠️ Step 5: The Counter & Win
1. Boss attacks the player.
2. If `player_hp <= 0`, print "DEFEAT! Binary Beasty wins."
3. If `boss_hp <= 0`, print "VICTORY! You saved the day!"

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "I am building an RPG. How do I add a 'Healing Potion' function that can be used only 3 times per battle? Use a local variable to track the uses!"

### 🌟 The "Real World" Mission
Add a **"Battle Log"** List.
Every time someone takes damage, `.append()` the event to the log. At the end, use a `for` loop to print the full history of the fight!
*This is how professional games like **Pokémon** or **Slay the Spire** track your journey!*

---

### 🕵️ Why are we doing this?
In the professional world, this is a **"Feature Complete" Project.** 
You just combined logic, data, randomness, and security (errors) into one working app. This is the exact same structure used to build massive games like **Elden Ring** or **Zelda**. You are now a System Designer!

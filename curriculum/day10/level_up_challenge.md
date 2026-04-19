# 🏆 Week 2 Hero Project: The Virtual AI Pet (Tamagotchi) 👾

**Goal:** Combine Loops, Lists, Comparisons, and AI to build a living digital pet that grows, eats, and plays based on your commands.

---

### 📋 The Mission
You are the developer of a new "Mobile Pet" app. You need to build a loop that keeps your pet "Alive" and updates its stats every second.

### 🛠️ Step 1: The Pet Stats
Create a dictionary (or a set of variables) for:
- `pet_name`
- `hunger = 50` (0 is full, 100 is starving)
- `happiness = 50` (100 is happy, 0 is sad)
- `is_alive = True`

### 🛠️ Step 2: The Action Menu
Create a `while is_alive:` loop. Every turn, ask the player:
"What do you want to do with {pet_name}? [Feed / Play / Check / Quit]"

### 🛠️ Step 3: The Logic (If/Else)
- **IF Feed:** Subtract 20 from `hunger`.
- **IF Play:** Add 20 to `happiness` but add 10 to `hunger`.
- **IF Check:** Print the current stats.
- **IF Quit:** Set `is_alive = False`.

### 🛠️ Step 4: The Time Tick
At the end of every loop, add 5 to `hunger`. 
**The Death Check:** `if hunger >= 100 or happiness <= 0:` set `is_alive = False` and print "Your pet ran away..."

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "I am building a Virtual Pet in Python. Can you design a simple ASCII art 'Cat' or 'Dog' that changes its face depending on if it is happy or sad? Give me the print lines to copy!"

### 🌟 The "Real World" Mission
Add an **"Activity Log"** List.
Every time you feed or play with the pet, `.append()` the action to a list called `pet_history`. When the game ends, use a `for` loop to print out everything you did today with your pet!

---

### 🕵️ Why are we doing this?
In the professional world, this is called a **"State Engine."** 
When you play **The Sims** or **Pet Simulator 99** on Roblox, the game is running a giant loop exactly like this one. It’s always checking: "Is the character hungry? Is the user clicking a button?" You just built the fundamental framework of a life-simulation game!

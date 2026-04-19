# 🏆 Day 16 Level Up Challenge: The Super-Save Terminal 💾

**Goal:** Use Writing and Reading to build a "Profile System" that remembers your name and high score even after the program closes.

---

### 📋 The Mission
You are the developer of a new console app. You want to make sure your users don't have to re-type their names every single time they play.

### 🛠️ Step 1: The Initial Check
1. Try to open `user_profile.txt` in `"r"` mode.
2. **If** the file exists, read the name and print "Welcome back, {name}!".
3. **Else** (use `try/except`), ask "What is your name?" and write it into the file.

### 🛠️ Step 2: The Score System
1. Create a `score` variable.
2. Every time the user types "Play", add 10 points.

### 🛠️ Step 3: The Auto-Save
1. When the user types "Quit":
2. Open `status.txt` in `"w"` mode.
3. Write the current `score` into the file.
4. Print "Progress Saved. Goodbye!"

### 🛠️ Step 4: The Verification
Launch your program again. Does it remember your name? Look in your folder—can you see the `.txt` files? Open them with your notepad and see what you wrote!

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "I am building a save system in Python. How do I use the `os.path.exists()` function to check if a file is already there before I try to read it?"

### 🌟 The "Real World" Mission
Create a **"Cheat Code"** file. 
Place a secret word like "KA-ME-HA-ME-HA" inside a text file named `secrets.txt`. 
In your main game, read that file. If the player types the word they found in the file, give them 1,000,000 points!
*This is how professional game testers used to 'hack' games to find bugs!*

---

### 🕵️ Why are we doing this?
In the professional world, this is called **"Persistence."** 
Without persistence, the internet wouldn't exist. **Amazon** wouldn't remember your cart, **V-Bucks** would disappear every time you logged out, and **Messages** would vanish. You just mastered the technology that allows computers to "Remember" the human world!

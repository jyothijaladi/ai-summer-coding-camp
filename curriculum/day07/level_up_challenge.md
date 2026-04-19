# 🏆 Day 7 Level Up Challenge: The Voyager’s Log 🚀

**Goal:** Master the difference between flexible Lists and fixed Tuples by building a travel tracking program.

---

### 📋 The Mission
You are an explorer traveling between planets. You need to keep track of where you’ve been (A flexible list) and the exact coordinates of your home base (A fixed tuple).

### 🛠️ Step 1: The Home Base
Create a **Tuple** named `home_base` that stores two numbers: your Home Longitude and Latitude. (Example: `(45, -12)`).

### 🛠️ Step 2: The Travel List
Create a **List** named `planets_visited` that starts with one planet: `"Earth"`.

### 🛠️ Step 3: The Journey
1. Use `input()` to ask the player: "What is the next planet you want to visit?"
2. `.append()` that planet to your `planets_visited` list.
3. Print the whole list with a cool message: `f"Our journey so far: {planets_visited}"`.

### 🛠️ Step 4: The Navigation Check
Use an f-string to shout: `f"Warning! Never forget your Home Base at {home_base}!"`

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "I have a list of planets visited. How do I print them out like a numbered list (1. Earth, 2. Mars)? Show me a simple code snippet!"

### 🌟 The "Real World" Mission
Add a **"Current Mission"** Tuple. It should hold: `("Find Water", "Planet X", 1000)`. 
Try to change the mission name to "Found Gold". 
*Watch the code fail!* Explain to your partner why a "Mission" should be a Tuple (because you can't just change the mission in the middle of a flight!).

---

### 🕵️ Why are we doing this?
In the professional world, this is called **"Data Integrity."** 
When you use a banking app, your **Account Balance** is a List/Variable (it changes). But your **Account Number** is a Tuple (it must NEVER change). You just learned how to keep important data safe from accidental changes!

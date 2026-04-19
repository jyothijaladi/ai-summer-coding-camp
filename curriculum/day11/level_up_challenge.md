# 🏆 Day 11 Level Up Challenge: The Ultimate Game Store 🏬

**Goal:** Use Dictionaries to store prices and Sets to keep track of unique customers.

---

### 📋 The Mission
You are opening a "Digital Game Store." You need to keep track of what you’re selling (Prices in a Dictionary) and who has visited your store (Unique names in a Set).

### 🛠️ Step 1: The Inventory
Create a **Dictionary** called `game_prices` with:
- "Minecraft": 20
- "Roblox_Card": 10
- "Fortnite_Skins": 15

### 🛠️ Step 2: The Visitor Log
Create an empty **Set** called `villagers`.

### 🛠️ Step 3: The Workday (The Loop)
1. Create a `while` loop that runs 3 times.
2. Ask for the visitor's name and `.add()` it to your `villagers` set.
3. Ask which game they want to buy.
4. Get the price from your `game_prices` dictionary and print: `f"That will be ${price}, {name}!"`

### 🛠️ Step 4: The Summary
At the end, print how many **unique** people visited your store using `len(villagers)`.

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "I have a dictionary of game prices. How do I use a `for` loop to print every game name AND its price in a nice list?"

### 🌟 The "Real World" Mission
Create a **"Discount Badge"** Set. 
Add "Premium" to it. Use an `if` statement to check: `if "Premium" in badges: price = price * 0.5`. 
*This is how professional stores like **Steam** or **PlayStation Store** calculate member discounts!*

---

### 🕵️ Why are we doing this?
In the professional world, this is called **"Database Interaction."** 
When you use **Amazon** or **eBay**, the site is constantly looking up your item in a Dictionary (The Catalog) and Checking your user ID against a Set (Who is logged in?). You just built the core logic of a multi-billion dollar e-commerce platform!

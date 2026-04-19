# 🏆 Day 19 Project: The AI Detective Agency 🕵️‍♂️

**Goal:** Use AI Prompting and Python Logic together to solve a "Mystery" and track down a digital criminal.

---

### 📋 The Mission
The "Code Burglar" has stolen the master password to the city! You are the lead detective. You must use Antigravity Gemini to analyze clues and write code to find the thief.

### 🛠️ Step 1: The Suspects (Data)
Create a list of dictionaries called `suspects`. 
Each suspect should have a `name`, a `shoe_size`, and a `favorite_food`.
- `suspects = [{"name": "Cyrus", "shoe": 10, "food": "Pizza"}, ...]`
*(Teachers: Let students ask Gemini to generate 5 complex suspects for them!)*

### 🛠️ Step 2: The Clue (AI Prompting)
Ask **Antigravity Gemini**:
> "I am a detective in a Python game. I found a clue: 'The thief left a footprint of size 12 and loves Pasta.' Based on my list of suspects [Paste your list], who is the thief?"

### 🛠️ Step 3: The Search Code
Don't just believe the AI! Write a `for` loop that searches through your `suspects` list and finds the person who matches the shoe size AND the food.

### 🛠️ Step 4: The Confrontation (Functions)
Define a function `arrest(name)`. 
1. The function should print: `f"STOP RIGHT THERE, {name.upper()}!"`
2. Save the arrest report to a file called `cases_closed.txt`.

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "Write a Python script that 'scrambles' a suspect's name by shuffling the letters. Then, I have to guess the name before I can arrest them!"

### 🌟 The "Real World" Mission
Imagine you are building **FBI Cyber-Tools**. 
Create a set of "Known Criminal IP Addresses." 
Use a `while` loop to monitor a mock "Network Log" (a list of numbers). 
**IF** a number in the log matches one in your "Criminal Set," call the `alert()` function!
*This is the exact logic used in real-world cybersecurity to catch hackers!*

---

### 🕵️ Why are we doing this?
In the professional world, this is called **"AI-Assisted Investigation."** 
When data scientists at companies like **Apple** or **Google** are looking for "Bugs" or "Security Holes," they use AI to scan millions of lines of data and find the one piece that doesn't fit. You just built a professional digital forensics tool!

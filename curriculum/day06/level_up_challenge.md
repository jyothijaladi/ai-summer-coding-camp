# 🏆 Day 6 Level Up Challenge: The Ultra-Security Terminal 🔐

**Goal:** Use nested checks and logical operators (`and`/`or`) to build a high-security login system for a secret lab.

---

### 📋 The Mission
You are the Security Engineer for "Area 52". You need to build a terminal that only lets in the right people based on three different checks.

### 🛠️ Step 1: The Identity Check
Ask the user for their `username`. 
- **IF** the name is "Admin" OR "Lead_Scientist", let them proceed to the next step.
- **ELSE**, print "Unknown User. System Locked."

### 🛠️ Step 2: The Two-Factor Check (Nested)
Inside the first "If," ask for a `pin_code`.
- **IF** the `pin_code` is "007" AND the `device_trusted` variable (create this!) is True, let them proceed.

### 🛠️ Step 3: The Emergency Override
Create an `emergency_override` variable and set it to `False`.
Modify your code so that if `emergency_override == True`, the system opens **immediately** regardless of the username or pin!

---

### 🌟 Ultra Mission for "Flash" Students
Ask **Antigravity Gemini**:
> "I am building a security terminal. Can you help me write a Python line that checks if a password is at least 8 characters long AND contains the number '1'?"

### 🌟 The "Real World" Mission
Add an **"Access Log"**.
Every time someone tries to login, print a message: `f"Attempt detected for {username} at {time}."` 
*This is how real servers track hackers and identify security breaches!*

---

### 🕵️ Why are we doing this?
In the professional world, this is called **"Authentication & Authorization."** 
When you log into **Discord** or **Gmail**, the computer is running these exact nested checks to make sure:
1. You exist.
2. Your password matches.
3. You are using a device you’ve used before.
**You just built the same logic that keeps the internet’s biggest secrets safe!**

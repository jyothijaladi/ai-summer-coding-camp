# 🧠 Week 2, Day 8: Agentic AI - Writing Tools for AI 🛠️

**Time:** 1 - 1.5 Hours  
**Goal:** Understand the core concept of "Agentic AI." How do we make AI actually DO things in the real world instead of just talking to us?

---

## 1. The Core Concept: Giving the Brain Hands 👐

Regular AI (like ChatGPT or basic Gemini) is just a Brain in a Jar. You ask it a question, and it talks back. It can't send an email, it can't turn on your smart lights, and it can't read your files.

**Agentic AI** means we write Python **Functions** (Tools) and we give the AI permission to use them! 
It's like giving the Brain a pair of Robot Hands. 

### How does this work? (Conceptual)
1. You write a function: `def turn_on_lights():`
2. You tell the AI: *"Hey Gemini, you are a smart house assistant. Here is a list of tools you are allowed to use: [turn_on_lights]"*
3. The user types: *"It's dark in here!"*
4. Gemini realizes it needs help, and replies to the Python code: *"Please run the `turn_on_lights` tool for me!"*
5. Python runs your function! 💡

### Let's mock up a "Tool"
For now, we will write a normal python function, but we will pretend it's a tool for our AI.

```python
# Our "Tool"
def get_current_weather(city_name):
    # (Imagine this connects to the real internet!)
    if city_name == "New York":
        return "Raining and 50 degrees"
    else:
        return "Sunny and 75 degrees"

# Giving the AI the tool's answer
weather_data = get_current_weather("New York")
prompt_for_ai = "Gemini, act like a pirate weather man. The data is: " + weather_data
print("Sending to AI:", prompt_for_ai)
```

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Can't Gemini just look up the weather itself?**
**A:** Huge AI models are "frozen" in time when they are trained. Even if they have search capabilities, they can't access *private* things. Gemini can't check if your Minecraft server is online unless you write a Python tool that checks the server and hands the data to Gemini!

**Q: Is it safe to let AI run my code?**
**A:** That is why WE write the functions! AI only gets to pick Which tool to run. If you don't write a `delete_all_files()` function, the AI can't delete your files!

---

## 3. The AI Connection: AI Writing Tools ✨

We can ask Gemini to write these Python tools for us!

**Prompt Gemini:** *"I am building an Agentic AI application. I need you to write a Python function (a tool) called `math_calculator(num1, num2, operation_name)` that can add, subtract, multiply, or divide based on the `operation_name` string. Make it return the answer."*

*(Copy the code Gemini gives you! You just built your first AI tool!)*

---

## 4. Hands-on Coding 💻

**Action 1:** The File Reader Dummy Tool Document 📄
Let's pretend we are building an AI that reads emails. Write a tool function that takes an `email_id` (a number) and returns a fake string representing the email body.
```python
def read_email_tool(email_id):
    if email_id == 1:
        return "Subject: Lunch? Body: Hey do you want pizza today?"
    elif email_id == 2:
        return "Subject: Urgent! Body: Your car warranty is about to expire."
    else:
        return "Error: Email not found!"

email_content = read_email_tool(2)
print("Handing this to AI to summarize:", email_content)
```

**Action 2:** The "System Prompt" String
Write a string variable that acts as the "Personality" of your agent. This is a very important concept in Agentic programming!
```python
system_prompt = """
You are a grumpy robot assistant. 
You are given a tool called 'math'. 
Whenever you answer a math question, complain about how easy the math is!
"""
print(system_prompt)
```

---

## 5. 🌟 Challenge of the Day!
Write a python function tool called `generate_random_enemy()`. 
Use the python `random` library (you'll need to research `import random` and `random.choice()`) to make it return either a "Goblin", "Dragon", or "Slime" randomly! 
*Hint: Ask Gemini: How do I pick a random string from a list in Python?*

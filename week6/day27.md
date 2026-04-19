# 🏗️ Week 6, Day 27: Building Project V1 (Core Logic) ⚙️

**Time:** 1 - 1.5 Hours  
**Goal:** Focus entirely on the Python backend! Write the `def` tools, `requests` API calls, and the String Parser engine. NO Streamlit yet!

---

## 1. The Core Concept: The Engine Block 🏎️

When you build a car, you don't paint the doors before you build the engine. 
Today, we are building the "Terminal Version" of your app. 
If your Python Tools don't work in the black-and-white terminal, they won't magically work when you put them on a website!

### Your Checklist for V1:
1.  [ ] Write your python `def` functions.
2.  [ ] Put `print()` statements inside the functions so you can see them running!
3.  [ ] Call the functions manually at the bottom of the script just to test if they `return` the right data.
4.  [ ] Set up your `chat_history` list with your `System Prompt`!

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Why separate the UI from the Backend logic?**
**A:** Imagine if every time you tweaked the color of a Streamlit button, you accidentally broke your python internet API request. By separating them, you guarantee the "Data Fetching" is 100% bug-free before you ever try to make it look pretty on the screen!

---

## 3. The AI Connection: AI Code Review ✨

If your python function is returning an error (like a `KeyError` or a `TypeError`), Gemini is the world's best debugger.

**Prompt Gemini:** 
> *"Gemini, I am trying to write a python function for my final project. Here is my code: [PASTE YOUR FUNCTION CODE]. But when I run it, I am getting an error. Can you help me fix it and explain what went wrong?"*

---

## 4. Hands-on Coding 💻

**Action 1: Write the Core Functions!**
Open your `backend_logic.py` file and write your tools.

*Example pattern for an API tool if you are making a Joke/Fact bot:*
```python
import requests

def fetch_fact(topic):
    print("TOOL RUNNING -> Looking up fact about " + topic)
    # Put your Requests API call here!
    # ...
    return "Fact data string!"
```

**Action 2: The Parse Engine**
Write a temporary terminal text `while` loop, JUST like we did on Week 4, Day 20. 
Use an `if` statement to simulate the AI triggering your tool!
```python
# Fake terminal test:
test_input = input("Test Action: ")
if "fact" in test_input:
    print("[AI Triggered Tool]")
    result = fetch_fact(test_input)
    print("Final Result ready to give to UI:", result)
```

---

## 5. 🌟 Challenge of the Day!
Make sure every single function you wrote has a `print()` statement at the very top of it saying exactly what parameters it received. This makes debugging 10x easier tomorrow!

# 🔘 Week 5, Day 22: Buttons, Inputs, & State 🎛️

**Time:** 1 - 1.5 Hours  
**Goal:** Learn how Streamlit handles "Memory", because websites refresh their memory every time you click a button!

---

## 1. The Core Concept: The Goldfish Website 🐟

Remember our "Goldfish Memory" lesson from Week 4? Streamlit has the EXACT same problem!

Every time you click a button on a Streamlit website, Python says: *"Oh! A click! I'm going to re-run the ENTIRE script from line 1!"*

If you had a variable `score = 0`, and the user clicks "Gain points!", Python restarts the script, sets `score = 0` again, and you never get any points!

### The Session State Backpack 🎒
To give Streamlit a memory, we use a special dictionary called `st.session_state`. If we put something inside this backpack, Streamlit won't delete it when the script restarts!

```python
import streamlit as st

st.title("The Cookie Clicker Game 🍪")

# 1. Setup the memory (Only if it doesn't exist yet!)
if "score" not in st.session_state:
    st.session_state["score"] = 0

# 2. Add a Button
clicked = st.button("Click for a Cookie!")

# 3. Increase score
if clicked == True:
    # We update the backpack memory!
    st.session_state["score"] = st.session_state["score"] + 1

# 4. Display score
st.header("Total Cookies: " + str(st.session_state["score"]))
```
*Run this code with `streamlit run app.py` and click the button! The score goes up!*

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: This seems incredibly annoying. Why does Streamlit delete its memory?**
**A:** Imagine a website with 1,000 users right now. If the website remembered every single variable for every single user forever, the server's hard drive would explode! By resetting instantly, the website stays lightning fast. We just tell it exactly what specific data (`session_state`) it is allowed to keep!

---

## 3. The AI Connection: Chat History on the Web! 💬

When we build our AI Chatbot on the web, where do we keep our `chat_history` list?
In the `session_state`! If we didn't, the AI would forget the conversation the second you typed your next message!

**Prompt Gemini:** *"I am building a Streamlit app. Can you give me a 10 line example of using `st.session_state` and a python `List` to build a fake 'To-Do' list where typing in an `st.text_input` adds the task to the memory list and displays it below?"*

---

## 4. Hands-on Coding 💻

**Action 1:** The Magic 8-Ball App 🎱
Let's build an app where the user asks a question, and we give a random answer from a list! Memory isn't strictly needed here, but buttons and inputs are!

```python
import streamlit as st
import random

st.title("Magic AI 8-Ball 🎱")
user_question = st.text_input("Ask me anything about your future:")

# Only pick an answer if they click the button AND the question isn't empty!
if st.button("See the future") and user_question != "":
    answers = ["Without a doubt!", "Ask again later...", "Absolutely NOT!", "It is certain!"]
    final_answer = random.choice(answers)
    
    st.success("The Spirits say: " + final_answer)
```

**Action 2:** The Layout (Columns!) 🏛️
Websites look better when things are next to each other. We use `st.columns`!

```python
import streamlit as st

col1, col2 = st.columns(2) # Make 2 columns!

with col1:
    st.header("Left Column ⬅️")
    st.button("I am on the left!")

with col2:
    st.header("Right Column ➡️")
    st.button("I am on the right!")
```

---

## 5. 🌟 Challenge of the Day!
Combine them! Use `st.columns()` to put the Magic 8-Ball input box in the left column, and a giant picture of an 8-ball (`st.image("URL")`) in the right column!

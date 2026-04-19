# 🎨 Week 6, Day 28: Building Project V2 (The UI) 📱

**Time:** 1 - 1.5 Hours  
**Goal:** Take your perfect python engine from yesterday, import it, and build the Streamlit Graphic User Interface over it!

---

## 1. The Core Concept: Assembling the Pieces 🧩

Yesterday you built the Engine. Today we paint the Car.
Because our logic is all locked inside beautiful `def` functions, our Streamlit app doesn't have to be messy!

### The Power of `import`
Instead of copy-pasting your 100 lines of tool code into your Streamlit file, you can keep them in `backend_logic.py`, and just `import` them into `app.py`!

```python
# Inside your NEW app.py file:
import streamlit as st

# We import the tool we wrote yesterday!
from backend_logic import fetch_fact 

st.title("My Awesome App!")
# ... rest of your streamlit UI ...
```

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Wait, I can import my OWN files? I thought `import` was only for official libraries like `requests`!**
**A:** YES! In professional software, a single App might be built out of 50 different `.py` files, all connected using `import`. This keeps any single file from getting too confusing and long to read.

---

## 3. The AI Connection: Asking AI for Streamlit Layouts ✨

Streamlit has so many cool layout features you probably haven't memorized. `st.tabs`, `st.expander`, `st.sidebar`, `st.metrics`.

**Prompt Gemini:** 
> *"I am building a Streamlit chat app. I imported my python tool `fetch_fact(topic)`. Can you write the Streamlit UI code that has a `st.chat_input` box at the bottom, and if the user types 'fact', it shows a visual spinning wheel `st.spinner("Fetching...")` while it runs the imported `fetch_fact` tool?"*

---

## 4. Hands-on Coding 💻

**Action 1: Setup the Streamlit Skeleton**
In your `app.py` file, set up your Title, Sidebar, and the essential `st.session_state` chat memory list!
*Hint: Look back at the code from Week 5, Day 23!*

**Action 2: Wire up the Logic**
 inside your `if prompt = st.chat_input():` block:
1. Show the user's message using `st.chat_message("user")`.
2. Do your `if` statement logic check that decides if the tool should run.
3. Call your `backend_logic` tool function! (e.g. `answer = fetch_fact("dogs")`) 
4. Draw the `answer` using `st.chat_message("ai")`.
5. Append it all to `st.session_state` memory!

---

## 5. 🌟 Challenge of the Day!
Add an `st.image()` to your app's sidebar that perfectly fits your bot's Personality! 
If you made a Pirate bot, add a picture of a parrot!

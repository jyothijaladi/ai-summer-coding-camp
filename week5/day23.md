# 🔌 Week 5, Day 23: Connecting Chat to Streamlit 💬

**Time:** 1 - 1.5 Hours  
**Goal:** Build the visual interface for our Chatbot using Streamlit's awesome built-in chat UI components!

---

## 1. The Core Concept: The Chat bubbles 💭

Building chat bubbles manually (making gray boxes, centering text, aligning them left or right) is terrible. 
Thankfully, Streamlit has two built-in commands that do 100% of the work for us:
1. `st.chat_message("user")` - Draws a user icon and bubble.
2. `st.chat_input("Type here")` - Draws a pretty chat box at the bottom of the screen!

### The Visual Loop
We need to combine our `session_state` (Memory) with `st.chat_message()`!

```python
import streamlit as st

st.title("Agentic Chat Simulator 🤖")

# 1. Initialize Memory
if "messages" not in st.session_state:
    st.session_state["messages"] = []

# 2. Draw ALL past messages (The History)
for msg in st.session_state["messages"]:
    with st.chat_message(msg["role"]):
        st.write(msg["text"])

# 3. Accept User Input at the bottom of the screen!
user_input = st.chat_input("Say something!")

# 4. If they type something...
if user_input:
    # A. Save their message AND draw it instantly
    st.session_state["messages"].append({"role": "user", "text": user_input})
    with st.chat_message("user"):
        st.write(user_input)

    # B. Fake an AI Response! (Later this will be the real Gemini!)
    fake_ai_reply = "I heard you say: " + user_input
    
    # C. Save the AI's reply AND draw it
    st.session_state["messages"].append({"role": "ai", "text": fake_ai_reply})
    with st.chat_message("ai"):
        st.write(fake_ai_reply)
```
*Run this code! You just built the exact UI that ChatGPT uses!*

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Why do we have to draw ALL the past messages in a loop?**
**A:** Remember the goldfish memory! If you click Send on message #5... Streamlit restarts from line 1! It wipes the screen totally clean. The `for` loop looks inside the `session_state` backpack, sees the 4 old messages, and rapidly redraws them on the screen before drawing message #5!

---

## 3. The AI Connection: Understanding the UI flow ✨

**Prompt Gemini:** *"I have a python streamlit chat app. How can I change the `st.chat_message("ai")` icon from the default robot to a custom emoji, like a Dragon emoji 🐉?"*

*(Gemini will show you how to use parameters! e.g., `st.chat_message("ai", avatar="🐉")`)*

---

## 4. Hands-on Coding 💻

**Action 1:** The Character Chat! 🐉🧛‍♂️
Modify the chatbot you just built above. 
Change the AI's logic so that if the user's input contains a "?" question mark, the AI replies: "That is a great question!"
If the user's input does not contain a question mark, reply: "Please ask me a question!"

```python
    # ... inside the "if user_input:" block
    if "?" in user_input:
        fake_ai_reply = "That is a great question, human!"
    else:
        fake_ai_reply = "I am an answering bot. Please ask me a question!"
        
    # ... save and draw it! 
```

**Action 2:** Customizing the Avatars 🎨
Update your `st.chat_message()` lines to use emojis. Use "👤" for the user, and "🤖" for the AI!
When you redraw the history in the `for` loop, you have to pass the avatar there too!

---

## 5. 🌟 Challenge of the Day!
Let's add a "Clear Memory" button! 
Add an `st.button("Clear Chat")` to the `st.sidebar` (Ask Gemini how to use Streamlit sidebars!). 
If the button is clicked, set the `st.session_state["messages"] = []` (an empty list) to nuke the memory!

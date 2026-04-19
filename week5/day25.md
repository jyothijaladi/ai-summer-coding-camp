# 🛠️ Week 5, Day 25: Project 5 - Visual AI Chatbot App! 📱

**Time:** 1 - 1.5 Hours  
**Goal:** Take our Console Chatbot Engine from Week 4 and embed it directly into our beautiful Streamlit UI from Week 5!

---

## 1. The Core Concept: Merging Backend and Frontend 🧩

Today we bring everything together.
*   **The Backend (Brain):** The Tools, the Parsing logic, the Agent pipeline.
*   **The Frontend (Face):** The Streamlit Chat UI, the Sidebars, the Buttons.

We are going to build **"The Detective Bot"**.

---

## 2. Step-by-Step Build Guide 📝

### Step A: The Tool and The Engine
Write a fake python tool our detective can use (e.g. searching a database).
```python
import streamlit as st
import time

# --- THE BACKEND ---
def search_clues(suspect_name):
    print("Database search running...")
    if "bob" in suspect_name.lower():
        return "Bob was seen buying donuts at 9 PM."
    else:
        return suspect_name + " has a perfect alibi."
```

### Step B: The Streamlit UI Setup
Now we set up the Title, Sidebar, and the Memory (`st.session_state`).
```python
# --- THE FRONTEND ---
st.title("🕵️‍♂️ Detective AI Partner")

# Add a sidebar to show the rules!
with st.sidebar:
    st.image("https://images.dog.ceo/breeds/hound-basset/n02088238_10473.jpg", caption="Your Partner")
    st.write("Welcome Detective.")
    st.write("**Hidden Tool Rule:** If you want to search the database, the AI will type <SEARCH>name</SEARCH>")
    
    if st.button("Clear Case Files"):
        st.session_state["messages"] = []

# Initialize Memory
if "messages" not in st.session_state:
    st.session_state["messages"] = [{"role": "ai", "content": "Hello partner. Who are we investigating today?"}]
```

### Step C: Drawing the Visual Chat History
Every time the page restarts, redraw the old messages!
```python
for msg in st.session_state["messages"]:
    with st.chat_message(msg["role"]):
        st.write(msg["content"])
```

### Step D: The Human Input & AI Parser Logic
This is the magic block! When the user types, append it to memory, draw it, and then simulate the AI making a Tool Decision!
```python
user_input = st.chat_input("Ask your partner a question...")

if user_input:
    # 1. Save and draw human message
    st.session_state["messages"].append({"role": "user", "content": user_input})
    with st.chat_message("user"):
        st.write(user_input)

    # 2. Fake AI Logic (Connecting to real Gemini API is an advanced homework!)
    with st.chat_message("ai"):
        st.write("...thinking...")
        time.sleep(1) # Fake delay!
        
        # Simulated Decision parsing
        if "bob" in user_input.lower():
            # The AI "decides" to use the tool!
            st.info("Agent Partner is opening the database...")
            
            # Python runs the tool!
            tool_data = search_clues("Bob")
            
            # The AI formats the result!
            final_ai_reply = "I checked the database! " + tool_data + " He looks guilty."
            st.success("Tool Execution Complete")
            
        else:
            final_ai_reply = "I don't think we have any clues on " + user_input + "."
            
        # Draw and Save the final AI response
        st.write(final_ai_reply)
        st.session_state["messages"].append({"role": "ai", "content": final_ai_reply})
```

---

## 3. Play Testing! 🎮
1. Run `streamlit run app.py`
2. Talk to your agent. Ask about "Alice". It should use standard chat.
3. Ask the agent to investigate "Bob". Watch the Streamlit UI pop up Green and Blue info boxes (`st.info` / `st.success`) as it "triggers" your python tool and returns the formatted data!

---

## 4. Kid Q&A: "Why is this useful?" 🤔

**Q: I am just writing `if "bob"`... isn't this fake AI?**
**A:** Yes! But the *Architecture* is real. 
If you simply replace `if "bob" in user_input.lower():` with `ai_response_string = ask_gemini_api(user_input)`, and you parse `ai_response_string` for `<SEARCH>` tags, your code becomes 100% REAL Agentic AI with no other UI changes! You built the robotic car; next week we just put the real engine inside!

---

## 5. 🌟 Challenge of the Week!
This app is yours! Change the title, change the avatar image, change the background color. Make it your own unique Agent concept. Will it be a Space Navigator? A Pokemon guide? The choice is yours!

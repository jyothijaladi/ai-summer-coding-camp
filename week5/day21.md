# 🖥️ Week 5, Day 21: Intro to Visual Web Apps! 🌐

**Time:** 1 - 1.5 Hours  
**Goal:** Leave the black-and-white terminal behind and learn what Streamlit is and why it's perfect for AI Apps.

---

## 1. The Core Concept: Escaping the Terminal 🏃‍♀️

Until now, we have lived in the Terminal (or console). We type text, hit enter, and white text appears on a black screen. It feels like we are hacking in the 1990s!

Real people don't use the terminal. They click buttons and look at pictures on websites.
We are going to use a Python library called **Streamlit**. It takes our python code and turns it into a beautiful, clickable Website instantly!

### Installing Streamlit
*(If not already installed, ask your instructor!)*
In your terminal, type: `pip install streamlit`

### The First App
Create a new file called `app.py`.
```python
import streamlit as st

st.title("My First AI App! 🚀")
st.write("Welcome to the future of coding.")

# Let's add an emoji!
st.snow() 
```

### Running the App
You don't click "Run" like normal. In your terminal, you must type:
`streamlit run app.py`

*BOOM!* Your web browser will open and show a website with snow falling down!

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Why do we use Streamlit instead of making a normal website with HTML and CSS?**
**A:** Building a normal website takes HTML, CSS, JavaScript, routing, a backend server, and an API. That takes months to learn! Streamlit was built specifically for Data Scientists and AI Engineers because they just want to show off their AI quickly without learning JavaScript. One line of Python (`st.button()`) creates 50 lines of invisible HTML code for you!

---

## 3. The AI Connection: Generating UIs ✨

Streamlit is incredibly popular in the AI world. If you look at massive companies building AI tools, they often prototype their dashboards using Streamlit!

**Prompt Gemini:** *"I am learning how to build simple web apps with python `import streamlit as st`. Can you write a 10-line python script that uses `st.slider()` to ask my age, and `st.write()` to print a funny message about how old I am?"*

---

## 4. Hands-on Coding 💻

**Action 1:** The Emoji Spammer 😂
Create an app that uses a slider to let the user pick a number, and then prints that many emojis on the screen!

```python
import streamlit as st

st.title("The Emoji Spammer 🍕")

# This puts a slider on the screen from 1 to 100!
number = st.slider("How many pizzas do you want?", 1, 100)

# We can use python string multiplication!
pizza_string = "🍕" * number

st.write(pizza_string)
```

**Action 2:** Building a Secret Code Box
Let's use `st.text_input` (which is exactly like `input()` but for websites!) to make a password box!
```python
import streamlit as st

st.title("The Vault 🔒")
st.write("Enter the secret password to open the vault.")

password = st.text_input("Password:")

# It updates instantly as we type!
if password == "1234":
    st.success("ACCESS GRANTED! 🎉")
    st.balloons()
elif password != "":
    st.error("ACCESS DENIED!")
```

---

## 5. 🌟 Challenge of the Day!
Add a `st.button("Click Me!")` to your app. 
Wrap your balloons code in an `if` statement so the balloons *only* trigger when you click the button! (Ask Gemini how to use Streamlit buttons!)

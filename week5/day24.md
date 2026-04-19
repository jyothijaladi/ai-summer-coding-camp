# 🎨 Week 5, Day 24: Adding Images and Styling 🖼️

**Time:** 1 - 1.5 Hours  
**Goal:** Make our Streamlit app look professional by adding images, changing themes, and organizing our layout.

---

## 1. The Core Concept: The Polish ✨

A good app isn't just smart; it looks good too!
Streamlit makes adding multimedia incredibly easy. Instead of downloading images and dealing with complicated file paths, we can just pass an Image URL from the internet straight into our python code!

### Adding an Image
```python
import streamlit as st

st.title("My Awesome Image Viewer!")

# We use st.image!
image_url = "https://images.dog.ceo/breeds/husky/n02110185_10047.jpg"
st.image(image_url, caption="A Very Good Boy")
```

### The Magic of Expanding Elements
If you want to hide long text or secret rules, you can use `st.expander`!
```python
with st.expander("Click here for secret rules!"):
    st.write("1. No spamming.")
    st.write("2. Be nice to the AI.")
    st.image("https://images.dog.ceo/breeds/pug/n02110958_238.jpg")
```

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Why don't we download the image to our computer instead of using a URL?**
**A:** You can! But using URLs is faster for prototyping. More importantly, when we build our APIs, APIs often return Image URLs! (Remember the NASA API? It gave us a URL!). Our Streamlit app can take the URL *directly* from the API dictionary and plug it straight into `st.image()` dynamically!

---

## 3. The AI Connection: AI Layout Designers ✨

Designing pretty websites is hard. When you are stuck trying to figure out how to put an image next to a paragraph of text, you can ask Gemini to act as a Frontend Web Developer!

**Prompt Gemini:** *"I have a python streamlit app. Can you write a 15 line script demonstrating how to use `st.columns()` to put a title and description in the left column, and an `st.image` of a hamburger in the right column?"*

Take the code Gemini provides and run it! You instantly get a beautiful split-screen layout!

---

## 4. Hands-on Coding 💻

**Action 1:** The NASA Image App 🌌
Let's combine Week 3 (APIs) and Week 5 (Streamlit)! We will fetch the NASA API image and put it on our website!

```python
import streamlit as st
import requests

st.title("Daily NASA Explorer 🚀")

if st.button("Fetch Today's Space Image"):
    # 1. Show a spinner while we wait for the internet!
    with st.spinner("Calling NASA..."):
        # 2. Get the dictionary
        url = "https://api.nasa.gov/planetary/apod?api_key=demo_key"
        response = requests.get(url)
        data = response.json()
        
    # 3. Use Streamlit to draw the data!
    st.subheader(data["title"])
    st.image(data["url"])
    st.write(data["explanation"])
    
    st.success("Download complete!")
```
*Look how professional that looks! You didn't write a single line of HTML!*

---

## 5. 🌟 Challenge of the Day!
Use the Dog API: `https://dog.ceo/api/breeds/image/random`
Build a Streamlit app with a massive button that says "GIMME A DOGGO". 
Every time the user clicks the button, fetch the API, and use `st.image()` to display the random dog picture returning in the `"message"` key of the JSON!

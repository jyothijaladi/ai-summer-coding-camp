# 📡 Week 3, Day 13: Fetching Data (`requests`) 🌍

**Time:** 1 - 1.5 Hours  
**Goal:** Call an API from inside Python using the `requests` library and print out live data!

---

## 1. The Core Concept: Sending the Waiter 🏃

Yesterday, we used our Chrome Web Browser to act as the "Waiter" to fetch data from an API. Today, we are going to write python code that makes a request automatically!

We will use a special python tool (called a **Library**) named `requests`.

*Notice: You may need to ask your instructor to install the `requests` library (`pip install requests`) if your editor doesn't have it built-in!*

### Making our First API Call!
Let's get a random fact about a cat using the Cat Fact API!

```python
# 1. Import the library (bring the tools into our file)
import requests

# 2. Setup the URL (Endpoint)
url = "https://catfact.ninja/fact"

# 3. Ask the waiter to get the data!
response = requests.get(url)

# 4. Turn the answer into a Python Dictionary (JSON)!
data = response.json()

# 5. Print it out!
print(data)
```

Run this code! You should see something like:
`{'fact': 'Cats have 32 muscles in each ear.', 'length': 33}`

### Plucking Out Just What We Want 📌
Printing the whole dictionary is ugly. We only want the fact! Since `data` is a dictionary, we just ask for the `"fact"` key!

```python
# Assuming we have our 'data' dictionary from above:
clean_fact = data["fact"]
print("Did you know? " + clean_fact)
```

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Do all apps use `requests.get()`?**
**A:** Every single app that requires the internet uses something exactly like this! When you open Instagram, it basically runs `requests.get("instagram.com/my_feed")`, gets the JSON dictionary of pictures, and puts them on your screen. You just learned the foundation of the entire internet!

---

## 3. The AI Connection: AI loves formatting APIs ✨

Some APIs return MUDDY data. An API might return `{"temp": 298.15}` which is Kelvin, not Fahrenheit! Instead of doing the scary math, we can just hand that ugly API dictionary to Gemini and say "Gemini, turn this into a fun human sentence in Fahrenheit!" We will do this tomorrow!

**Prompt Gemini:** *"I have a python dictionary from an API that looks like this: `{'name': 'Luke Skywalker', 'height': '172', 'mass': '77'}`. Can you write a python script that extracts those three keys and prints them in a nice formatted sentence?"*

---

## 4. Hands-on Coding 💻

**Action 1:** The Space Station Tracker 🚀
There is an API that tells you who is currently floating in space on the International Space Station!
```python
import requests

url = "http://api.open-notify.org/astros.json"
response = requests.get(url)
data = response.json()

# Look at the dictionary it gives us!
print("There are " + str(data["number"]) + " people in space right now!")

# Can we loop through them? Yes! 'people' is a List of Dictionaries!
for person in data["people"]:
    print("- " + person["name"] + " is on the " + person["craft"])
```

**Action 2:** Building a Joke Machine 🤡
Let's use the Official Joke API to make a python program that tells you a random joke!
```python
import requests

url = "https://official-joke-api.appspot.com/random_joke"
response = requests.get(url)
data = response.json()

print(data["setup"])
# (Ask the user to press enter to see the punchline!)
input("...Press Enter...") 
print(data["punchline"] + " 🤣")
```

---

## 5. 🌟 Challenge of the Day!
Put your Joke Machine code inside a `while` loop so that after the joke is told, it asks the user: "Want another joke? (yes/no)". If yes, it fetches a BRAND NEW joke from the API!

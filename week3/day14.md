# 🤖 Week 3, Day 14: Letting AI Format Our Data 🎨

**Time:** 1 - 1.5 Hours  
**Goal:** Use an API to get raw data, and conceptually design how an Agentic AI will take that raw data and summarize it into a fun, readable format!

---

## 1. The Core Concept: The Interpreter 🗣️

Yesterday we fetched data from the Space Station API. The raw dictionary looked like this:
`{'name': 'Oleg Kononenko', 'craft': 'ISS'}`

That's great for computers, but if you are building an app for humans, it's boring!
What if we want our application to sound like a grumpy alien reporter giving the news about the humans hovering in space?

We use an **Agent** as the middle-man!
`API Data --> AI Agent Prompt --> Beautiful Formatted Result`

### The Manual "Agent" Simulation
Today, we are going to manually act as the API bridge! We will get data in Python, print it out, copy it with our mouse, give it to Gemini along with a System Prompt, and let Gemini rewrite it!

*Note: In Week 4, we will learn how to connect Python directly to Gemini so it happens automatically!*

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: If my Python code can print the API data, why involve AI?**
**A:** Imagine a Weather API returning a dictionary with 500 keys: pressure, humidity, dew point, wind angles, etc. Your python code would need 100 `if/else` statements to figure out if it should say "Bring an umbrella" or "Wear a coat". 
If you just hand the 500-key dictionary to an AI and say "Summarize this weather for a 5-year old," the AI handles ALL the logic for you instantly! It is a massive time-saver!

---

## 3. The AI Connection: AI Persona Prompts 🎭

To get an Agent to re-format data, we give it a Persona. 

A Persona has two parts:
1. **The System Prompt:** Who the AI is acting like.
2. **The User Prompt:** The raw JSON/Dictionary data from the API.

Let's test this directly inside Antigravity Gemini!

**Prompt Gemini:** 
> *"Act as an over-excited sports announcer. I am going to give you raw JSON data from a Weather API. Please announce the weather like it is the final quarter of the Super Bowl! Here is the data: `{'city': 'Chicago', 'temp': '10 degrees', 'wind': '30mph', 'status': 'BLIZZARD'}`"*

Read what Gemini outputs! Doesn't that sound WAY better than just `print("Weather is blizzard")`? This is the power of Agentic data formatting!

---

## 4. Hands-on Coding 💻

**Action 1:** Fetch the Raw Boring Data 🥱
Write this script to get the current Bitcoin or Crypto price using the Coindesk API!
```python
import requests

# Fetch the LIVE Bitcoin Price API
url = "https://api.coindesk.com/v1/bpi/currentprice.json"
response = requests.get(url)
data = response.json()

# The API hides the price deep inside a few dictionaries!
current_price = data["bpi"]["USD"]["rate"]
print("Raw Price data:", current_price)
```

**Action 2:** The Manual Agent Upgrade! 💎
Now that your terminal printed the raw price data (e.g. `Raw Price data: 65,000.45`)...
In your Gemini Chat, create an amazing custom prompt for it using that number!

**Example Prompt to test in Gemini:** 
> "You are a panicked goblin who loves shiny things. The current price of Bitcoin is [INSERT NUMBER HERE]. Can you scream a 3-sentence warning to your goblin friends about whether you should buy more or run away?"

---

## 5. 🌟 Challenge of the Day!
Find the Joke API script you wrote yesterday. Run it to get a raw joke.
Then, prompt the Gemini AI:
*"You are a grumpy old wizard who hates humor. I am going to tell you a joke. You must ruthlessly critique the joke and explain why it makes no logical sense. The joke is: [INSERT JOKE SETUP] ... [INSERT JOKE PUNCHLINE]"*

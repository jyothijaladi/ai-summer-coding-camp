# 💬 Week 4, Day 19: Handling the Bot's Responses (Parsing) 🕵️‍♂️

**Time:** 1 - 1.5 Hours  
**Goal:** Learn how to use python string commands to "crack open" an AI's response and figure out if it wants to chat or if it wants to run a tool!

---

## 1. The Core Concept: The Secret Code Word 🔑

In real Agentic frameworks (like LangChain or simple Gemini integrations), AI doesn't just return a single string. It returns a complex object. But conceptually, it's just passing text back to Python.

Imagine giving the AI this rule in your System Prompt:
> *"If you want to talk to the user, just type normally. BUT! If you want to use the weather tool, type exactly: `<TOOL>WEATHER</TOOL> [City Name]`"*

When the AI responds, Python receives a big string. We have to **Parse** (search through) the string to see if the AI typed the secret code phrase!

### Python String Methods (`in`, `.split()`)
How do we find secret words in a giant paragraph? We use `in`!
```python
ai_response = "I think it is raining. <TOOL>WEATHER</TOOL> London"

# Check if the secret code is inside the string!
if "<TOOL>WEATHER</TOOL>" in ai_response:
    print("ALERT! The AI wants to run the weather tool!")
else:
    print("Normal Chat:", ai_response)
```

### Ripping out the Parameter 🤏
If the AI typed `<TOOL>WEATHER</TOOL> London`, how do we delete the ugly `<TOOL>` tag so we just have the word "London" to pass into our python function? We use `.replace()` and `.strip()`!

```python
ugly_string = "<TOOL>WEATHER</TOOL> London"

# Replace the ugly tag with nothing ("")
cleaned_string = ugly_string.replace("<TOOL>WEATHER</TOOL>", "")

# .strip() removes any extra spaces at the beginning or end of the string!
final_city = cleaned_string.strip()

print("Clean City Name:", final_city) # Output: London
```

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Why don't we just use real AI libraries instead of fake `replace()` commands?**
**A:** Underneath the hood, the massive Google servers are doing exactly this! They receive the text from the AI, they look for specific JSON brackets `{}` or XML tags `<tool>`, and they slice the string apart. Understanding *how* parsing works helps you fix bugs when the AI makes a typo and the tool fails to run!

---

## 3. The AI Connection: Asking AI to write Parsers ✍️

Parsing strings can get messy. Thankfully, we can ask Gemini to write the `.replace()` chained commands for us!

**Prompt Gemini:** *"I have a python string `response = '[ACTION] JUMP [SPEED] 50'`. Can you write a python script using `.replace()` and `.split()` that extracts just the word 'JUMP' into an Action variable, and the number '50' into a Speed variable?"*

---

## 4. Hands-on Coding 💻

**Action 1:** The Minecraft Bot Command Parser ⛏️
Let's build a script that handles an "AI's response string". If the AI types `COMMAND:DIG`, our Python print function will dig!

```python
print("The AI has responded...")

# Pretend this string just came back from Gemini API over the internet!
fake_ai_response_string = "Based on the zombies approaching, COMMAND:RUN"

if "COMMAND:DIG" in fake_ai_response_string:
    print("⛏️ Python Tool Activated: Digging one block down.")
elif "COMMAND:RUN" in fake_ai_response_string:
    print("🏃‍♂️ Python Tool Activated: Player running away fast!")
else:
    # If there is no command, just print what the AI said!
    print("Chat:", fake_ai_response_string)
```

**Action 2:** The Password Extractor 🎟️
Write a script that takes a messy string: `ai_message = "I have cracked the code! The secret is PASSWORD[dragon_breath]"`
Use `.replace("PASSWORD[", "")` and `.replace("]", "")` to clean the string so ONLY the word `dragon_breath` is left in a variable!

```python
ai_message = "PASSWORD[dragon_breath]"

# Chaining replaces!
clean_pass = ai_message.replace("PASSWORD[", "").replace("]", "")
print("The secret code is:", clean_pass)
```

---

## 5. 🌟 Challenge of the Day!
Write a python `while` loop that acts like a calculator parsing engine.
Keep asking the user for `input()`. 
If they type a string that contains a `+`, use `.split("+")` (ask Gemini how split works!) to rip the two numbers apart, convert them to `int()`, and print the sum!

# 🔧 Week 4, Day 18: Giving the Bot a "Tool" 🛠️

**Time:** 1 - 1.5 Hours  
**Goal:** Understand how an AI chooses to trigger a Python function (A Tool) instead of just talking to the user.

---

## 1. The Core Concept: The Robot Arm 🦾

Right now, our AI can talk safely inside its jar. But if the user says "What is the weather in Paris?" the AI will try to invent a fake temperature because it doesn't have internet access!

Instead, we give the AI a **Tool Definition**. 
We tell the AI: *"Hey, if the user asks for the weather, DON'T guess. Use the `get_weather` tool. If you use it, I will run my Python code, and I will hand you the answer!"*

### The Tool JSON (Dictionary)
How do we tell the AI about a tool? We send it a dictionary explaining what the tool does! 
```python
# Our actual Python function
def get_weather(city):
    print("PYTHON IS RUNNING! Fetching weather for " + city)
    return "72 Degrees and Sunny"

# The dictionary we hand to the AI to describe the function
weather_tool_definition = {
    "name": "get_weather",
    "description": "Call this tool when the user asks for the weather.",
    "parameters": {
        "city": "The name of the city the user wants the weather for"
    }
}
```

When the user asks for weather, the AI looks at the list of tools and says: *"Oh! I shouldn't type text to the user. I should output a secret JSON dictionary asking python to run `get_weather(city='Paris')`"*

This is the absolute core of **Agentic AI**. The AI makes a **Decision** to run code!

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Can the AI write its own tools?**
**A:** In advanced systems, yes! But for now, WE are the programmers. We control the world. If we give the AI a `move_minecraft_player_forward()` tool, we can literally talk to the AI, and the AI will play Minecraft for us by triggering that tool over and over!

**Q: What if the AI uses the wrong tool?**
**A:** This happens! If you say "How are you?", the AI might accidentally trigger the weather tool. That is why the `"description"` string inside your tool definition is super important. It tells the AI's brain the exact rules for when to press the button.

---

## 3. The AI Connection: Generating Tool Definitions ✨

Writing large `tool_definition` dictionaries can get annoying because they have to be formatted perfectly. We can use Gemini to write them for us!

**Prompt Gemini:** *"I am building an Agentic AI in Python. I have a function called `fire_laser(color, power_level)`. Can you write the JSON Schema dictionary (like OpenAI or Gemini tool definitions use) that describes this tool to the AI so the AI knows how to use it?"*

Look at how detailed Gemini makes the dictionary! It defines what type of data the parameters need (e.g. `power_level` must be an integer!).

---

## 4. Hands-on Coding 💻

**Action 1:** The Simulated Tool Call 📟
Today, we are going to write a script that acts like a fake AI making a decision using an `if` statement based on user input.

```python
# The Tool
def play_sound(sound_name):
    # Imagine this connects to the speakers!
    print("🎶 BEEP BOOP! Playing: " + sound_name)
    return "Sound played successfully."

print("Robot Assistant: How can I help you?")
user_request = input("You: ")

# Imagine this next block is the AI's brain thinking...
if "play" in user_request.lower() or "sound" in user_request.lower():
    print("[AI DECISION] The user wants a sound. I am triggering the 'play_sound' tool!")
    
    # The AI "extracts" a parameter (we just hardcode it for this simulation)
    parameter_to_pass = "Guitar Solo" 
    
    # Python runs the tool!
    result = play_sound(parameter_to_pass)
    
    # The AI sees the result
    print("Robot Assistant: Done! I played that sound for you.")
else:
    print("[AI DECISION] The user is just chatting.")
    print("Robot Assistant: That is very interesting! Tell me more.")
```

---

## 5. 🌟 Challenge of the Day!
Add a second tool to the simulation above called `def change_lights(color):`.
Use an `elif` statement inside the "AI Brain" block to check if the user typed the word "light" or "color". If they did, print an `[AI DECISION]` message explaining it is triggering the `change_lights` tool, and then run it!

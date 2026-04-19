# 🛠️ Week 4, Day 20: Project 4 - The Basic Console Agent 🤖

**Time:** 1 - 1.5 Hours  
**Goal:** Combine your `while` chat loop, your `System Prompt`, your Python Function `Tools`, and your `String Parser` into a fully working Agentic Simulation framework!

---

## 1. The Core Concept: The Agentic Matrix 🌐

Today we put the 4 pieces of the Agent puzzle together.
**The Pipeline:**
1. You say something to the Bot.
2. The Bot "Thinks" (Checks if it needs a tool using `in`).
3. If it needs a tool -> Python runs the tool -> Pass the data back to the Bot!
4. If it doesn't need a tool -> Bot just prints a response.

---

## 2. Step-by-Step Build Guide 📝

### Step A: The Tool Definition
Put your tools at the very top of your file.
```python
import random

def get_random_joke():
    jokes = ["Why did the computer squeak? Someone stepped on its mouse!", 
             "What do you call a baby robot? A micro-chip!"]
    # return a random choice from the list!
    return random.choice(jokes)
```

### Step B: The Setup & Memory
Set up the `chat_history` and the `system_prompt`!
```python
print("🌟 The Bot is awake! Type 'quit' to exit. 🌟")

system_prompt = """
You are a helpful assistant.
RULE: If the user asks for a joke, you MUST respond exactly with the text: <TOOL>JOKE</TOOL>
If the user asks a normal question, just respond normally.
"""

chat_history = [{"role": "system", "text": system_prompt}]
```

### Step C: The Chat Loop & Human Input
```python
while True: # Infinite loop until we 'break'
    user_input = input("\nYou: ")
    
    if user_input.lower() == "quit":
        print("Goodbye!")
        break # This destroys the while loop!
        
    chat_history.append({"role": "user", "text": user_input})
```

### Step D: The AI Parser Matrix (Inside the loop!)
Because we don't have the Gemini API hooked up directly yet, we will simulate the AI's brain using an `if` statement based on the user's input, but treating the output as if it came from the AI.

```python
    # Ensure this is indented inside the while loop!
    print("...Bot is thinking...")
    
    # Fake AI Engine Logic
    # (In Week 5, 'ai_response' will come directly from requests.get('gemini_api')!)
    if "joke" in user_input.lower():
        ai_response = "<TOOL>JOKE</TOOL>"
    else:
        ai_response = "That is very interesting! Can you tell me more about " + user_input + "?"
    
    # Now, parse the AI's response to see if it triggered a tool!
    if "<TOOL>JOKE</TOOL>" in ai_response:
        print("[SYSTEM ALERT] AI triggered the Joke Tool!")
        
        # 1. Run the Python function
        tool_data = get_random_joke()
        
        # 2. Pretend to send the data back to the AI for formatting...
        print("Bot: Okay, I have a joke for you! " + tool_data)
        
        # 3. Add to memory
        chat_history.append({"role": "assistant", "text": tool_data})
        
    else:
        # Standard chat!
        print("Bot: " + ai_response)
        chat_history.append({"role": "assistant", "text": ai_response})
```

---

## 3. Play Testing! 🎮
Run your game!
1. Type "Hello there". Wait for the Bot to reply.
2. Type "Tell me a joke". Watch the Terminal explode with System Alerts as it routes the command through the Python tool and hands the result back!

You have just built the architectural blueprint of an $8,000,000 tech startup. This loop is exactly how AI assistants control your computer, search the web, and run code!

---

## 4. Kid Q&A: "Why is this useful?" 🤔

**Q: Wait, I wrote the tool AND I wrote the if statement. Where is the AI?**
**A:** This is a **Mock-up**. When engineers build rockets, they test them on empty frames first. Before you pay money to hook up a real AI API to your code, you MUST make sure your Python loops, parsers, and tool functions work perfectly using fake data! Next week, we rip out the `if joke...` fake engine, and slot the REAL Gemini engine in its place!

---

## 5. 🌟 Challenge of the Day! (Bonus)
Add a second tool called `def roll_dice():` that returns a random integer from `1 to 20`. 
Add a rule to the system prompt `<TOOL>DICE</TOOL>`, and update the engine block to catch it and run the tool when the user types "roll"!

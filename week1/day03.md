# ⚖️ Week 1, Day 3: Decisions & Logic (If/Else) 🤔

**Age Group:** 3rd - 8th Grade (Complete Beginners)
**Time:** 1 - 1.5 Hours  

## 👩‍🏫 Teacher's Lesson Plan
1. **(10 min) Review:** How do we glue strings together? How do we ask the user a question?
2. **(20 min) The Lesson:** The Traffic Light analogy. Explain `if`, `elif` (Else-If), and `else`. Explain the difference between `=` (saving to a box) and `==` (comparing). Also highly emphasize **Indentation** (hitting the Tab key).
3. **(40 min) Hands-on:** Kids design an RPG choice or a password gate.

---

## 1. What are we doing? (The Core Concept) 👑

Computers only know what to do if you tell them *exactly* how to decide.

Imagine driving a car:
- 🟢 **If** the light is green, go.
- 🟡 **Else If (`elif`)** the light is yellow, slow down.
- 🔴 **Else** (it must be red), stop!

In Python, it looks like this:
```python
light_color = input("What color is the traffic light? ")

if light_color == "green":
    print("Go Go Go!")
elif light_color == "yellow":
    print("Slow down!")
else:
    print("STOP!")
```
**Super Important Rules:** 
1. See the double equals sign `==`? We use `==` when checking if two things are the same. We use a single `=` when putting something inside a variable box! 
2. Notice the **Indentation** (spacing). The code under the `if` line *must* be pushed in with the `Tab` key so Python knows it belongs to that decision.

---

## 2. Kid Q&A: "Why do I care?" 🤔

**Kid: Why do games need `if` statements?**
**Teacher:** Imagine playing Minecraft. **If** your health drops to 0, **then** the game runs `print("You died!")`. **If** you hold down 'W', **then** you walk forward. Without `if` statements, games wouldn't be able to react to your controller! 

**Kid: What does `else` mean?**
**Teacher:** `else` is the giant safety net that catches everything else! "If the password is 'dragon', let them in. **Else**, lock them out." It saves you from having to type out every single wrong password in the dictionary!

---

## 3. The AI Connection: Logic vs. AI Brains 🧠

If we use `if/else`, the computer follows exactly what we say forever. 
An AI Agent (like Copilot, Cursor, or Claude) works a bit differently. It guesses the *most likely* next word, rather than following rigid `if` statements.

But for our Agentic Apps, we use them together! We can write Python code that says:
`if user_wants_a_joke == "yes":`
&nbsp;&nbsp;&nbsp;&nbsp;`ask_gemini_for_joke()`

**Prompt Your AI:** *"I have a Python if/elif/else block checking for the weather (sunny, rainy, snowy). Can you write a creative Python program that uses if statements to tell the user what to wear, but make the advice sound like a pirate is giving it?"*

---

## 4. Hands-on Coding 💻

**Action 1:** The Secret Password Door 🚪
Write code that asks the user for a password using `input()`.
If they guess "OpenSesame", print "The treasure room opens!".
If they guess anything else, print "Intruder Alert!"

```python
password = input("Enter the secret password: ")

if password == "OpenSesame":
    print("The treasure room opens! 🪙")
else:
    print("Intruder Alert! 🚨")
```

**Action 2:** Number Guessing Mini-Game 🎲
Let's see if the user can guess our favorite number.
```python
guess = int(input("Guess my favorite number between 1 and 10: ")) # We use int() for numbers!

if guess == 7:
    print("You got it!")
elif guess > 7:
    print("Too high!")
else:
    print("Too low!")
```

---

## 5. 🌟 Challenge of the Day!
Create a **Pokemon/RPG Encounter!** 
Ask the player: "A wild Goblin appears! Do you choose to 'fight' or 'run'?"
Use an `if/elif/else` statement to print what happens based on their choice. What if they type 'dance'? Make sure `else` handles any weird inputs!

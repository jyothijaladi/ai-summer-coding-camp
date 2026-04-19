# 🔢 Week 1, Day 2: Text vs Numbers & Asking Questions 🔡

**Age Group:** 3rd - 8th Grade (Complete Beginners)
**Time:** 1 - 1.5 Hours  

## 👩‍🏫 Teacher's Lesson Plan
1. **(10 min) Review:** Ask the class: "What does `print()` do?" and "What is a variable?"
2. **(20 min) The Lesson:** Explain that computers are incredibly literal. They don't know that "10" (in quotes) is a number. Show them concatenation (gluing strings). Introduce `input()`.
3. **(40 min) Hands-on:** Kids build their first interactive script where the computer talks to them by name!

---

## 1. What are we doing? (The Core Concept) 🏷️

Our magic variable boxes from yesterday can hold different *types* of things. 

The two most important types are:
1.  **Strings (Words/Text):** Always wrapped in quotes. `"Hello"`, `"Monkey"`, `"555"`.
2.  **Integers (Numbers):** Just the raw math number, no quotes! `10`, `42`, `9000`.

### Why does this matter?
Let's see what happens when we try to do math. Type this into your code and Run it!
```python
# Math with Integers (Works perfectly)
score = 10 + 5
print(score)  # This will print 15!

# Math with Strings (Words get glued together!)
funny_word = "10" + "5"
print(funny_word) # This will print 105 !! 
```
When you use a plus sign `+` with Strings (words), the computer literally glues them together like Lego bricks! 

### Asking Questions with `input()` 🎤
Instead of putting a word into a variable ourselves, we can ask the person using the computer to type it in!
```python
user_name = input("What is your name? ")
print("Nice to meet you, " + user_name)
```
*Note: Run this code, click DOWN in the terminal window, type your name, and hit Enter!*

---

## 2. Kid Q&A: "Why do I care?" 🤔

**Kid: Why does it matter if I put quotes around numbers or not?**
**Teacher:** Imagine you are making a game where the player buys a sword for 10 coins. If the computer thinks 10 is a "String word" instead of a "Number", it doesn't know how to subtract it from your wallet! The game will literally crash. Computers are very smart, but also very literal.

**Kid: What is `input()` useful for?**
**Teacher:** Have you ever played a game that asked you to "Type your Username"? Or used a Google Search bar? That is exactly what `input()` does! It freezes the code and waits for the human to type something. 

---

## 3. The AI Connection: Cleaning up Messes ✨

Sometimes users type messy answers. "   JoHn  ", "aLiCE". 
Agentic AI is amazing at cleaning up messy text! Let's ask our AI tool how to clean up a string safely in Python.

**Prompt Your AI:** *"I am writing a Python program where a user types their name using the `input()` command. But what if they type their name with annoying lowercase letters? How can I use Python to automatically capitalize the first letter?"* 

---

## 4. Hands-on Coding 💻

**Action 1:** The Age Calculator Bug! 🐛
Type this code. It will crash! Why? Because `input()` always thinks we are typing a **String Word**, and you can't add math to a word!
```python
age = input("How old are you? ")
next_year = age + 1  # 💥 CRASH! ERROR TIME!
print("Next year you will be: " + str(next_year))
```
**Fix it:** You need to wrap `int()` around the input to tell Python "Turn this word into a math Number!"
```python
age = int(input("How old are you? "))
```

**Action 2:** The Superhero Greeter 🦸
Write a program that asks for:
1. The user's favorite color.
2. The user's hero alias.
Then prints: *"Wow, a [color] cape fits [hero alias] perfectly!"*

---

## 5. 🌟 Challenge of the Day!
Create a "Mad Libs" sentence generator! Ask the user for 1 Noun, 1 Adjective, and 1 Verb using `input()`. Then print out a funny sentence by gluing (`+`) all those words together with spaces in between!

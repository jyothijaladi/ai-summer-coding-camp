# 🛠️ Week 2, Day 10: Project 2 - Smart Quiz Game! 🧠

**Time:** 1 - 1.5 Hours  
**Goal:** Combine Functions, Returns, Loops, and Lists to build a fully working Trivia Game, using Gemini to generate the questions!

---

## 1. The Core Concept: Putting it together 🧩

Today we are building a Trivia Game. We need:
1. A list of questions.
2. A list of correct answers.
3. A `for` loop to ask the questions one by one.
4. A way to track our score (a variable).
5. (Optional!) A function `check_answer(guess, correct)` to keep our code clean!

---

## 2. Step-by-Step Build Guide 📝

### Step A: Use the Agent to write our content!
We don't want to write silly questions manually. Let's use Gemini to generate our content!

**Prompt Gemini:** *"I am making a python quiz game. Can you give me two python lists? One list called `questions` containing 3 fun trivia questions about animals. And another list called `answers` containing the 3 correct answers (as strings). Make sure the order matches exactly!"*

Copy and paste Gemini's code into your file!
```python
# (Your code should look something like this)
questions = ["What animal is the tallest?", "What animal goes meow?", "What animal is a giant fish?"]
answers = ["giraffe", "cat", "whale"] 
```

### Step B: The Setup
Let's set up our variables.
```python
print("🌟 Welcome to the Smart Quiz Game! 🌟")
score = 0
```

### Step C: The Loop
We need a way to loop through our questions. Since we have two lists that match, we will use a regular `for` loop with numbers.
```python
# `len(questions)` gets the length of the list (which is 3)
for i in range(len(questions)): 
    # Grab the current question using `[i]`
    current_question = questions[i]
    correct_answer = answers[i]
    
    # Ask the user!
    guess = input("Question: " + current_question + " \nHint: type answer in lowercase! >>> ")
    
    # Check if they got it right!
    if guess == correct_answer:
        print("✅ CORRECT!")
        score = score + 1
    else:
        print("❌ WRONG! The correct answer was: " + correct_answer)

print("\n--- GAME OVER ---")
print("You scored: " + str(score) + " out of " + str(len(questions)))
```

---

## 3. The AI Connection: The "Agentic" Upgrade 🤖

Right now, your game is cool, but if you play it twice, you get the exact same questions.
A TRUE Agentic game would generate *new* questions every single time you click run! 

While connecting Python directly to an AI API is a bit complex for today, conceptually, in the future, your `questions` list won't be hard-coded. It will be `questions = ask_gemini_for_questions()`. 

**For now:** Ask Gemini to generate a Python List of 10 totally strange and weird questions about space! Replace your old list with this new list and suddenly your game is completely different WITHOUT changing the game logic loops! This separates the *Content* from the *Engine*.

---

## 4. Kid Q&A: "Why is this useful?" 🤔

**Q: Why didn't we just write `print(question 1)`, `input`, `if/else`, `print(question 2)` etc?**
**A:** Imagine a Kahoot quiz with 100 questions! Using a `for` loop and a `List`, our game "engine" is only 15 lines of code, no matter if we have 3 questions or 3,000 questions! The code loops forever until the list is empty. This is how real apps scale up!

---

## 5. 🌟 Challenge of the Day! (Bonus)
Change your game so that it has **Multiple Choice Answers**. 
*Hint: You will need the AI to generate the `questions` list so it looks like "What is the tallest animal? A) Cat, B) Giraffe, C) Dog". And then the `answers` list just contains "b".*

# ↩️ Week 2, Day 7: Return Values (Getting Data Back) 🪃

**Time:** 1 - 1.5 Hours  
**Goal:** Understand how to use the `return` keyword so your functions aren't just printing things, but actually handing data *back* to you!

---

## 1. The Core Concept: The Vending Machine 🥤

Yesterday, our functions were like fireworks 🎆. We gave them instructions, they went off (`print()`), and it was exciting! But what if we want the function to actually give us something useful we can store in a variable? 

Imagine a Vending Machine.
- The **Parameter** is your Dollar bill.
- The **Function** is the machine selecting the soda.
- The **Return Value** is the soda popping out for you to hold!

If the vending machine just printed "Here is your soda" on a screen but didn't drop a can, you wouldn't be very happy!

### Using `return` vs `print`
```python
# A function that only prints
def make_pizza(topping):
    print("Here is your " + topping + " pizza!")
    
make_pizza("cheese") # Nothing is saved...


# A function that RETURNS
def get_secret_code(name):
    secret = name + "12345"
    return secret       # ⬅️ This hands the data back out!

# We can save it in a variable!
my_code = get_secret_code("Alex")
print("My new password is: " + my_code)
```

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Wait, why not just `print()` everything? What’s the difference?**
**A:** `print()` is only for Human eyeballs. The computer looks at text on the screen and forgets it instantly. If you want the computer to USE the result of the function later (like adding damage in a game or saving a high score), you MUST use `return` so the math gets handed back into a variable. 

**Q: Can a function return two things?**
**A:** Yes! It can return a list or a "tuple" of things. But usually, a function has one specific job to return one final answer.

---

## 3. The AI Connection: The Output of an Agent 🧠

When you build real AI applications, the Agent never `prints` to the console. It takes your prompt as a parameter, and it `returns` the fully written essay or generated code back to your Python script! Then your Python script decides what to do with it (like save it to a file, or show it on a website).

**Prompt Gemini:** *"I get confused between `print` and `return` in Python. Can you show me a simple example of a Python function that uses `return` to give back the square of a number, and show me how to save that in a variable?"*

---

## 4. Hands-on Coding 💻

**Action 1:** The Double Trouble function ✖️2️⃣
Write a function that takes a number, doubles it, and returns the answer.
```python
def double_it(num):
    answer = num * 2
    return answer

# Save the return value
my_math = double_it(50)
print(my_math)
```

**Action 2:** Building a simple Password Checker
Write a function that takes a user's `guess`. If the guess is "pizza", return `True`. Otherwise, return `False`.
```python
def check_password(guess):
    if guess == "pizza":
        return True
    else:
        return False

# Now use it!
result = check_password("tacos")
print("Access granted? " + str(result))
```

---

## 5. 🌟 Challenge of the Day!
Write a function called `biggest_number(num_a, num_b)`. 
Use an `if/else` block inside the function to check which number is larger. 
**Return** the larger number. 
Then call your function with two random numbers and print the result!

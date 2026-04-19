# 📦 Week 2, Day 6: Functions & Parameters 🎁

**Time:** 1 - 1.5 Hours  
**Goal:** Learn how to create "boxes" of code that we can use over and over without re-typing them.

---

## 1. The Core Concept: The Code factory 🏭

Imagine you want to bake a cake. You have to get flour, crack eggs, stir it, and bake it.
If you bake a cake every day, you don't want to read the recipe every single time. Instead, you build a "Cake Baking Machine"!

In Python, a **Function** is exactly that. It's a machine where you write the instructions ONCE, and then you can just call the machine's name whenever you want!

### Defining a Function using `def`
Let's build a machine that says a super cool greeting.
```python
# 1. Defining the Function (Building the machine)
def super_greeting():
    print("✨ WELCOME TO THE AWESOME ZONE ✨")
    print("Prepare for amazing code!")

# 2. Calling the Function (Pressing the button on the machine)
super_greeting()
super_greeting()
```
*Note: Just like `if` and `while`, the code inside the function MUST be indented!*

### Parameters: Giving the Machine Ingredients 🥚
What if you want the greeting to use someone's specific name? We use **Parameters**!
```python
def greet_hero(hero_name):
    print("Welcome, mighty " + hero_name + "!")

greet_hero("Batman")
greet_hero("Wonder Woman")
```
*The variable `hero_name` acts like a slot on the machine where we insert the name!*

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Why don't I just use copy and paste instead of a function?**
**A:** Imagine a game like Roblox. When your character jumps, it plays a sound, moves your arms, and changes your height. If jumping was copy-pasted everywhere, and the creator wanted to change the jump sound, they would have to find it 10,000 times! With a `jump()` function, they change the sound ONCE inside the function, and suddenly every jump in the game is updated!

**Q: Why are parameters so helpful?**
**A:** They make your code flexible! A `shoot_laser()` function is cool. A `shoot_laser(color, power)` function means the same code can shoot a red laser that deals 10 damage, OR a blue laser that deals 50 damage!

---

## 3. The AI Connection: AI and Reusable Prompts 🤖

When you build complex AI apps, you will realize that you ask the AI the same questions over and over. "Summarize this string," "Translate this string," "Make this string sound like a pirate."

Writing a python function to talk to Gemini saves you TONS of time! We'll start building these soon.

**Prompt Gemini:** *"I am learning Python functions. Can you write a Python function named `draw_square(size)` that uses a loop to print a square made out of '#' symbols based on the `size` parameter?"*

---

## 4. Hands-on Coding 💻

**Action 1:** The Calculator Function 🧮
Write a function that takes two numbers and adds them together!
```python
def add_numbers(num1, num2):
    answer = num1 + num2
    print("The sum is: " + str(answer))

add_numbers(5, 10)
add_numbers(99, 1)
```

**Action 2:** The Emoji Printer 🎨
Write a function called `print_emojis` that takes two parameters: an `emoji_string` and a `count`. It should use a loop to print that emoji `count` times.

```python
def print_emojis(emoji_string, count):
    for loop_number in range(count):
        print(emoji_string)

print_emojis("🔥", 5)
```

---

## 5. 🌟 Challenge of the Day!
Write a function called `pet_greeter(pet_type, pet_name)`. 
If `pet_type` is "dog", print "Woof woof! Hi [pet_name]!"
If `pet_type` is "cat", print "Meow! Hello [pet_name]!"
Otherwise, print "What a weird pet, [pet_name]..."

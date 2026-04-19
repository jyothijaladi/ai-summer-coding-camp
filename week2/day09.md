# 📋 Week 2, Day 9: Lists (Keeping track of things) 🎒

**Time:** 1 - 1.5 Hours  
**Goal:** Learn how to store lots of items in a single variable box using a Python `List`.

---

## 1. The Core Concept: The Backpack 🎒

So far, our variables can only hold ONE thing. `player_name = "Alex"` holds one name.
But what if you are making a game and the player has an inventory with a Sword, a Shield, an Apple, and a Potion? 
Creating `item1`, `item2`, `item3`, `item4` is annoying. 

Instead, we use a **List**! A List is like a backpack. It's one variable that holds many items in a specific order.
We use square brackets `[]` to make a list.

### Making and using a List
```python
# Create the list
inventory = ["Sword", "Shield", "Apple", "Potion"]

# Print the whole list
print(inventory)

# Print just one item (Computers start counting at 0!)
print("Equipping the " + inventory[0]) # Prints 'Sword'
print("Eating the " + inventory[2])    # Prints 'Apple'
```

### Adding and Removing Items
Your backpack isn't glued shut! You can add (`.append()`) and remove (`.remove()`) things while the game runs.
```python
inventory.append("Magic Ring") # Adds to the end!
print(inventory)

inventory.remove("Apple") # You ate it!
print(inventory)
```

---

## 2. Kid Q&A: "Why is this useful?" 🤔

**Q: Do real games use lists?**
**A:** YES! Every single game uses lists. A list of all the players currently on the server. A list of all the high scores. A list of all the zombies currently alive on the map. Without lists, multiplayer games literally could not exist!

**Q: Why don't they just make 100 variables like `player1`, `player2`?**
**A:** Because you don't know how many players will join! A list can grow and shrink automatically (`append` and `remove`). 

---

## 3. The AI Connection: AI loves Lists ✨

When you ask an AI, "Give me 5 ideas for a youtube video," it will likely give you text. But what if we want to use those ideas in our code? We can ask the AI to output a **Python List**!

**Prompt Gemini:** *"Can you generate a python list containing 5 funny names for a pet dragon? Just give me the python list code, nothing else!"*

*Look at the code Gemini gives you! You can copy and paste that right into your game!*

---

## 4. Hands-on Coding 💻

**Action 1:** The High Score Tracker 🏆
Write a list called `high_scores` with three numbers. Then write a loop that goes through the list and prints them one by one.

```python
high_scores = [100, 450, 9999]

# This is a super powerful loop! It automatically loops for every item in the list!
for score in high_scores:
    print("New Score: " + str(score))
```

**Action 2:** Building a To-Do List!
Let's use a `while` loop to let the user add things to a list forever!
```python
tasks = []
keep_adding = True

while keep_adding == True:
    new_task = input("What do you need to do? (Type 'done' to stop): ")
    if new_task == "done":
        keep_adding = False
    else:
        tasks.append(new_task)
        print("Current tasks:", tasks)

print("Final list:", tasks)
```

---

## 5. 🌟 Challenge of the Day!
Write a list of your top 3 favorite foods.
Then ask the user `input("Guess one of my favorite foods: ")`.
Use the `in` keyword (ask Gemini!) to check if their guess is inside your list! If it is, print "You got it!" If not, print "Nope!"

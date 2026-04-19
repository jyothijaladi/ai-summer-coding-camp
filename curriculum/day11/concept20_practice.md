# 🛠️ Concept 20 Practice: The Unique Vault (Sets)

### 🚀 The 20-Problem Challenge Menu
*Note: Sets are the ultimate way to clean up messy data!*

#### 🟢 Group A: The Set Builders (Warmups)
1.  **Create a Set:** Make a set called `colors` with 3 color names.
2.  **The Proof:** Try to `.add()` the same color twice to your set. Print it and see what happened!
3.  **The Count:** Use `len()` to see how many unique items are in your set.
4.  **Check for Item:** Print `True` if "Blue" is in your set.
5.  **Remove it:** Use `.remove()` to delete an item.

#### 🟡 Group B: The De-Duplicator
6.  **The Messy List:** Create `my_list = [1, 1, 2, 2, 3]`. Turn it into a set.
7.  **Unique Visitors:** Create a set of 5 guest names. Add a name that is already there.
8.  **The Difference:** Create two sets and use `-` to see what is in one but not the other.
9.  **The Combine:** Use `|` (The Union) to merge two sets into one unique master set.
10. **The Intersection:** Use `&` to see which items are in BOTH sets.

#### 🔴 Group C: The Bug Squasher (Fix the Vault)
11. **The Index Error:** `print(my_set[0])` (Explain why this crashed!).
12. **The Method Trap:** `my_set.append("New")` (Fix it—use `.add()`!).
13. **The Colon Mystery:** `my_set = {"a": 1}` (Is this a set? Fix it by removing the dict logic!).
14. **The Unsafe Remove:** `my_set.remove("NotHere")` (Fix it by using `.discard()` instead—it doesn't crash if the item is missing!).
15. **Bracket Mixup:** `my_set = (1, 2, 3)` (Is this a set or a tuple? Change it!).

#### 💎 Group D: The AI Whisperer (Gemini Missions)
16. **The Hashtag Hero:** Ask Gemini: "I have a list of hashtags with duplicates. Give me a one-line Python code to make them all unique."
17. **The Speed Champion:** Ask Gemini: "Why is searching a Set faster than searching a List in Python?"
18. **The Math Pro:** Ask Gemini: "What are 'Union' and 'Intersection' in Python Sets? Show me an example with two friend lists."
19. **The Real-World Modeler:** Ask Gemini: "How does a website like Reddit use Sets to make sure you only upvote a post once?"
20. **The Challenge:** Ask Gemini: "Give me a hard Python challenge where I have to compare two sets of lottery numbers."

---

### 🌟 Stretch Goal for "Flash" Students
Build a **"Unique Guest Book"**! 
1. Create an empty set `guests`.
2. Use a `while` loop to ask the user for names.
3. Every name gets added to the set.
4. If they enter a name that is ALREADY there, print "You're already on the list, {name}!"
5. At the end, print the total count of unique guests!

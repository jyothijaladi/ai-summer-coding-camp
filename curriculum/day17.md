# 🏰 Day 17: Project - The Haunted House Builder

**Time:** 9:00 AM - 12:00 PM
**Daily Goal:** Build a game where the user can "design" a haunted house and save it to a file for a friend to play!

---

## 🕒 9:00 AM – 10:40 AM: 🛠️ Guided Build – Creating the Map
*Learning how to store a world in a file.*

1.  **The Concept:** 
    - We will use `input()` to ask for the name of a room and a description (e.g., "Kitchen: Smells like old pizza"). 
2.  **Saving the Map:**
    - Every time the user creates a room, we append it to `house.txt` in a specific format: `RoomName | Description`.
3.  **The AI Connection:**
    - Ask Gemini: "I'm building a haunted house game. Give me 3 spooky descriptions for rooms like a basement, an attic, and a hallway."

---

## 🕒 10:40 AM – 11:00 AM: 🥤 Mini-Break / Buffer

---

## 🕒 11:00 AM – 12:00 PM: 🏝️ The Sandbox Exploration (Project Finishing)
*Goal: Build the "Game Reader" to play through your house.*

**Challenges for the Students:**
1.  **The Decorator:** Add a feature where the user can also chose a "Monster" for each room. Save it to the file along with the description.
2.  **The Explorer:** Write a function that reads `house.txt` and prints each room one by one, like a guided tour. 
3.  **The AI Boss Fight:** 
    - Open Antigravity Gemini.
    - Prompt: "I have a file with lines like 'Basement | Spooky'. How do I use the `.split('|')` command in Python to separate the room name from the description?"

---

### 🏆 Milestone:
*Students who finish can swap their `house.txt` files with a neighbor and see if they can "Escape" each other's haunted houses!*

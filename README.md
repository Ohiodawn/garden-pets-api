# 🌱 Grow a Garden: Pets API for Roblox

Welcome to the **Grow a Garden Pets API** — a lightweight, JSON-based resource that lists pet data and visual assets used in the Grow a Garden Roblox game. This API is ideal for tracking pets, generating UI, or building companion tools.

---

## 🐾 What's Included

- `pets.json`: A structured list of pets including:
  - `id`: unique identifier  
  - `name`: pet name  
  - `rarity`: Common, Uncommon, Rare, Legendary, Mythical, Bug, Event, or Craftable  
  - `icon`: relative path to the PNG icon  
  - `skill`: the pet’s in‑game ability or effect  

- `/icons/`: Icon images (PNG) for each pet (low-res, web-optimized)

---

## 📦 Example Pet Entries

```json
[
  {
    "id": "dog",
    "name": "Dog",
    "rarity": "Common",
    "icon": "icons/dog.png",
    "skill": "Attempts to dig up a seed with a 10% success chance." 
  },
  {
    "id": "golden-lab",
    "name": "Golden Lab",
    "rarity": "Common",
    "icon": "icons/golden-lab.png",
    "skill": "Has a 10% chance of digging up a seed every minute; success rate increases as the pet ages." 
  },
  {
    "id": "bunny",
    "name": "Bunny",
    "rarity": "Common",
    "icon": "icons/bunny.png",
    "skill": "Looks for a carrot every 40 seconds; if found, eats it to auto‑sell at 1.5× base value (only works if carrots are planted)." 
  }
]

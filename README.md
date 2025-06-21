# 🌱 Grow a Garden: Pets API for Roblox

A lightweight, JSON‑based resource that lists all pet data and visual assets used in the Grow  a  Garden Roblox game. Ideal for in‑game trackers, companion dashboards, or external tools.

---

## 🐾 What’s Included

* **`pets.json`**
  An array of pet objects with these fields:

  * `id` (string): Unique identifier
  * `name` (string): Pet’s in‑game name
  * `rarity` (string): Common, Uncommon, Rare, Legendary, Mythical, Bug, Event, or Craftable
  * `icon` (string): Path to the self‑hosted PNG in `/icons/`
  * `skill` (string): Pet’s in‑game ability or effect

* **`/icons/`**
  PNG icons for each pet (web‑optimized, 64×64px)

* **`ASSETS.md`**
  Table of icon attributions and licenses

* **`LICENSE.md`**

  * **Code & JSON**: MIT License
  * **Icons & Images**: CC BY‑SA 4.0 (community content)

---

## 📋 Folder Structure

```
grow-a-garden-data/
├── pets.json
├── icons/
│   ├── dog.png
│   ├── golden-lab.png
│   ├── bunny.png
│   └── …other pets…
├── ASSETS.md
├── LICENSE.md
└── README.md
```

---

## 📜 Example `pets.json` Entry

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
    "skill": "10% chance per minute to dig up a seed; success rate increases as the pet ages."
  },
  {
    "id": "bunny",
    "name": "Bunny",
    "rarity": "Common",
    "icon": "icons/bunny.png",
    "skill": "Searches for a carrot every 40 s; if found, auto‑sells it at 1.5× base value."
  }
]
```

---

## 🌐 Usage

Fetch and consume the full list of pets in one call:

```js
fetch("https://yourusername.github.io/grow-a-garden-data/pets.json")
  .then(res => res.json())
  .then(pets => {
    pets.forEach(p => {
      // Example: render each pet card
      const card = document.createElement("div");
      card.innerHTML = `
        <img src="${p.icon}" alt="${p.name}" />
        <h3>${p.name}</h3>
        <p>Rarity: ${p.rarity}</p>
        <p>Skill: ${p.skill}</p>
      `;
      document.body.appendChild(card);
    });
  });
```

> **Versioning tip**: For future breaking changes, move to `/v1/pets.json`, `/v2/pets.json`, etc.

---

## ⚠️ License & Attribution

### Code & Data

Released under the **MIT License**. See [`LICENSE.md`](LICENSE.md).

### Icons & Images

Community content from Grow  a  Garden Fandom is under **CC BY‑SA 4.0**. See [`ASSETS.md`](ASSETS.md) for full attributions. You must:

1. Provide credit with a link to the original Fandom “File:” page.
2. Distribute any derivatives under **CC BY‑SA 4.0**.

---

## 📢 Contact & Contributions

* **Issues & Feature Requests**: Open a GitHub issue
* **Pull Requests**: Welcome — please follow the existing JSON schema
* **Email**: [p07096602@gmail.com](mailto:p07096602@gmail.com)

---

🌼 Happy gardening!

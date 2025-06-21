🌱 Grow a Garden: Pets API for Roblox

A lightweight, JSON-based resource that lists all pet data and visual assets used in the Grow a Garden Roblox game. Ideal for in-game trackers, companion dashboards, or external tools.

🐾 What’s Included

pets.json

An array of pet objects with these fields:

id (string) – Unique identifier

name (string) – Pet’s in-game name

rarity (string) – Common, Uncommon, Rare, Legendary, Mythical, Bug, Event, or Craftable

icon (string) – Path to the self-hosted PNG in /icons/

skill (string) – Pet’s in-game ability or effect

/icons/

PNG icons for each pet (web-optimized, 64×64px)

ASSETS.md

Table of icon attributions and license details

LICENSE.md

MIT License for code and data

LICENSE-CCA.md

Creative Commons Attribution-ShareAlike 4.0 License for images

📋 Folder Structure

garden-pets-api/
├── pets.json
├── icons/
│   ├── dog.png
│   ├── golden-lab.png
│   ├── bunny.png
│   └── …other pets…
├── ASSETS.md
├── LICENSE-MIT.md
├── LICENSE-CCA.md
└── README.md

📜 Example pets.json Entry

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
    "icon": "icons/golden_lab.png",
    "skill": "Occasionally digs up a random seed at a higher chance."
  }
]

🌐 Usage

Once hosted on GitHub Pages, you can fetch and consume the full list of pets in one call:

fetch("https://Ohiodawn.github.io/garden-pets-api/pets.json")
  .then(res => res.json())
  .then(pets => {
    pets.forEach(p => {
      const card = document.createElement("div");
      card.innerHTML = `
        <img src="https://Ohiodawn.github.io/garden-pets-api/${p.icon}" alt="${p.name}" />
        <h3>${p.name}</h3>
        <p>Rarity: ${p.rarity}</p>
        <p>Skill: ${p.skill}</p>
      `;
      document.body.appendChild(card);
    });
  });

🗂 Versioning tip: For future breaking changes, consider using /v1/pets.json or versioned folders.

⚠️ License & Attribution

Code & Data

Released under the MIT License. See LICENSE.md.

Icons & Images

Community content from Grow a Garden Fandom is under CC BY-SA 4.0. See ASSETS.md for full attributions.

You must:

Provide credit with a link to the original Fandom File page.

Distribute any derivatives under CC BY-SA 4.0.

📢 Contact & Contributions

Issues & Feature Requests: Open a GitHub issue

Pull Requests: Welcome! Please follow the existing JSON schema

🌼 Happy gardening!


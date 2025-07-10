# WackyFlip-Avatars

**Player Avatars, Skins & Customization System**
Centralized library for all Wacky Flip character avatars, skins, cosmetic animations, and the systems that manage customization, rendering, and player inventory.

---

## 🎯 Overview

`WackyFlip-Avatars` powers the **visual identity of players** across the entire [Wacky Flip](https://wackyflip.com/) universe. It contains sprite assets, animated character rigs, customizable gear, and all logic needed to load, render, and manage avatars across platforms.

Whether a player is flipping through chaos as a “Rainbow Noob” or unlocking seasonal skins, this repository enables those experiences with scalable, reusable systems for avatar management.

---

## 🎨 Features

* 🧢 **Avatar Metadata System**
  Unique identifiers, categories, rarities, and unlock conditions for each character.

* 🕶️ **Skin Collections**
  Modular outfits, hats, accessories, and effects — including seasonal or limited-edition skins.

* 🎮 **Animation Assets**
  Flip cycles, emotes, idle poses, and win/fail reactions (supporting 2D sprites and 3D rigs).

* 🎛️ **Customization Logic**
  Equip, preview, and persist avatar loadouts across games and devices.

* 🎯 **UI Components for Selection**
  Includes avatar preview renderers and drag/drop or grid-style selectors.

---

## 📁 Directory Structure

```
WackyFlip-Avatars/
├── assets/
│   ├── base/                # Core avatar sprite sheets
│   ├── skins/               # Alternate skins and accessories
│   └── animations/          # Walk, flip, idle, taunt cycles
├── config/
│   ├── avatars.json         # Avatar metadata
│   ├── skins.json           # Outfit definitions
│   └── unlocks.json         # Rules for skin availability
├── src/
│   ├── render/              # Avatar preview and animation renderer
│   ├── logic/               # Equip/save/load customization logic
│   └── ui/                  # Avatar selection and shop widgets
├── docs/
│   └── CONTRIBUTING.md
├── README.md
└── LICENSE
```

---

## 🧬 Example: Avatar Metadata

```json
{
  "id": "noob_classic",
  "name": "Classic Noob",
  "rarity": "common",
  "unlock": "default",
  "category": "starter",
  "animations": ["flip", "idle", "celebrate"]
}
```

---

## 🧥 Usage Example (React + Tailwind)

```tsx
import { AvatarPreview, SkinSelector } from '@wackyflip/avatars';

function ProfilePage() {
  return (
    <>
      <AvatarPreview avatarId="rainbow_warrior" animation="flip" />
      <SkinSelector onSelect={(skinId) => saveSelection(skinId)} />
    </>
  );
}
```

---

## 🔁 Integration Targets

* [`WackyFlip-Web`](https://github.com/wackyflipgame/WackyFlip-Web) – Avatar rendering on profile and leaderboard pages
* [`WackyFlip-Mobile`](https://github.com/wackyflipgame/WackyFlip-Mobile) – Avatar picker and preview in-game
* [`WackyFlip-Stats`](https://github.com/wackyflipgame/WackyFlip-Stats) – Storing owned/unlocked skins
* [`WackyFlip-Tournaments`](https://github.com/wackyflipgame/WackyFlip-Tournaments) – Rewarding special avatars

---

## 🔄 Supported Formats

* `.png` / `.webp` sprite sheets
* `.json` animation maps (custom or Lottie)
* `.glb` for 3D models (in progress)
* `.svg` for lightweight icons and UI badges

---

## 💡 Contribution Guidelines

Want to design a new character?

* Submit your assets to `assets/skins` with metadata in `skins.json`.
* Include sprite sheet previews and animation frames.
* All submissions must be original or properly licensed.

Refer to `docs/CONTRIBUTING.md` for detailed format and style requirements.

---

## 📦 Tech Stack

* React + TypeScript
* Tailwind CSS
* Node.js tools for asset optimization
* Lottie/Spine (animation export support)
* Vite + Storybook (for UI testing)

---

## 🧾 License

MIT License © Wacky Flip Studios
All original avatar assets are © their respective creators or Wacky Flip unless otherwise stated.

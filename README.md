# Awesome Gemini 3.0 Pro Game Collection

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![Status](https://img.shields.io/badge/status-Experimental-orange)

## 📖 Introduction

**Awesome Gemini 3.0 Pro Game Collection** is an open-source experimental project that pushes the boundaries of Web technologies fused with Generative AI.

Our goal is simple: **To integrate multiple innovative gameplay mechanics driven by AI into a single web portal.** We combine Three.js/WebGL for high-performance graphics with Large Language Models (like Gemini 3.0 Pro) acting as the "God Engine" to generate narratives, visual assets (SVG/Pixel Art), and logic code in real-time.

> **Core Philosophy:** Games shouldn't be limited to pre-baked content. Your API Key is the passport to an infinite world.

-----

## 🎮 Playable Games (Available Now)

You can play these games directly by opening the corresponding HTML files in your browser.

### 1. ☯️ Karma Flow (Bazi Roguelike)
**Files:** `game/KarmaFlow.html` (CN), `game/KarmaFlow_en.html` (EN)

* **Genre:** Chinese Metaphysics Roguelike / Deck Building
* **Language:** 🇨🇳 Chinese & 🇺🇸 English
* **Gameplay:**
    * **Bazi Deck Building:** Your birth date (Four Pillars of Destiny) is randomly generated. The Five Elements (Metal, Wood, Water, Fire, Earth) determine your stats.
    * **Cycles of Luck:** Survive "Bad Luck Years" and dominate "Golden Ages" using elemental interactions (Creation/Destruction cycles).
* **Play:**
    * [🇨🇳 Play Chinese Version](./game/KarmaFlow.html)
    * [🇺🇸 Play English Version](./game/KarmaFlow_en.html)

![Karma Flow](./svger/karma-flow.svg)

### 2. 🧪 Element AI (Chemlab)
**Files:** `game/Chemlab.html` (EN), `game/ElementChemistry.html` (CN)

* **Genre:** AI-Powered Alchemy / Synthesis Puzzle
* **Language:** 🇨🇳 Chinese & 🇺🇸 English
* **Gameplay:**
    * **Infinite Synthesis:** Start with basic elements. Combine them to create anything in the universe.
    * **AI Adjudication:** Unlike traditional synthesis games with fixed recipes, the **AI determines the result** of your combinations in real-time based on chemical logic and creativity.
* **Play:**
    * [🇺🇸 Play English Version (Chemlab)](./game/Chemlab.html)
    * [🇨🇳 Play Chinese Version (Element Chemistry)](./game/ElementChemistry.html)
    * *(Alternative CN Version: [ElementAl](./game/ElementAl.html))*

### 3. ⚔️ Sky Voxel Drifter
**File:** `fly.html`

* **Genre:** 3D Action / Parkour
* **Gameplay:**
    * A high-performance web experience of "Minecraft + Elytra Flight".
    * Experience ultimate aerodynamics, use fireworks for boosting, and drift through procedurally generated floating islands.
* **Tech Stack:** Three.js, Cannon.js (Physics).
* **Play:** [✈️ Launch Flight Simulator](./fly.html)

![Sky Voxel](./svger/sky-voxel.svg)

-----

## 🚧 In Development / Roadmap

The following modules are in active research and development:

### 🌌 The Infinite Text Dungeon
* **Concept:** An AI-Native RPG where your wildest actions ("Try to convince the slime to invest in Bitcoin") are rationalized by the AI to drive the plot.
* **Status:** *Coming Soon*
![Text Dungeon](./svger/text-dungeon.svg)

### 🏙️ Dream City Builder
* **Concept:** Text-to-City idle builder where Gemini 3.0 generates SVG building codes in real-time.
* **Status:** *Coming Soon*
![City Builder](./svger/city-builder.svg)

-----

## ⚙️ Architecture & Config

This project adopts an **"AI-Optional"** architecture. Core game logic runs locally, while AI features enhance the experience via API.

### Global Settings Panel

In the games (specifically AI-enabled ones), look for the ⚙️ icon to configure:

```json
{
  "ai_provider": "custom", // or "gemini", "openai"
  "base_url": "[https://generativelanguage.googleapis.com/v1beta/openai/](https://generativelanguage.googleapis.com/v1beta/openai/)",
  "api_key": "sk-proj-...",
  "model_name": "gemini-1.5-pro-latest",
  "image_generation_enabled": true
}
```

-----

## 🚀 Getting Started

Since these are standalone WebGL/HTML5 applications, you have two ways to run them:

### Method 1: Direct Play

Simply navigate to the folder and double-click the `.html` files listed above to open them in your default browser (Chrome/Edge recommended).

### Method 2: Developer Mode

If you want to contribute or modify the code:
```bash
# 1. Clone the repository
git clone [https://github.com/your-username/awesome-gemini-game.git](https://github.com/your-username/awesome-gemini-game.git)

# 2. Navigate to directory
cd awesome-gemini-game

# 3. Install dependencies (if backend/bundling is required)
npm install

# 4. Start local server
npm run dev
```
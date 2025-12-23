# ⚛️ Synthesis - Changelog

### 📦 Release: The "Elementary Engineering" Update

> "We don't do magic. We do Chemistry." — WolfHydra

| Build | Date | NeoForge |
| :--- | :--- | :--- |
| **alpha-0.2.0** | **2025-12-23** | **1.21.1** |

---

## 🔥 Highlights

This update marks the mod's transition from "basic resources" to **Technological Gadgets** based on real physicochemical properties.

* ✨ **4 New Scientific Gadgets** implemented.
* 🎨 **Complete Visual Overhaul** of the Tooltip system (RGB/Gradients).
* 📡 **Tactical HUD** implemented for scanning items.

---

## 🛠️ New Features

### 🔵 Sodium (Na) - Thermodynamics
**New Item: Sodium Thermal Siphon**
* **Fluid Mechanic:** Absorbs Lava and Magma Blocks from the world using RayTracing, storing internal heat.
* **Injection Mechanic:** `Shift + Right Click` on furnaces performs an **Insta-Smelt**, injecting heat directly into `cookingProgress` via Java Reflection.
* **Visual:** A colored durability bar (Orange) indicates thermal charge (0-1000°C).

### 🟢 Beryllium (Be) - Geo-Resonance
**New Item: Beryllium Tectonic Resonator**
* **Mechanic:** Long-range biome scanner (6.4km radius).
* **Calibration:** `Shift + Click` on a block saves the current biome signature.
* **HUD System:** While holding the item, a tactical overlay appears on the screen showing the target biome, found coordinates, and real-time distance.

### 🟡 Potassium (K) - Life Support
**New Item: Potassium Superoxide Canister**
* **Real Chemistry:** Simulates the actual chemical reaction: `4KO2 + 2CO2 → 3O2`.
* **Mechanic:** Automatically restores oxygen when the player is submerged.
* **Audio Loop:** Emits a rhythmic mechanical breathing sound (via Server Tick) during use.

### 🔴 Lithium (Li) - Portable Energy
**New Item: Lithium-Ion Accumulator**
* **Mechanic:** Passive inventory battery. Repairs other damaged items in the player's inventory every second.

---

## 🎨 UI & UX Improvements

### 🌈 Tooltip Rendering Engine v2.0
A complete rewrite of the item description renderer (`TooltipHandler.java`).

* **Palette System:** Themed colors defined by chemical element:
    * 🔴 **Lithium:** Fire Red
    * 🟢 **Beryllium:** Emerald Green
    * 🔵 **Sodium:** Electric Blue
    * 🟣 **Potassium:** Purple/Violet
    * ⚪ **Magnesium:** Metallic White
* **Visual Effects:**
    * Dynamic Vertical Gradient borders.
    * Animated Chroma/RGB support for High-Tech items (like the Resonator).

---

## ⚙️ Technical Changes (Under the Hood)

* **Data Components (1.21):** Complete migration from old NBT Tags to the new `DataComponents.CUSTOM_DATA` system. This ensures secure and modern data persistence (coordinates, heat, target biome).
* **LayeredDraw API:** Implementation of the Beryllium HUD using the new NeoForge 1.21 GUI rendering API (replacing the deprecated `IGuiOverlay`).
* **Reflection:** Implementation of secure access to private fields (`litTime`, `cookingTotalTime`) of furnace TileEntities to allow advanced manipulation of vanilla logic.
* **Refactoring:** Cleaned and modularized code (Registry pattern) to facilitate adding new elements in the future.

---

## 🐛 Bug Fixes

* **FIX:** Corrected the chemical symbol for Potassium in descriptions (Was N, now is K).
* **FIX:** Corrected inverted logic of the Thermal Siphon (Shift+Click now prioritizes furnace injection).
* **FIX:** Resolved compilation crash due to incorrect `VanillaGuiOverlay` imports.
* **FIX:** Resolved syntax errors ("illegal start of expression") in the Tooltip handler.

---
**Synthesis Mod** - Science over Magic.

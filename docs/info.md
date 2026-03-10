<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## 🔹 How It Works
- The circuit uses **DIP switches** (IN0–IN3) as inputs to form a secret code (`1010`).  
- These inputs are processed through **NOT gates** (to handle “must be 0” conditions) and cascaded **AND gates** to generate an **unlock signal**.  
- The unlock signal is then **inverted** to match the active‑low nature of the 7‑segment display.  
- When the correct code is entered, the inverted unlock drives the segments **a, b, c, e, f, g**, forming the letter **M**.  
- Any other DIP combination leaves the display blank.

## 🔹 How to Test
1. **Set DIP switches** to the secret code (`1010`).  
   - IN3 = ON (1)  
   - IN2 = OFF (0)  
   - IN1 = ON (1)  
   - IN0 = OFF (0)  
2. Observe the 7‑segment display: the letter **M** should appear.  
3. Flip any switch away from the code → the unlock signal goes LOW → display turns OFF.  
4. Optional: Try different codes by rewiring the AND/NOT logic to check other patterns.

## 🔹 External Hardware Used
- **DIP Switch (4‑bit)** → for inputting the secret code.  
- **Logic Gates (AND, NOT)** → to detect the correct input pattern.  
- **7‑Segment Display (common cathode or common anode, depending on wiring)** → to show the letter.  
- **Resistors (10k pull‑up/pull‑down)** → for stable DIP switch operation.  
- **Push Buttons (optional)** → for reset or clock stepping if you expand the design.  
- **Breadboard + Jumper Wires** → for prototyping.  
- **Power Supply (5V VCC + GND)** → to drive the logic and display.


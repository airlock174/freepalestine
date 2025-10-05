# FreePalestine — Max/MSP patch (v1.1)

## About
This Max/MSP patch provides a custom skin for `number` boxes, stylising them as the Palestinian flag.  
On bang, it scripts three `panel` objects (black, white, green) aligned to the number box.  
The patch sets the number’s background alpha to 0, recolors the built-in triangle to red, and makes the text bold with a slightly darker red tone for better legibility.

Version 1.1 introduces compatibility with `@presentation 1` objects, an internal logic rewrite, and a new **variant 2 (triscale 1.8)** with proportions closer to the real flag.

---

## Instructions
1. De-encapsulate this patcher in the target patch (in **Patching Mode**).  
2. Connect the target number box:  
   - to the **2nd outlet** of `getattr`  
   - to the **1st outlet** of `p free`  
3. Choose **ver.1** or **ver.2** from the menu.  
4. Press the **bang** button to create the panels.  
5. Select the number and the three panels, then choose **Group Objects**.  
6. If you move the number manually, delete the panels and bang again (manual moves cause rounding, which may create small gaps).  
7. Optionally, press **reset colors** to restore the default number colors (delete the panels manually if needed).

---

## Changes in v1.1
- Added compatibility with objects using `@presentation 1`.  
- Rewritten internal logic using `uzi`, `sprintf`, and `deferlow`.  
- Introduced **variant 2** with `triscale 1.8` for more accurate flag proportions.  
- Added visual arrows indicating connection outlets.  
- Added **color reset** option.  
- Corrected red tone from `255 0 0` to `238 42 53`.

---

## Notes
- Works with both **int** and **float** number boxes.  
- Tested in **Max 9.0.5**.  
- Design modifications applied to the number box:  
  - transparent background (alpha 0)  
  - red built-in triangle  
  - bold text in slightly darker red for contrast  
- The chevron uses the number’s built-in triangle rather than a custom polygon.  
- Suitable for live performances, installations, or symbolic interface design.

---

## License
- **MIT License** — for patch logic and code.  
- **CC-BY 4.0** — for documentation and images.

---

## Preview
<img width="1133" height="427" alt="Immagine 2025-10-05 175804" src="https://github.com/user-attachments/assets/6ac097e7-63b4-49cd-8a27-338e734c9668" />


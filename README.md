# freepalestine — Max/MSP Patch (v1.2)

## Overview

**freepalestine** is a Max/MSP patch that applies a custom visual style to number boxes, using the colors of the **Palestinian flag**.  
On *bang*, it scripts three aligned panel objects (black, white, and green) and restyles the number box to create a symbolic, minimal visual design.

---

## Features

- Automatic creation of black, white, and green panels aligned with the number box
- Transparent number box background (`alpha 0`)  
- Red built-in triangle (chevron): **ver.1** = default triscale; **ver.2** = triscale 1.8 
- Bold text in a slightly darker red for contrast  
- Works with both `int` and `float` number boxes  
- Non-destructive: does not modify the number box’s core parameters  
- Includes a **clear** function to restore default appearance and remove spawned panels  

---

## Instructions

1. **De-encapsulate** this patcher inside the target patch (in *Patching Mode*).  
2. Connect the **target number box**:
   - to the **2nd outlet** of `getattr`
   - to the **1st outlet** of `p free`
3. Select **ver.1** or **ver.2** from the *umenu*.  
4. Press the **bang** to apply the flag design.  
5. Each activation removes previously spawned panels at the same position before creating new ones.  
6. Select the number box and the three panels, then choose **Group Objects**.  
7. Delete this patcher after grouping.  
8. If necessary, press **clear** to restore the default number box colors and remove panels in their spawn position.

> Panels that have been moved from their original position are not deleted automatically and must be removed manually if necessary.

---

## Technical Notes

- Compatible with both integer and float number boxes.  
- Tested with **Max 9.0.5**.  
- Uses built-in Max scripting for UI element creation and deletion.  
- No external dependencies or third-party objects required.  
- The patch modifies only visual attributes — all functional behavior remains unchanged.

---

## License

- **MIT License** — for patch logic and code  
- **CC-BY 4.0** — for documentation and images

---

## Preview
<img width="1496" height="613" alt="Immagine 2025-10-06 232130" src="https://github.com/user-attachments/assets/73683cdd-4fb3-4662-9b5f-0280c76309f4" />

---

## Credits

Developed as an open-source Max/MSP resource for creative interface design and visual expression.  
This patch may be freely used, studied, and modified under the terms of its license.





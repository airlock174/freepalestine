# freepalestine — Max/MSP UI Patch (v1.2)

> A Max/MSP patch that reimagines the number box as a symbol of visual solidarity, restyled in the colors of the Palestinian flag and intended for public-facing creative works.


---

## Overview

**freepalestine** is a Max/MSP patch that restyles number boxes using the colors of the **Palestinian flag**.  
When triggered by a `bang`, it automatically creates three aligned panel objects (black, white, and green) and modifies the number box appearance to achieve a minimal, symbolic visual design.  
A dedicated **clear** `bang` is also provided to restore the default appearance and remove the panels.

---

## Features

- Applies the **colors of the Palestinian flag** to Max number boxes, generating aligned **black**, **white**, and **green** panel layers beneath the box and coloring its built-in triangle **red** to create a unified visual design.  
  - **Color palette (RGB):** **red** `238-42-53`, **black** `0-0-0`, **white** `255-255-255`, **green** `0-151-54`  
  *(based on widely referenced sources such as Wikimedia/Wikipedia; no officially codified color standard is documented)*  
  - **ver.1** — uses the default `triscale 1.`, keeping the number box’s default geometry with the triangle detached from the left edge 
  - **ver.2** — uses `triscale 1.8`, adjusting panel length and alignment for a geometry closer to the actual layout of the Palestinian flag
- Transparent number box background (`alpha 0`) with **bold dark-red text** for visual contrast  
- Panels automatically adapt to the **size** of the connected number box  
- Compatible with objects using `@presentation 1` — correctly distinguishes and supports both `patching_rect` and `presentation_rect`  
- Automatically replaces previously spawned panels at the same position, allowing multiple flag generations or design variations without overlap  
- Non-destructive: preserves all number box parameters  
- Includes a dedicated **clear** `bang` to restore the default appearance and remove panels spawned at the same position

---

## Requirements

- Tested with **Max 9.0.5** (should work on 8.5+).  
- No external dependencies or third-party objects required.

---

## Installation

1. **De-encapsulate** this patcher inside your target patch (in *Patching Mode*).  

---

## Usage

1. Connect the **target number box**:
   - to the **2nd outlet** of `getattr`  
   - to the **1st outlet** of `p free`
2. Select the desired version (`ver.1` or `ver.2`) from the `umenu`, then press the `bang` to apply the flag-style design.  
   Each activation removes previously spawned panels at the same position before creating new ones.  
3. Select the number box and the three panels, then choose **Group Objects**.  
4. Delete this patcher after grouping.  

---

## Cleanup

If needed, press **clear** to restore the default number box colors and remove all panels in their spawn position.  
Panels moved from their original position are not automatically deleted and must be removed manually if necessary  
— addressing this limitation would require embedding a JavaScript file, which would compromise the patch’s standalone nature.

---

## Technical Notes

- Compatible with both integer and float number boxes  
- Uses native Max scripting for UI element creation and cleanup  
- In **ver.2**, panel positioning includes a small horizontal offset relative to the triangle to prevent antialiasing artifacts  
- Fully supports both **Patching** and **Presentation** modes  
- Modifies only **visual attributes** — functional behavior remains unchanged  

---

## License

- **MIT License** — for patch logic and code  
- **CC-BY 4.0** — for documentation and images

---

## Preview
<img width="1496" height="613" alt="Immagine 2025-10-06 232130" src="https://github.com/user-attachments/assets/45671241-e224-4f1c-b3cc-ee569350fe1f" />

*The patch as it appears when opened in Max — showing the two available flag versions (“ver.1” and “ver.2”).*

---

## Credits

Developed as an open-source resource for **creative interface design** and **visual expression** in Max/MSP.  
You are free to use, study, and modify this patch in accordance with the license terms.

---

## Support

If you enjoy this patch or find it useful, consider giving the repository a ⭐ on GitHub.  
It helps increase visibility for independent creative tools and supports open-source interface design projects like this one.

This patch was conceived as an open invitation to students, performers, and educators to incorporate acts of visual solidarity into their public-facing work — in exams, concerts, or installations where the patch appears on screen.  
In times when gestures of empathy and awareness matter deeply, even small design choices can become meaningful statements.

---

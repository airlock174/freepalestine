# FreePalestine — Max/MSP patch

## About
This Max/MSP patch repurposes a number box as a stylised Palestinian flag. On bang it scripts three `panel` objects (black, white, green) aligned to the number. The patch sets the number’s background alpha to 0, recolors the built-in triangle to red, and makes the number text bold and a slightly darker red for legibility.

## Instructions
1. De-encapsulate this patcher in the target patch.  
2. Connect the number box:  
   - to the 2nd outlet of `getattr patching_rect`  
   - to the 1st outlet of `p freepalestine`  
3. Bang to spawn the panels.  
4. Select the number + the three panels and choose **Group Objects**.  
5. If you move the number manually, delete the panels and bang again (manual moves cause rounding, which may create gaps between stripes).

## Notes
- Works with both **int** and **float** number boxes.  
- Tested in Max 9.0.5.  
- Design choices applied to the number box:  
  - transparent background (alpha 0)  
  - red triangle (chevron)  
  - bold text, red with a slightly darker tone for readability  
- Intentionally stylised: the chevron is the recolored built-in triangle rather than a drawn polygon.  
- Suitable for performances, installations, or generative/visual art.

## License
MIT License (for the code).  
Creative Commons Attribution (CC-BY) for documentation and media.

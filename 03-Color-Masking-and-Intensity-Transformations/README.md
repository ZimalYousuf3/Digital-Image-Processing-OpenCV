# 03 - Color Masking and Intensity Transformations

Part of the **Digital Image Processing with OpenCV** lab series.

## Overview
This lab covers two core ideas:
1. **Color masking in HSV:** isolating or removing a color from an image.
2. **Intensity transformations:** changing image brightness with pointwise formulas.

## Topics Covered

### Part A: Color Masking (HSV)
- BGR to HSV conversion
- Creating binary masks with `cv2.inRange()`
- Extracting colors with `cv2.bitwise_and()`
- Removing colors with mask inversion (`cv2.bitwise_not()`)

### Part B: Intensity Transformations (Grayscale)
| Transform | Formula | Effect |
|---|---|---|
| Negative | `s = 255 - r` | Inverts brightness |
| Log | `s = c * log(1 + r)` | Enhances dark regions |
| Gamma | `s = 255 * (r / 255)^γ` | γ < 1 brightens, γ > 1 darkens |

Each transform includes a pixel level check and a side by side comparison.

## Why HSV?
HSV separates color (Hue, Saturation) from brightness (Value), which makes color selection more stable when lighting changes.

## Key Functions
- `cv2.cvtColor()`
- `cv2.inRange()`
- `cv2.bitwise_and()` / `cv2.bitwise_not()`
- `np.log1p()`, `np.clip()`, `np.hstack()`

## Requirements
```
opencv-python
numpy
matplotlib
```

## How to Run
1. Open the notebook in Google Colab.
2. Run the setup cell and upload the two images when asked:
   - **Image A:** a colorful photo (for masking)
   - **Image B:** a photo with dark and bright areas (for intensity transforms)
3. Run the remaining cells in order.

## Files
- `03_Color_Masking_and_Intensity_Transformations.ipynb`: lab notebook

## Notes
- OpenCV Hue ranges from 0 to 179.
- Red wraps around the hue circle, so a complete red mask needs two ranges. This lab uses the lower range (0-10) for simplicity.

## Course Info
Digital Image Processing Lab, BS(CS), 3rd Semester
Fazaia Bilquis College of Education for Women, PAF Nur Khan, Rawalpindi

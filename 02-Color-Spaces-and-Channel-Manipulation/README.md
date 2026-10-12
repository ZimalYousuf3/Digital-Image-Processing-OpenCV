# Color Spaces and Channel Manipulation

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ZimalYousuf3/Digital-Image-Processing-OpenCV/blob/main/02-Color-Spaces-and-Channel-Manipulation/02_Color_Spaces_and_Channel_Manipulation.ipynb)

## Objective

Understand how color images are stored and practise working with the BGR, RGB, HSV and LAB color spaces using OpenCV and NumPy.

## Topics Covered

| Topic | Description |
|---|---|
| Image loading | Read an image in BGR and validate its shape and data type |
| Pixel access | Read and modify single pixels and rectangular regions |
| Channel operations | Split, merge, remove and isolate B, G, R channels |
| RGB conversion | Convert BGR to RGB and see why the order matters |
| HSV conversion | Split Hue, Saturation and Value channels |
| HSV adjustments | Increase brightness, decrease saturation and shift hue |
| LAB conversion | Split Lightness, A and B channels |

## Key Concepts

- OpenCV reads images in **BGR** order, not RGB.
- An image is a NumPy array with shape `(Height, Width, Channels)` and type `uint8` (0 to 255).
- In OpenCV, **Hue ranges from 0 to 179**, while Saturation and Value range from 0 to 255.
- `cv2.add()` and `cv2.subtract()` clip values at 255 and 0, while normal NumPy operations can overflow.
- A hue shift uses `% 180` so values wrap around the hue circle.

## Main Functions Used

| Function | Purpose |
|---|---|
| `cv2.imread()` | Load an image from a file |
| `cv2.split()` / `cv2.merge()` | Separate or combine color channels |
| `cv2.cvtColor()` | Convert between color spaces |
| `cv2.add()` / `cv2.subtract()` | Adjust channel values safely |
| `np.zeros_like()` | Create a blank channel with the same size |

## Project Structure

```
02-Color-Spaces-and-Channel-Manipulation/
    02_Color_Spaces_and_Channel_Manipulation.ipynb
    README.md
    kitchen.jpg
```

## How to Run

1. Click the **Open in Colab** badge at the top.
2. Run the cells in order.
3. When asked, upload `image.jpg` or any colored photo of your own.

## Requirements

- Python 3
- OpenCV (`opencv-python`)
- NumPy

The notebook is written for Google Colab. It uses `google.colab.patches.cv2_imshow` to display images.

## Tools

Python, OpenCV, NumPy, Google Colab

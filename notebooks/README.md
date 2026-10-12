# Image Basics and Transformations using OpenCV

A beginner-friendly Digital Image Processing practical that covers the core operations of loading, analysing and transforming an image using Python, OpenCV and NumPy.

## Objective

To understand how a digital image is stored as an array of pixels and to perform basic operations on it.

## Tasks Covered

| Step | Task | OpenCV / NumPy Function |
|------|------|--------------------------|
| 1 | Install and import libraries | `cv2`, `numpy` |
| 2 | Upload and read an image | `files.upload()`, `cv2.imread()` |
| 3 | Check image dimensions | `img.shape` |
| 4 | Display the image | `cv2_imshow()` |
| 5 | Convert to grayscale | `cv2.cvtColor()` |
| 6 | Save the processed image | `cv2.imwrite()` |
| 7 | Calculate average brightness | `np.mean()` |
| 8 | Binary thresholding | `cv2.threshold()` |
| 9 | Resize the image | `cv2.resize()` |
| 10 | Flip the image | `cv2.flip()` |
| 11 | Draw a rectangle | `cv2.rectangle()` |

## Key Concepts

- **BGR format:** OpenCV reads colors as Blue, Green, Red (not RGB).
- **Image shape:** `(Height, Width, Channels)`. A color image has 3 channels, a grayscale image has 1.
- **Grayscale:** Pixel values range from 0 (black) to 255 (white).
- **Thresholding:** Pixels above 128 become white (255), all others become black (0).
- **Resizing:** `shape` gives (height, width) but `cv2.resize()` needs (width, height).

## Results

| Operation | Result |
|-----------|--------|
| Original image size | 676 x 1200 pixels, 3 channels |
| Average brightness | 63.53 (a fairly dark image) |
| Resized image | Half of the original size |

## Tools Used

- Python
- OpenCV
- NumPy
- Google Colab

## How to Run

1. Open `01_Image_Basics_and_Transformations.ipynb` in Google Colab.
2. Run the cells one by one from top to bottom.
3. When asked, upload any image from your computer.
4. View the outputs below each cell.

## Files

```
├── 01_Image_Basics_and_Transformations.ipynb   # Main notebook
├── README.md                                   # Lab description
```

## What I Learned

- How images are stored as NumPy arrays
- How to convert a color image to grayscale
- How brightness can be measured using the mean pixel value
- How thresholding creates a black and white image
- How to resize, flip and annotate images using OpenCV

## Author

**Zimal**
GitHub: [ZimalYousuf3](https://github.com/ZimalYousuf3)

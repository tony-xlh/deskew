# deskew

A collection of document deskewing methods.

* [index.html](https://tony-xlh.github.io/deskew/). A web document scanning app based on [Dynamic Web TWAIN](https://www.dynamsoft.com/web-twain/overview) which provides document images deskewing.
* `run-magick.bat`. Deskew document images using ImageMagick.
* `run-magick.py`. Deskew document images using Python + OpenCV.


## Delve into Deskewing

Here are the steps using image processing to deskew document images based on text lines.

1. Normalize the image with the following operations:
    * Blur
    * Resize
    * Crop border
    * Grayscale
    * Invert
    * Threshold
2. Find countours based on the binary image.
3. Get the rotation angle of every contours and use the median as the skewed angle.
4. Run affine transformation to get the deskewed image.

You can find the corresponding code in the `py` file.

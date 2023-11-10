# Image-VideoSegmentationinNIRforPlantDetection
Thresholding Image/Video Segmentation for NIR+NDVI for Plant Detection - a simple but effective method that uses the NIR reflectance of plants with active thresholding of the red channel to focus only on the plants in an image or video
# Image + Video Segmentation in Near-Infrared Using HSV Color Spaces with OpenCV in Python

This repository shares a technique for performing a simple type of image segmentation used to separate objects visible in near-infrared and ultraviolet using the hue, saturation, and value (HSV) values in the color space with OpenCV in Python. This is a useful tool for processing NIR images and videos when you want to search for vegetation in an image using a defined threshold. Additionally, you can perform fast NDVI analysis on the examined region in video clips.

## What is Segmentation?

In this context, segmentation literally means cutting out an object that has a particularly well-defined color in the image.

## Understanding Color

It's important to remember that we don't see the red spectrum of light but rather see every other spectrum except that one. Our brain interprets this and labels it as a red object. This labeling depends on the level of light exposure, not the intrinsic color of the object.

## Color Spaces

In photography, images are captured using CCD sensors equipped with a filter that correlates properly with our visual perception. The demosaicking process is used to reconstruct a full-color image from incomplete color samples.

## HSV Color Space

The HSV (Hue, Saturation, Value) model defines a color space in terms of three main components: Hue, Saturation, and Value. It is widely used in computer graphics applications.

## Segmentation in HSV Color Space

Segmenting images in the HSV color space can be applied to near-infrared photography to capture the NIR reflectance of plants. By applying a threshold in the interpreted red channel, we can separate vegetation taken in the NIR from the background.

```python
# Threshold for vegetation in the red to orange range in the NIR
low_red = np.array([160, 105, 84])
high_red = np.array([179, 255, 255])

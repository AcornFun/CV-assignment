# CV-assignment ocr
# Optical Character Recognition (OCR) Report

## Introduction
This repository contains the implementation and results of Optical Character Recognition (OCR) using the Tesseract and EasyOCR libraries. The goal is to extract text from images and evaluate the performance of both OCR methods. The report includes preprocessing of example images at different levels and compares the final recognition results, focusing on the efficiency and accuracy of the EasyOCR library.

## Environment Setup

### Libraries Used:
- **Tesseract OCR**: An open-source OCR engine.
- **Pytesseract**: A Python wrapper for Tesseract.
- **EasyOCR**: A deep learning-based OCR library.
- **OpenCV**: A library for image processing.
- **Matplotlib**: For visualizing images.

The code implementation is built on Google Colab due to the lack of GPU power on the local machine.

## Load Picture and Preprocessing
1. **Initial Setup**: Upload the image to Google Colab and read it using Pytesseract for initial recognition.
  
2. **Preprocessing Steps**:
    - **First Preprocessing**:
        - Convert the image to grayscale.
        - Apply Gaussian blur to reduce noise.
        - Perform binarization to create a black-and-white image.
        - Use morphological erosion with a 5x5 rectangular structuring element to reduce the size of white regions (text).
  
    - **Second Preprocessing**:
        - Binarize the grayscale image and invert colors (text becomes white on black).
        - Use contour detection to identify potential text areas.
        - Filter and crop contours to obtain relevant regions in the binary image.

After preprocessing, recognition accuracy may decrease due to the order of operations or parameter settings.

## EasyOCR Implementation
EasyOCR was implemented without any preprocessing to compare results with Tesseract. Results showed that EasyOCR performed better for this specific example.

## Video 
- **Video**: [Watch here](https://youtu.be/hJnIVd38gjI)

## Conclusion
Both Tesseract and EasyOCR are effective for OCR tasks, with EasyOCR showing superior performance in this particular case.

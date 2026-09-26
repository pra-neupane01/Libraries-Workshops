# 01 - NumPy Image Basics

This module demonstrates foundational image manipulation and representation techniques in Python using only NumPy.

---

## Core Concepts Explained

### 1. What is an image?
Digitally, an image is a discrete grid (matrix) of numerical values. Each numerical entry dictates the intensity or color at a specific coordinate in space. Rather than being continuous visual media, digital images are structured numerical datasets that can be processed with matrix mathematics and linear algebra.

### 2. What is a pixel?
A **pixel** (short for *picture element*) is the smallest individual addressable unit in a digital image. In a standard 8-bit image, a pixel is stored as an unsigned integer (`uint8`) ranging from `0` to `255`, where `0` represents complete absence of light (black) and `255` represents maximum intensity (white).

### 3. What is an image shape?
In NumPy, an image's shape describes its dimensional dimensions in the order `(Height, Width, Channels)`:
- **Grayscale / Single-channel**: Represented as a 2D matrix with shape `(H, W)`.
- **Color (RGB)**: Represented as a 3D array with shape `(H, W, 3)`, where the third dimension corresponds to individual color layers.

### 4. What does RGB mean?
**RGB** stands for **Red, Green, Blue**. It is an additive color model where colors are created by superimposing light from these three primary channels:
- Pure Red: `[255, 0, 0]`
- Pure Green: `[0, 255, 0]`
- Pure Blue: `[0, 0, 255]`
- Pure White: `[255, 255, 255]`
- Pure Black: `[0, 0, 0]`

### 5. What is normalization?
Normalization is the process of rescaling pixel intensity values from their default integer range (`[0, 255]`) into a floating-point range between `0.0` and `1.0`.

$$\text{Pixel}_{\text{norm}} = \frac{\text{Pixel}}{255.0}$$

**Why normalize?**
- Prevents computational instability and exploding gradients in neural networks.
- Standardizes feature scales so uniform learning rates can be applied across different data pipelines.

---

## Running the Code

Install dependencies:
```bash
pip install -r requirements.txt
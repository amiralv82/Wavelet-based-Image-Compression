# Wavelet-based-Image-Compression
This project demonstrates **image compression** using **Discrete Wavelet Transform (DWT) with configurable hard thresholding. The method reduces the image file size while attempting to preserve its visual quality.

## Overview

**Wavelet compression** is a powerful technique that transforms an image into its frequency components. By thresholding and removing insignificant coefficients, we can reconstruct a near-identical version of the image with much smaller size.

This implementation uses:
- **`pywt`** (PyWavelets) for DWT
- **`OpenCV`** and **`matplotlib`** for image I/O and visualization
- **`NumPy`** for matrix operations

---

## Features

- Compresses grayscale images using 2D wavelet transform
- Adjustable compression threshold
- Visualizes the original vs. compressed images
- Calculates and prints **compression ratio** and **space savings**
- Supports batch testing on multiple thresholds

---

## Requirements

Install the required packages via pip:

```bash
pip install numpy matplotlib opencv-python PyWavelets


⸻

▶ How to Run
	1.	Place your grayscale image (e.g. lena30.jpg, 4K.jpg) in the same directory.
	2.	Run the Python script:

python wavelet_compression.py

	3.	You’ll see original and compressed images side by side, along with the compression statistics printed to the terminal.

⸻

 Example Output

[Threshold=1]  Original: 200.54 KB | Compressed: 190.12 KB | Ratio: 1.05
[Threshold=32] Original: 200.54 KB | Compressed: 83.45 KB  | Ratio: 2.40

And visual comparison:

Original	Threshold = 8	Threshold = 32
		


⸻

 How It Works
	1.	Wavelet Decomposition: The image is decomposed into approximation and detail coefficients using DWT.
	2.	Thresholding: Coefficients with absolute values below a set threshold are zeroed.
	3.	Reconstruction: The image is reconstructed from the modified coefficients.
	4.	Compression Ratio: File sizes before and after compression are compared.

⸻

 Parameters to Tune
	•	wavelet type: 'haar', 'db1', 'db2', etc.
	•	level: Decomposition level (default is 2)
	•	threshold: The cutoff for discarding coefficients

⸻


Author

Developed by Amir-Abbas Alvand – feel free to contribute or reach out for collaboration!

---

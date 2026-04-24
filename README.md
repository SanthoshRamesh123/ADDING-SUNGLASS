# Virtual-Sunglasses
This is a fun project that adds sunglasses to photos using image processing

## Overview

This project demonstrates how to overlay a sunglasses image onto a human face using OpenCV in Python. It focuses on basic image manipulation techniques such as resizing, region-of-interest (ROI) selection, and pixel replacement.

The implementation is intentionally simple and serves as a foundational exercise for understanding how image compositing works before moving on to more advanced techniques like alpha blending and facial landmark detection.

---

## Features

* Load and process images using OpenCV
* Resize overlay image to fit a target region
* Replace a specific region of an image (eye area)
* Basic image visualization using Matplotlib

---

## Project Structure

```
.
├── main_sunglass.ipynb
├── face image (input)
├── sunglasses image (PNG)
└── README.md
```

---

## Requirements

Make sure the following libraries are installed:

```bash
pip install opencv-python numpy matplotlib
```

---

## How It Works

1. The face image is loaded
2. The sunglasses image is resized to match the desired region
3. A region of interest (ROI) is selected on the face image
4. The resized sunglasses image is placed onto that region

---

## Example Code Snippet

```python
import cv2
import matplotlib.pyplot as plt

# Resize sunglasses
glassPNG = cv2.resize(glassPNG, (100,25))

# Copy original image
faceWithGlassesNaive = faceImage.copy()

# Define region
y1, x1 = 85,60
h, w = glassPNG.shape[:2]

# Overlay
faceWithGlassesNaive[y1:y1+h, x1:x1+w] = glassPNG

# Display
plt.imshow(faceWithGlassesNaive[..., ::-1])
plt.axis('off')
```

---

## Output
<img width="432" height="500" alt="Screenshot 2026-04-24 135302" src="https://github.com/user-attachments/assets/b5aa62a5-4652-4ea6-a350-2a875128dc64" />


<img width="1233" height="165" alt="Screenshot 2026-04-24 135313" src="https://github.com/user-attachments/assets/8cbfc327-addb-4014-af8c-ea2fb687646d" />


<img width="1265" height="731" alt="Screenshot 2026-04-24 135326" src="https://github.com/user-attachments/assets/406cb609-1cf1-4a53-a183-8a63385e6f3b" />


---

## Future Improvements

* Integrate face and eye detection using Haar cascades or Dlib
* Add alpha blending for realistic overlays
* Dynamically scale and position glasses based on facial landmarks
* Support multiple face inputs

---

## License

This project is open-source and available for educational purposes.

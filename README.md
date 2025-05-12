# Number-Plate-Detection-Of-Vehicles
Here is the updated **README.md** without the example and license sections:

---

# 🚗 Indian Vehicle Number Plate Detector

This project implements a **Number Plate Detection and Recognition System** specifically designed for **Indian vehicle license plates**. Using a combination of image processing techniques and OCR (Optical Character Recognition), the system detects license plates from images and extracts the alphanumeric characters using a deep learning-based OCR engine.

A user-friendly **Gradio web interface** allows for easy interaction and testing. This project is ideal for traffic monitoring, automated toll systems, parking lot management, and smart surveillance systems.

---

## 🔍 Project Overview

The primary goal of this project is to build an end-to-end pipeline for detecting vehicle number plates and extracting readable text using minimal training and maximum generalization, specifically for Indian license plates.

---

## 📦 Features

* ✅ Automatic detection of number plates from vehicle images
* ✅ Text recognition using `EasyOCR` (no training needed)
* ✅ Edge-based contour detection for accurate localization
* ✅ Clean Gradio interface for easy testing
* ✅ Works on JPG and PNG image formats
* ✅ Google Colab-compatible and cloud-friendly

---

## 🧠 Technologies Used

* **Python 3.9+**
* **OpenCV** – Image preprocessing and contour detection
* **EasyOCR** – Deep learning-based OCR for multilingual text
* **Gradio** – Web UI for uploading and testing images
* **Matplotlib** – For optional visualization
* **NumPy** – Numerical operations
* **scikit-learn** – For optional train-test split
* **Google Colab** – Development and testing environment
* **Google Drive** – Dataset hosting

---

## 🛠️ How It Works

1. **Image Preprocessing**
   Images are converted to grayscale and filtered to reduce noise.

2. **Edge Detection**
   Canny edge detection highlights edges that are likely part of a number plate.

3. **Contour Detection**
   Largest rectangular-like contours are searched for the plate region.

4. **Cropping Plate Region**
   Once found, the plate area is cropped from the original image.

5. **OCR Processing**
   The cropped plate is passed through `EasyOCR` to extract readable characters.

6. **Gradio Interface**
   Users upload an image and get predicted number plate text instantly.

---

## 📂 Project Structure

```
Indian_Number_Plate_Detector/
│
├── Indian_Number_Plates/        # Folder containing input images
├── number_plate_detector.ipynb  # Main Colab Notebook (or .py version)
├── README.md                    # This file
├── requirements.txt             # Python dependencies
└── sample_outputs/              # Example images and outputs (optional)
```

---

## 🚀 Getting Started

### ▶️ Run on Google Colab

1. Upload your `Indian_Number_Plates` folder to your Google Drive.
2. Open the provided `number_plate_detector.ipynb` notebook in Google Colab.
3. Mount Google Drive when prompted.
4. Verify the `DATASET_PATH` is correctly pointing to your dataset.
5. Run all cells and use the Gradio UI to test with vehicle images.

### 🏠 Run Locally (Optional)

Install the necessary Python packages:

```bash
pip install opencv-python easyocr gradio numpy scikit-learn matplotlib
```

Then run your `.py` script or notebook locally.

---

## ⚠️ Limitations

* Not suitable for real-time detection (image only, not video).
* Performance may drop with rotated, obscured, or dirty plates.
* Plate localization relies on contours and may fail in cluttered backgrounds.
* Currently supports English characters only (regional plates may need language configuration).

---

## 💡 Future Enhancements

* Support for live video streams or real-time camera feed
* Integration with YOLOv5 or SSD for robust plate localization
* Handling tilted/skewed plates with perspective correction
* Adding multilingual OCR for regional languages
* Integration with RTO databases for vehicle verification

---

## ❤️ Acknowledgements

* [EasyOCR](https://github.com/JaidedAI/EasyOCR)
* [Gradio](https://www.gradio.app/)
* [OpenCV](https://opencv.org/)
* Indian traffic surveillance datasets (where applicable)


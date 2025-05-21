# 🖼️ Image Localization Preprocessing with OpenCV

> 🧠 This project showcases my skills in image preprocessing, bounding box localization, and dataset preparation for computer vision tasks.

This repository implements a preprocessing pipeline for image localization tasks using Python and OpenCV. It loads class-wise image data and corresponding bounding box annotations from CSV files, normalizes the coordinates, and converts all inputs to NumPy arrays for use in deep learning models.

## 📂 Dataset Structure

The dataset is included in the repository under the `dataset/` folder:

- `dataset/images/`: Contains subfolders for each class (e.g., `airplane`, `car`, etc.)
- `dataset/annotations/`: Contains CSV files with bounding box annotations for each class

Each CSV file has the format:

```
image_name,x_min,y_min,x_max,y_max
img1.jpg,49,30,349,137
img2.jpg,...
```

## 🔍 What the Code Does

- Loads class names from the image directory.
- Loads corresponding annotation CSVs.
- For each image:
  - Reads the image and finds its bounding box.
  - Normalizes bounding box coordinates by width and height.
  - Converts the image from BGR to RGB.
  - Resizes it to 224×224 pixels.
- Saves the processed data into NumPy arrays:
  - `images` — RGB resized images
  - `labels` — numeric class labels
  - `annotations` — normalized bounding boxes

## 🛠️ Technologies Used

- Python 3
- OpenCV
- NumPy
- Pandas
- Matplotlib (optional)

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/reyhaneghaderi/image-localization.git
   cd image-localization
   ```

2. Install the dependencies:
   ```bash
   pip install opencv-python numpy pandas matplotlib
   ```


   `
   ```

## 📌 Notes

- This repository focuses on preprocessing for localization. No model training is included.
- Normalized coordinates make it easy to use this data with popular detection models like YOLO or SSD.



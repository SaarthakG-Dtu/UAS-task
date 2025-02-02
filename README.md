# UAS TASK
Image detection model for counting number of fruits using YOLO,Open-cv and numpy.
This project uses a YOLO (You Only Look Once) model to detect fruits in front and back view images. It aligns both views using homography and counts unique fruits based on their position and color.

Features:
1.Detects fruits using a YOLO model.
<br>
2.Identifies the dominant color of each fruit using refined HSV color ranges.
<br>
3.Aligns front and back view images using feature matching and homography.
<br>
4.Counts unique fruits across both views.
<br>
5.Displays detected fruits and their respective colors.

Requirements:
Ensure you have the following installed:
<br>
Python 3.x
<br>
OpenCV
<br>
NumPy
<br>
Ultralytics YOLOv8

Fruit Detection and Counting with YOLO

This project uses a YOLO (You Only Look Once) model to detect fruits in front and back view images. It aligns both views using homography and counts unique fruits based on their position and color.

Features

Detects fruits using a YOLO model.

Identifies the dominant color of each fruit using refined HSV color ranges.

Aligns front and back view images using feature matching and homography.

Counts unique fruits across both views.

Displays detected fruits and their respective colors.

Requirements

Ensure you have the following installed:

Python 3.x

OpenCV

NumPy

Ultralytics YOLOv8

Install dependencies using:

pip install opencv-python numpy ultralytics

Usage

1. Model Setup

Download or train a YOLO model and place it in the project directory.

2. Run the Script

Modify the file paths in count_unique_fruits() and run:

python fruit_detection.py

3. Output

The script prints detected unique fruits along with their colors:

Unique Fruits and Their Colors:
Center: (150, 200), Color: Red
Center: (300, 400), Color: Green
...
Total unique fruits detected: 5

File Structure

📂 UAS_DTU_Fruit_Detection
 ├── fruit_detection.py  # Main detection script
 ├── best.pt             # Trained YOLO model
 ├── sample_images/      # Folder for input images
 ├── README.md           # Project documentation

Customization

Adjust HSV color ranges in detect_color() for better accuracy.

Modify the distance threshold in count_unique_fruits() to fine-tune fruit matching.

Acknowledgments

Ultralytics YOLO for the object detection framework.

OpenCV for image processing.

License

This project is open-source and available under the MIT License.




<br>
Author-Saarthak Gupta


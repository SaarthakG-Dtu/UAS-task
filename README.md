# UAS TASK
Image detection model for counting number of fruits using YOLO,Open-cv and numpy.
This project uses a YOLO (You Only Look Once) model to detect fruits in front and back view images. It aligns both views using homography and counts unique fruits based on their position and color.

Features:
<br>
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

Install dependencies using:
<br>
pip install opencv-python numpy ultralytics

Usage
<br>
1. Model Setup
<br>
Download or train a YOLO model and place it in the project directory.
<br>
<br>
2. Run the Script
<br>
Modify the file paths in count_unique_fruits() and run:
<br>
python fruit_detection.py
<br>
<br>
3. Output
<br>
The script prints detected unique fruits along with their colors:
<br>
Unique Fruits and Their Colors:
<br>
Center: (150, 200), Color: Red
<br>
Center: (300, 400), Color: Green
<br>
...
<br>
Total unique fruits detected: 5
<br>
<br>
File Structure
<br>
📂 UAS_DTU_Fruit_Detection
<br>
 ├── fruit_detection.py  # Main detection script
 <br>
 ├── best.pt             # Trained YOLO model
 <br>
 ├── sample_images/      # Folder for input images
 <br>
 ├── README.md           # Project documentation
 <br>

Customization :
<br>
Adjust HSV color ranges in detect_color() for better accuracy.
<br>
Modify the distance threshold in count_unique_fruits() to fine-tune fruit matching.
<br>

Acknowledgments
<br>
Ultralytics YOLO for the object detection framework.
<br>
OpenCV for image processing.

License
<br>
This project is open-source and available under the MIT License.




<br>
Author-Saarthak Gupta


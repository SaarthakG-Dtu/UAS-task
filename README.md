# UAS TASK # Fruit Detection and Counting System  
<br>
Accurate fruit counting across multiple views using YOLO detection and homography alignment. Image detection model for counting number of fruits using YOLO,Open-cv and numpy.
This project uses a YOLO (You Only Look Once) model to detect fruits in front and back view images. It aligns both views using homography and counts unique fruits based on their position and color.

## Features  

1. **Dual-View Fruit Detection**  
   - Detects fruits in both front and back view images using YOLOv8  
   - Maintains view context for each detected fruit  

2. **Advanced Color Identification**  
   - Uses HSV color masking with morphological cleanup  
   - Specialized purple detection range (H:125-159, S:50-255)  
   - Handles multi-range colors (e.g., Red has two HSV ranges)  

3. **Precise View Alignment**  
   - ORB feature matching with RANSAC homography  
   - 30-pixel distance threshold for fruit matching  

4. **Unique Fruit Counting**  
   - Matches fruits across views using color + spatial proximity  
   - Prints detailed report of unique fruits  

## Installation  
```bash
pip install opencv-python numpy ultralytics
```

## Usage  
1. **Configure Paths**  
   Modify these paths in the `__main__` block:  
   ```python
   front_path = r'C:\Users\saart\...\8\front.jpg'
   back_path = r'C:\Users\saart\...\8\back.jpg'
   model_path = r'C:\Users\saart\...\best.pt'
   ```

2. **Run Detection**  
   ```bash
   python fruit_detection.py
   ```

3. **Sample Output**  
   ```
   Unique Fruits and Their Colors:
   View: Both, Color: Purple
   View: Back, Color: Yellow
   View: Front, Color: Green

   Total unique fruits detected: 3
   ```

## Customization  

| Component            | Location                     | Key Parameters                 |
|----------------------|------------------------------|--------------------------------|
| Color Detection      | `detect_color()`             | `color_masks` dictionary       |
| Alignment Accuracy   | `align_views()`              | `nfeatures=2000`, RANSAC threshold |
| Matching Precision   | `count_unique_fruits()`      | `dist < 30` (line 100)         |

## File Structure  
```
📦UAS_DTU_Fruit_Detection
├── 📂UAS_DTU_Round_2_Task_data  # Parent folder
│   └── 📂8                      # Example image pair
│       ├── front.jpg           # Front view image
│       └── back.jpg            # Back view image
├── **fruit_detection.ipynb**        # Main detection script
├── best.pt                     # YOLOv8 model weights
└── README.md                   # This documentation
```

## Key Technical Specs  
- **YOLO Model**: Requires Ultralytics YOLOv8 format (`best.pt`)  
- **Color Space**: HSV with morphological cleaning (opening + closing)  
- **Alignment**: ORB features + RANSAC homography (50 best matches)  
- **Matching Logic**: Color consistency + 30-pixel distance threshold  

---

**Author**: Saarthak Gupta  
**License**: MIT License

<br>
Author-Saarthak Gupta


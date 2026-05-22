# OpenCV Tutorial

A comprehensive set of tutorials demonstrating various computer vision techniques using OpenCV, based on the Tech-with-Time OpenCV tutorial series.

## Overview

This project contains a series of tutorials that progressively introduce key OpenCV concepts and functionality. Each tutorial is self-contained and demonstrates specific computer vision techniques using real-time video from a webcam.

## Prerequisites

- Python 3.x
- OpenCV (cv2)
- NumPy

## Installation

1. Install the required dependencies:
```bash
pip install opencv-python numpy
```

2. Ensure you have a webcam connected (required for most tutorials)

3. The tutorials use image assets stored in the `assets/` directory (dog.jpg, ball.PNG, soccer_practice.jpg, shoe.PNG)

## Tutorials

### Tutorial 1: Image Manipulation Basics
**File:** `tutorial1.py`

Demonstrates basic image manipulation techniques including:
- Loading images from disk using `cv2.imread()`
- Resizing images with `cv2.resize()`
- Pixel-level manipulation - randomly modifying pixel colors in a region
- Displaying images in a window with `cv2.imshow()`
- Window management with `cv2.namedWindow()` and `cv2.moveWindow()`

**Key Concepts:**
- Image I/O operations
- Array indexing for pixel access
- Image display and window management

**Usage:**
```bash
python tutorial1.py
```

### Tutorial 3: Video Manipulation with Transformations
**File:** `tutorial3.py`

Demonstrates real-time video manipulation with geometric transformations:
- Capturing video from webcam using `cv2.VideoCapture()`
- Resizing and flipping frames
- Arranging multiple transformed views of the same frame in a grid layout
- Applying transformations: resize, flip, and rotate

**Key Concepts:**
- Real-time video capture and processing
- Frame transformations (scale, flip, rotate)
- Image composition - combining multiple frames
- Event handling with `cv2.waitKey()`

**Usage:**
```bash
python tutorial3.py
# Press 'q' to quit
```

### Tutorial 4: Drawing Shapes and Text on Frames
**File:** `tutorial4.py`

Demonstrates drawing various shapes and text annotations on video frames:
- Drawing lines with `cv2.line()`
- Drawing rectangles with `cv2.rectangle()`
- Drawing circles with `cv2.circle()`
- Adding text with `cv2.putText()`
- Working with different font types

**Key Concepts:**
- Shape drawing primitives
- Text rendering
- Color representation in BGR format
- Real-time frame annotation

**Usage:**
```bash
python tutorial4.py
# Press 'q' to quit
```

### Tutorial 5: Color Space Conversion and Masking
**File:** `tutorial5.py`

Demonstrates color-based image filtering and segmentation:
- Color space conversion from BGR to HSV using `cv2.cvtColor()`
- Creating masks with `cv2.inRange()` to isolate specific color ranges
- Applying masks using bitwise operations with `cv2.bitwise_and()`
- Real-time color filtering on video stream

**Key Concepts:**
- Color space conversion (BGR to HSV)
- Color range definition
- Image masking and bitwise operations
- Real-time color-based filtering

**Usage:**
```bash
python tutorial5.py
# Press 'q' to quit
# (Filters for blue colored objects)
```

### Tutorial 6: Corner Detection and Feature Tracking
**File:** `tutorial6.py`

Demonstrates feature detection and tracking:
- Detecting corners using `cv2.goodFeaturesToTrack()`
- Converting floating-point coordinates to integers
- Drawing circles at corner locations
- Connecting corners with lines to visualize corner patterns
- Real-time feature tracking on video

**Key Concepts:**
- Corner/feature detection algorithms
- Feature extraction and representation
- Real-time feature tracking
- Coordinate transformation

**Usage:**
```bash
python tutorial6.py
# Press 'q' to quit
```

### Tutorial 7: Template Matching
**File:** `tutorial7.py`

Demonstrates object detection using template matching:
- Loading template images with `cv2.imread()`
- Matching templates in source images using `cv2.matchTemplate()`
- Comparing different matching methods (6 methods demonstrated):
  - TM_CCOEFF: Correlation coefficient
  - TM_CCOEFF_NORMED: Normalized correlation coefficient
  - TM_CCORR: Cross correlation
  - TM_CCORR_NORMED: Normalized cross correlation
  - TM_SQDIFF: Sum of squared differences
  - TM_SQDIFF_NORMED: Normalized sum of squared differences
- Finding best match location using `cv2.minMaxLoc()`
- Drawing rectangles around detected matches

**Key Concepts:**
- Template matching algorithms
- Method selection based on use case
- Result interpretation (min vs max values)
- Object localization

**Usage:**
```bash
python tutorial7.py
# Detects soccer balls in practice field images
# Press any key to continue to next matching method
```

### Tutorial 8: Face Detection with Cascade Classifiers
**File:** `tutorial8.py`

Demonstrates real-time face detection and feature detection:
- Loading pre-trained cascade classifiers (face, eye, smile detection)
- Multi-scale face detection using `cv2.CascadeClassifier.detectMultiScale()`
- Detecting features within detected face regions (Region of Interest - ROI)
- Drawing detection results on video frames
- Detecting eyes within face regions
- Detecting smile/mouth regions

**Key Concepts:**
- Cascade classifier-based detection
- Multi-scale object detection
- Region of Interest (ROI) processing
- Hierarchical feature detection
- Real-time face and eye detection

**Usage:**
```bash
python tutorial8.py
# Press 'q' to quit
# Detects and marks faces, eyes, and mouth regions
```

## Common Dependencies and Operations

### VideoCapture Operations
- `cv2.VideoCapture(0)`: Open webcam (0 = default camera)
- `cap.read()`: Read frame from video source
- `cap.get(propId)`: Get video property (3=width, 4=height)
- `cap.release()`: Release the video capture object

### Image Conversion and Processing
- `cv2.imread()`: Read image from file
- `cv2.cvtColor()`: Convert between color spaces
- `cv2.resize()`: Resize images
- `cv2.flip()`: Flip image horizontally or vertically
- `cv2.rotate()`: Rotate image

### Drawing Functions
- `cv2.line()`: Draw line
- `cv2.rectangle()`: Draw rectangle
- `cv2.circle()`: Draw circle
- `cv2.putText()`: Add text

### Event Handling
- `cv2.imshow()`: Display image in window
- `cv2.waitKey()`: Wait for keyboard input (in milliseconds)
- `cv2.destroyAllWindows()`: Close all windows

## Tips and Best Practices

1. **Press 'q' to quit**: Most tutorials use this key binding to exit
2. **Webcam requirements**: Ensure proper lighting for face detection tutorials
3. **Performance**: Image operations are real-time but dependent on webcam FPS
4. **BGR Color Format**: OpenCV uses BGR (not RGB) as default color order
5. **Grayscale conversion**: Some algorithms work on grayscale images - use `cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)`

## Learning Path

1. Start with **Tutorial 1** to understand image basics
2. Progress to **Tutorial 3-4** for real-time video manipulation
3. Learn color processing with **Tutorial 5**
4. Explore feature detection in **Tutorial 6**
5. Master template matching in **Tutorial 7**
6. Advance to cascade-based detection in **Tutorial 8**

## References

- [OpenCV Official Documentation](https://docs.opencv.org/)
- [OpenCV Python Tutorials](https://docs.opencv.org/master/d6/d00/tutorial_py_root.html)
- Tech-with-Time OpenCV Tutorial Series

## License

This project is based on the Tech-with-Time OpenCV tutorial and is provided for educational purposes.

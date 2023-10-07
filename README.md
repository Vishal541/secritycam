# Motion Detection Using OpenCV

This Python script uses OpenCV to detect motion from a camera feed. When motion is detected, it triggers an alert sound.

## Prerequisites

- Python
- OpenCV library (`cv2`)
- `winsound` library (for playing alert sound)
- Webcam or camera connected to your computer

## How it Works

1. The script captures video frames from the specified camera (in this case, camera index 1).

2. It compares two consecutive frames to detect any differences, which indicate motion.

3. The differences are converted to grayscale for further processing.

4. Gaussian blur is applied to reduce noise in the grayscale image.

5. Thresholding is used to create a binary image, highlighting the areas with significant changes.

6. Dilation is performed to make the detected motion regions more prominent.

7. Contours are found in the binary image to identify the regions of motion.

8. For each detected contour, a bounding rectangle is drawn around it in the original frame.

9. An alert sound ('alert.wav') is played asynchronously using `winsound` whenever motion is detected.

10. The processed frame with bounding rectangles is displayed in a window called 'Granny Cam.'

11. The script continues to run until you press the 'q' key, at which point it stops.

## Usage

1. Ensure you have Python installed on your system.

2. Install the necessary libraries by running the following commands:

   ```bash
   pip install opencv-python-headless
   pip install opencv-python

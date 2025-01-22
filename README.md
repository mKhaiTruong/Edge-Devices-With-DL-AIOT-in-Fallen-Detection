# Edge-Devices-With-DL-AIOT-in-Fallen-Detection

Test 2 approaches to fallen detection: YOLOv11 for object detection and Mediapipe's Pose Estimation

For Object Detection,
YOLO models require two types of datasets: a set of images and set of numeric data. These numeric data consists of a label, and the cordinates of detected objects. Based on these two data, YOLO model can learn and process.

For Pose Estimation,
I tested 2 approaches: Calculating the Angle between joints or Calculating the width and height of detected person. 
+ If angle > threshold then a person is falling
+ If w > h * threshold then a person is falling
+ ![image](https://github.com/user-attachments/assets/762471b2-d812-4971-9d63-dc07c938bb69)

I decided to work with Pose Estimation's second approach: measure width and height. But sometimes there are weird ways to fall so adding an Optical Flow Approach to decide if a person action changed dramatically.

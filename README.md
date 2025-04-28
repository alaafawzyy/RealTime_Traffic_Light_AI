Real-Time AI Traffic Light Detection
This project is an Android application that performs real-time object detection using a YOLOv8 model converted to TensorFlow Lite format. The primary focus is detecting traffic lights and their states.

Features
Real-time object detection using YOLOv8 model

Camera preview with bounding box overlay

Performance metrics display (inference time)

Customizable detection thresholds

Non-Maximum Suppression (NMS) for filtering overlapping boxes

Project Structure
Main Components
MainActivity

Entry point of the application

Simple UI with a button to launch the real-time detection

RealTimeActivity

Handles camera setup and permissions

Processes frames for object detection

Displays results with overlay

Detector Class

Core detection logic using TensorFlow Lite

Handles model loading and inference

Processes detection results and applies NMS

OverlayView

Custom view for drawing bounding boxes and labels

Handles visualization of detection results

Key Packages
com.example.realtimeaitrafficlight: Contains the main activities

com.surendramaran.yolov8tflite: Contains the detection core classes

Setup Instructions
Clone the repository

Open the project in Android Studio

Add your YOLOv8 TFLite model to assets folder

Add corresponding labels file

Build and run the application

Dependencies
AndroidX libraries

CameraX for camera operations

TensorFlow Lite for model inference

Configuration
Constants can be modified in the Detector companion object:

kotlin
companion object {
    private const val INPUT_MEAN = 0f
    private const val INPUT_STANDARD_DEVIATION = 255f
    private val INPUT_IMAGE_TYPE = DataType.FLOAT32
    private val OUTPUT_IMAGE_TYPE = DataType.FLOAT32
    private const val CONFIDENCE_THRESHOLD = 0.3F
    private const val IOU_THRESHOLD = 0.5F
}
Usage
Launch the application

Grant camera permissions if requested

Tap the "Start Detection" button

Point the camera at traffic lights to see detection results

License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
YOLOv8 model by Ultralytics

TensorFlow Lite for mobile inference

Android CameraX team

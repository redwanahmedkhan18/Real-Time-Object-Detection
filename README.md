# Real-Time Object Detection using YOLOv6, OpenCV, and Python

This project implements real-time object detection using the YOLOv6 model in Python, leveraging OpenCV for video processing. The system can detect multiple objects from live webcam feeds or video files, providing high accuracy and efficiency.

## Features

- **Real-Time Detection:** Detect objects from a webcam feed or video file in real-time.
- **Multiple Object Detection:** Identifies multiple objects simultaneously with their respective confidence scores.
- **Optimized with YOLOv6:** Utilizes YOLOv6's pre-trained weights for high-speed and accurate detection.
- **Customizable Parameters:** Allows you to tweak confidence thresholds, image size, and more.

## Requirements

### Hardware
- A computer with a working webcam (if using webcam mode).
- A GPU is recommended for faster processing, but CPU mode is supported.

### Software

Ensure you have the following installed:

- Python 3.7+
- OpenCV
- PyTorch
- NumPy

You can install the required packages using the command below:

```bash
pip install -r requirements.txt
```
### Download Pre-trained Weights
Download the YOLOv6 pre-trained weights from the [YOLOv6 GitHub repository](https://github.com/meituan/YOLOv6/releases) and place it in the root directory of this project. For example:

```bash
wget https://github.com/meituan/YOLOv6/releases/download/0.1/yolov6s.pt
```
### Usage

#### Running Detection from Webcam
To start real-time object detection from a webcam, use the following command:

```bash
python detect.py --weights yolov6s.pt --source 0
```
Where `--source 0` indicates the webcam feed. If you have multiple cameras, you can change the index (e.g., `--source 1`).

#### Running Detection from a Video File
To run detection on a video file, use the following command:

```bash
python detect.py --weights yolov6s.pt --source path_to_video.mp4
```
### Results
When the model runs, it will open a video feed showing real-time object detection with bounding boxes, labels, and confidence scores.

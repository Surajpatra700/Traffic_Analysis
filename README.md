# Real-Time Traffic Analysis with YOLOv8

![Working Video][(link-to-the-video)](https://drive.google.com/file/d/1s0nyyijHFbfrtuI2fHo9CvxHWwAUX5nm/view?usp=sharing)

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [script_arguments](#script_arguments)
- [Run](#Run)
- [Results](#results)
- [License](#license)

## Introduction

This repository contains a real-time traffic analysis system leveraging YOLOv8 for object detection and unique vehicle tracking. The system is capable of analyzing live video feeds, assigning unique IDs to detected vehicles, plotting their trajectories, and counting vehicles entering specific zones or lanes.

## Features

- **Real-time Object Detection**: Utilizes YOLOv8 for efficient and accurate detection of vehicles in live video feeds.
- **Unique Vehicle Tracking**: Employs ByteTrack for tracking each vehicle uniquely across frames.
- **Trajectory Plotting**: Plots the trajectories of vehicles to visualize their paths.
- **Zone-based Counting**: Counts the number of vehicles entering specific zones or lanes.
- **Supervision**: Integrates with Supervison for enhanced monitoring and visualization.

## 💻 Installation

- clone repository and navigate to current directory

  ```bash
  git clone [https://github.com/roboflow/supervision.git](https://github.com/Surajpatra700/Traffic_Analysis.git)
  cd Traffic Analysis
  ```

- setup python environment and activate it [optional]

  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

- install required dependencies

  ```bash
  pip install -r requirements.txt
  ```

- download `traffic_analysis.pt` and `traffic_analysis.mov` files

  ```bash
  ./setup.sh
  ```
    ```

## 🛠️ script_arguments

- ultralytics

  - `--source_weights_path`: Required. Specifies the path to the YOLO model's weights
    file, which is essential for the object detection process. This file contains the
    data that the model uses to identify objects in the video.

  - `--source_video_path`: Required. The path to the source video file that will be
    analyzed. This is the input video on which traffic flow analysis will be performed.
  - `--target_video_path` (optional): The path to save the output video with
    annotations. If not specified, the processed video will be displayed in real-time
    without being saved.
  - `--confidence_threshold` (optional): Sets the confidence threshold for the YOLO
    model to filter detections. Default is `0.3`. This determines how confident the
    model should be to recognize an object in the video.
  - `--iou_threshold` (optional): Specifies the IOU (Intersection Over Union) threshold
    for the model. Default is 0.7. This value is used to manage object detection
    accuracy, particularly in distinguishing between different objects.

- inference

  - `--roboflow_api_key` (optional): The API key for Roboflow services. If not provided
    directly, the script tries to fetch it from the `ROBOFLOW_API_KEY` environment
    variable. Follow [this guide](https://docs.roboflow.com/api-reference/authentication#retrieve-an-api-key)
    to acquire your `API KEY`.
  - `--model_id` (optional): Designates the Roboflow model ID to be used. The default
    value is `"vehicle-count-in-drone-video/6"`.

  - `--source_video_path`: Required. The path to the source video file that will be
    analyzed. This is the input video on which traffic flow analysis will be performed.
  - `--target_video_path` (optional): The path to save the output video with
    annotations. If not specified, the processed video will be displayed in real-time
    without being saved.
  - `--confidence_threshold` (optional): Sets the confidence threshold for the YOLO
    model to filter detections. Default is `0.3`. This determines how confident the
    model should be to recognize an object in the video.
  - `--iou_threshold` (optional): Specifies the IOU (Intersection Over Union) threshold
    for the model. Default is 0.7. This value is used to manage object detection
    accuracy, particularly in distinguishing between different objects.## ⚙️ run

## ⚙️ Run

- ultralytics

  ```bash
  python ultralytics_example.py \
  --source_weights_path data/traffic_analysis.pt \
  --source_video_path data/traffic_analysis.mov \
  --confidence_threshold 0.3 \
  --iou_threshold 0.5 \
  --target_video_path data/traffic_analysis_result.mov
  ```

- inference

  ```bash
  python inference_example.py \
  --roboflow_api_key <ROBOFLOW API KEY> \
  --source_video_path data/traffic_analysis.mov \
  --confidence_threshold 0.3 \
  --iou_threshold 0.5 \
  --target_video_path data/traffic_analysis_result.mov
  ```


## Results

The following is a demonstration of the system in action:

![Working Video][(link-to-the-video)](https://drive.google.com/file/d/1s0nyyijHFbfrtuI2fHo9CvxHWwAUX5nm/view?usp=sharing)

**Key Results**:
- Real-time detection and aerial view tracking of vehicles.
- Visualization of vehicle trajectories.
- Accurate counting of vehicles entering specific zones.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

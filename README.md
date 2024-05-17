# Real-Time Traffic Analysis with YOLOv8

![Demo Video](link-to-your-video)

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This repository contains a real-time traffic analysis system leveraging YOLOv8 for object detection and unique vehicle tracking. The system is capable of analyzing live video feeds, assigning unique IDs to detected vehicles, plotting their trajectories, and counting vehicles entering specific zones or lanes.

## Features

- **Real-time Object Detection**: Utilizes YOLOv8 for efficient and accurate detection of vehicles in live video feeds.
- **Unique Vehicle Tracking**: Employs ByteTrack for tracking each vehicle uniquely across frames.
- **Trajectory Plotting**: Plots the trajectories of vehicles to visualize their paths.
- **Zone-based Counting**: Counts the number of vehicles entering specific zones or lanes.
- **Supervision**: Integrates with Supervison for enhanced monitoring and visualization.

## Installation

To set up the project, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/traffic-analysis-yolov8.git
    cd traffic-analysis-yolov8
    ```

2. **Create a virtual environment and activate it**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install the required dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Prepare your video feed**: Ensure you have a live video feed or a video file ready for analysis.

2. **Run the traffic analysis script**:
    ```bash
    python traffic_analysis.py --video path/to/your/video --config path/to/config/file
    ```

3. **View the results**: The system will process the video feed, display the live detection and tracking results, and output the vehicle counts and trajectories.

## Results

The following is a demonstration of the system in action:

![Demo Video](link-to-your-video)

**Key Results**:
- Real-time detection and tracking of vehicles.
- Visualization of vehicle trajectories.
- Accurate counting of vehicles entering specific zones.

## Contributing

Contributions are welcome! If you have suggestions for improvements or want to contribute new features, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

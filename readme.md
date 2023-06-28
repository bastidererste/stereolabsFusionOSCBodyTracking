# Body Tracking with multiple Stereolabs ZED Cameras and OSC output

This program allows you to track multiple bodies across multiple Stereolabs ZED cameras and send the tracked bodies and keypoints in the COCO18 Skeleton format to an OSC (Open Sound Control) receiver. The program utilizes computer vision techniques and the ZED SDK to detect and track bodies, and then sends the tracking data over OSC for further processing or visualization.

## Features

- **Multi-camera Body Tracking:** The program can handle multiple Stereolabs ZED cameras simultaneously. Each camera captures the video feed and performs body tracking independently.

- **COCO18 Skeleton Keypoints:** The program tracks the bodies using the COCO18 Skeleton model, which consists of 18 keypoint locations on the human body (e.g., nose, eyes, shoulders, elbows, wrists, etc.). It provides detailed information about the body pose.

- **OSC Communication:** The program sends the tracked bodies and keypoints data to an OSC receiver. OSC is a widely used protocol for communication between multimedia applications. It allows you to transmit various types of data, including positional and movement information.

## Installation

1. Clone the repository or download the program files to your local machine.

```
$ git clone https://github.com/your-username/body-tracking-program.git
```


2. Install the dependencies required for the program to run:

- Stereolabs ZED SDK: Follow the installation instructions provided by Stereolabs to install the ZED SDK for your operating system.

- OSC library: Install an OSC library compatible with your programming language of choice. Some popular options include pyOSC (Python), oscP5 (Processing), oscpack (C++), or liblo (C/C++).

3. Connect and configure your Stereolabs ZED cameras.

- Connect the ZED cameras to your computer via USB.
- Ensure that the cameras are recognized by the system and their drivers are installed correctly.
- Adjust camera settings such as resolution, frame rate, and exposure according to your requirements.

## Usage

1. Launch the OSC receiver on the destination machine or software that will receive the tracking data.

2. Modify the program configuration file (`config.json`) to set the OSC server IP address, port, and any other relevant parameters.

3. Run the program:

```
$ python body_tracking.py calibrationfile.json
```


4. The program will initialize the ZED cameras and start capturing video feeds.

5. It will perform body detection and tracking on each camera stream, identifying the bodies and their corresponding COCO18 Skeleton keypoints.

6. The program will send the tracked bodies and keypoints data to the specified OSC receiver according to the configured settings.

7. The OSC receiver can then process or visualize the received data for further use.

8. To stop the program, press `Ctrl + C` in the terminal or command prompt.

## Configuration

The program utilizes a configuration file (`config.json`) to specify various settings. You can modify this file to adjust the program behavior according to your requirements. Some configurable parameters include:

- `osc_server_ip`: The IP address of the OSC receiver.
- `osc_server_port`: The port number on which the OSC receiver is listening.
- `camera_parameters`: Camera-specific settings such as resolution, frame rate, and exposure.

## Contributing

Contributions to this project are welcome. If you find any issues or would like to suggest enhancements, please submit an issue or a pull request.

## License

This program is licensed under the [MIT License](LICENSE).

## Acknowledgements

This program utilizes the Stereolabs ZED SDK for camera integration and body tracking. We would

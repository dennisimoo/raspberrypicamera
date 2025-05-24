# Raspberry Pi Camera Stream

This project uses Flask to stream video from a Raspberry Pi camera to a web browser. It utilizes the `picamera2` library for camera interaction and OpenCV for frame encoding. This repository also includes a pre-existing working script (`working.py`) to make it easy to set up and run.

## Features
- Live streaming of the Raspberry Pi camera feed.
- MJPEG stream served via Flask.
- Supports Raspberry Pi Camera V2 (and other compatible camera modules).

## Requirements

Before running the application, ensure that your Raspberry Pi is properly set up with the following:

- **Raspberry Pi 4** (or compatible Raspberry Pi model with Camera Module V2).
- **Raspberry Pi OS** (latest version).
- **Camera Module** connected to the CSI port.

## Installation

### 1. **Clone the Repository**

Clone the repository to your Raspberry Pi:

```bash
git clone https://github.com/dennisimoo/raspberrypicamera.git
cd raspberrypicamera
2. Update and Install Dependencies
Run the following commands to update your Raspberry Pi and install the necessary dependencies:

bash
Copy
Edit
sudo apt update && sudo apt full-upgrade && sudo rpi-update && sudo reboot
pip3 install Flask
sudo apt install -y python3-opencv python3-picamera2 libcamera-apps libcamera-dev libopencv-dev
3. Enable Camera and Test
Enable the camera using raspi-config:

bash
Copy
Edit
sudo raspi-config nonint do_camera 0
Then, test the camera by running:

bash
Copy
Edit
libcamera-hello
4. Run the Flask Application
Once everything is set up, you can start the Flask app using:

bash
Copy
Edit
python3 working.py
5. Access the Camera Stream
Open a web browser and navigate to:

arduino
Copy
Edit
http://raspberrypi.local:8080/
You should see the live camera feed streaming in MJPEG format.

vbnet
Copy
Edit


ChatGPT can make mistakes. Check important info.

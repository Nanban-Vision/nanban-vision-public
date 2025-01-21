# Nanban Vision Model (Archive)
This is an archived public copy of the final version of the original Nanban vision-based assistive device system. This implementation used Raspberry Pi and YOLOv8 for object detection and distance measurement.

## Overview
Nanban was developed as an assistive device for the visually impaired, combining object detection, distance measurement, and voice assistant capabilities. The system used a Raspberry Pi platform to process camera input and provide auditory feedback to users.

## Core Features

### Object Detection Mode
- Camera-based object detection using YOLOv8
- Distance measurement using geometric calculations
- Real-time object recognition and distance estimation using DepthAnything AI model.

### Voice Assistant Mode
- Real-time information services:
  - Current time and temperature
  - News updates
  - YouTube audio playback
- Interactive voice assistant for user queries

### Hardware Configuration
- Raspberry Pi as the main processing unit
- Dual switch system:
  - Mode switching capability
  - Volume control functionality

## System Components

### Core Files
- `main.py` - System entry point and initialization
- `main_mode.py` - Object detection implementation
- `voice_assistant_mode.py` - Voice assistant services
- `widths.yaml` - Object width reference data
- `pulse.py` - Switch control and volume management
- `Nanban_launcher.desktop` - Raspberry Pi autostart configuration

## Installation Guide

1. Clone the repository:
```bash
git clone https://github.com/arungeorgesaji/Nanban.git
```

2. Install required packages:
```bash
sudo apt-get install pip mpg321
pip install gpiozero pulsectl ultralytics gtts opencv-python pyyaml spotipy requests beautifulsoup4 pytube youtube-search-python pydub SpeechRecognition keyboard youtube-dl huggingface_hub langchain_community openai
```

3. Configure autostart:
   - Create `.config/autostart` directory if it doesn't exist
   - Copy `Nanban_launcher.desktop` to `.config/autostart`
   - Update the path in `Nanban_launcher.desktop` to point to your `main.py` location
   - Reboot the system

## Usage Instructions

1. Hardware Setup:
   - Connect the Raspberry Pi to required peripherals
   - Ensure camera and switches are properly connected

2. System Operation:
   - Launch system via `main.py`
   - Use switches to toggle between modes:
     - Object Detection Mode for environmental awareness
     - Voice Assistant Mode for information services

## Development Notes

### Object Detection
- Utilized YOLOv8 for real-time object detection
- Implemented distance calculation using geometric principles
- Integrated predetermined object width data for accuracy

### Voice Assistant
- Incorporated multiple information services
- Implemented interactive voice communication
- Added multimedia playback capabilities

## Archival Note
This version of Nanban represents the original vision-based implementation. It has been archived to preserve the development history as the project moves forward with new approaches and technologies.

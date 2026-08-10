# AIR PENCIL - Project Explanation

## What this project does

`AIR-PENCIL-main` is a Python-based computer vision application that lets you draw in the air using hand gestures. It tracks a single hand from your webcam and converts finger position and gesture states into drawing actions, color selection, and erase commands.

## Core functionality

- Real-time webcam input using OpenCV
- Hand pose detection using MediaPipe Hands
- Finger state recognition for gesture control
- Drawing on a virtual canvas with the index fingertip
- Color selection and eraser mode
- Smooth coordinate tracking and gesture stabilization
- On-screen overlay for status, mode, and toolbar controls
## Main project components

### `main.py`

This is the main entrypoint for the full AIR PENCIL application.
It uses:
- `HandTracker` from `hand_tracker.py`
- `GestureStabilizer` and gesture detection functions from `gesture.py`
- `Painter` from `painter.py`
- UI drawing helpers from `ui.py`
- Coordinate smoothing from `utils.py`
- Camera capture via OpenCV

`main.py` reads webcam frames, finds the hand landmarks, detects gesture state, and then either draws, selects a color, erases, or shows idle mode.

### `hand_tracker.py`

Handles MediaPipe hand detection and returns:
- a list of 21 hand landmarks as screen coordinates
- whether the hand is `Left` or `Right`

This module also draws the hand skeleton on the camera frame.

### `hand_track_demo.py`

A simpler demo script for testing raw MediaPipe hand tracking and gesture detection.
It shows live webcam output and prints the detected finger state and mode. This is useful for verifying that the webcam and MediaPipe pipeline work correctly.

### Other modules

- `config.py` — stores camera settings, gesture thresholds, toolbar dimensions, and default colors.
- `gesture.py` — determines which fingers are up and maps finger states to gestures such as DRAW, SELECT, ERASE, and CLEAR.
- `painter.py` — maintains the canvas and draws lines based on fingertip movement.
- `ui.py` — draws the toolbar, cursor, interface text, and selected color status.
- `utils.py` — provides smoothing and helper utilities for coordinate handling.

## Technologies used

- Python 3.12
- OpenCV (`opencv-python`) for webcam capture, image display, and drawing overlays
- MediaPipe (`mediapipe`) for hand landmark detection and tracking
- NumPy for numeric operations and coordinate handling
- Additional Python utilities from the local project modules

## Installation and setup

Run these commands from the project folder:

```powershell
cd "C:\Users\user\OneDrive\Desktop\3rd Year\MPro\AIR-PENCIL-main"
py -3.12 -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

If PowerShell blocks activation, you can run directly with the virtual environment Python:

```powershell
.\venv\Scripts\python.exe main.py
```

## How to run

### Full application

From the project folder:

```powershell
.\venv\Scripts\Activate.ps1
python main.py
```

or without activation:

```powershell
.\venv\Scripts\python.exe main.py
```

### Demo script

To run the simpler hand tracking demo:

```powershell
.\venv\Scripts\python.exe hand_track_demo.py
```

## Controls

- Press `C` to clear the drawing canvas
- Press `Q` to quit the application
- Use specific hand gestures to switch modes:
  - Index finger up: draw mode
  - Index + middle finger up: color selection mode
  - All fingers up: erase or clear mode

## Notes

- Make sure your webcam is connected and allowed for use.
- Run the app from the project root so relative imports work correctly.
- If the webcam does not open, check that no other application is using it.

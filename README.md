# ✋ AIR PENCIL

**AIR PENCIL** is a Python-based computer vision application that allows users to draw in the air using hand gestures. It uses a webcam, OpenCV, and MediaPipe to detect hand movements and convert gestures into drawing actions.

## 🚀 Features

* Real-time hand tracking
* 21-point hand landmark detection
* Finger gesture recognition
* Air drawing using the index finger
* Color selection
* Eraser mode
* Canvas clearing
* Smooth fingertip tracking
* Interactive toolbar and status display

## 🛠️ Technologies

* Python 3.12
* OpenCV
* MediaPipe
* NumPy

## 📂 Project Structure

```text
AIR-PENCIL-main/
├── main.py
├── hand_tracker.py
├── hand_track_demo.py
├── gesture.py
├── painter.py
├── ui.py
├── utils.py
├── config.py
├── requirements.txt
└── README.md
```

## ⚙️ Installation

Clone the repository:

```bash
git clone <YOUR-REPOSITORY-URL>
cd AIR-PENCIL-main
```

Create a virtual environment:

```powershell
py -3.12 -m venv venv
```

Activate it:

```powershell
.\venv\Scripts\Activate.ps1
```

Install dependencies:

```powershell
pip install -r requirements.txt
```

## ▶️ Run

Run the main application:

```powershell
python main.py
```

Or directly using the virtual environment:

```powershell
.\venv\Scripts\python.exe main.py
```

For the hand-tracking demo:

```powershell
.\venv\Scripts\python.exe hand_track_demo.py
```

## 🎮 Controls

| Gesture / Key     | Action          |
| ----------------- | --------------- |
| ☝️ Index finger   | Draw            |
| ✌️ Index + Middle | Color selection |
| 🖐️ All fingers   | Erase / Clear   |
| `C`               | Clear canvas    |
| `Q`               | Quit            |

## 🧠 How It Works

```text
Webcam
   ↓
OpenCV
   ↓
MediaPipe Hand Tracking
   ↓
21 Hand Landmarks
   ↓
Finger/Gesture Recognition
   ↓
Drawing / Color / Eraser
   ↓
Virtual Canvas
```

## 🎯 Applications

* Digital drawing
* Touch-free interaction
* Educational demonstrations
* Computer vision projects
* Gesture-based interfaces
* Human-computer interaction

## 🔮 Future Improvements

* Undo/Redo functionality
* More colors and brush sizes
* Save drawings as images
* Air-writing and text recognition
* Multi-hand support
* AI-based gesture recognition

## 👨‍💻 Author

**Nikhil Navale**

B.Tech — Computer Science & Artificial Intelligence

---

⭐ If you find this project useful, consider giving it a star!


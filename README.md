# Drowsiness Detection System

## Overview

The **Drowsiness Detection System** is a computer vision-based application designed to detect driver drowsiness in real time. It uses a webcam to monitor the user's face and eyes, analyzes eye movements and blink patterns, and triggers an alert when signs of drowsiness are detected. This system aims to improve road safety by helping prevent accidents caused by driver fatigue.

---

## Features

* 👁️ Real-time face and eye detection
* 😴 Drowsiness detection using Eye Aspect Ratio (EAR) or facial landmarks
* 🔔 Audio alert when drowsiness is detected
* 🎥 Live webcam monitoring
* ⚡ Fast and lightweight implementation
* 💻 Easy to run on a standard computer

---

## Technologies Used

* Python
* OpenCV
* dlib
* NumPy
* SciPy
* imutils
* playsound (or pygame for alerts)

---

## Project Structure

```text
Drowsiness-Detection-System/
│
├── models/                 # Pre-trained models (shape predictor, etc.)
├── images/                 # Screenshots and output images
├── alarm.wav               # Alert sound
├── drowsiness_detector.py  # Main application
├── requirements.txt        # Required Python packages
├── README.md               # Project documentation
└── LICENSE                 # License file (optional)
```

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/Drowsiness-Detection-System.git
```

2. Navigate to the project directory:

```bash
cd Drowsiness-Detection-System
```

3. Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## Required Dependencies

Install the following packages if they are not included in `requirements.txt`:

```bash
pip install opencv-python
pip install dlib
pip install imutils
pip install scipy
pip install numpy
pip install playsound
```

---

## How It Works

1. The webcam captures live video.
2. The system detects the user's face.
3. Facial landmarks are extracted.
4. Eye Aspect Ratio (EAR) is calculated for both eyes.
5. If the eyes remain closed for a predefined number of consecutive frames, the system identifies the user as drowsy.
6. An alarm sound is played until the eyes are opened again.

---

## Usage

Run the application using:

```bash
python drowsiness_detector.py
```

Press **Q** to quit the application.

---

## Output

* Detects face and eyes in real time.
* Displays the current eye status.
* Triggers an audible alarm when drowsiness is detected.
* Shows live detection on the webcam feed.

---

## Future Improvements

* Support for multiple faces
* Mobile application integration
* Driver performance analytics
* Deep learning-based eye state classification
* Head pose estimation
* Cloud logging and monitoring

---

## Applications

* Driver safety systems
* Fleet management
* Smart vehicles
* Transportation monitoring
* Industrial operator monitoring

---

## Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a new branch.

```bash
git checkout -b feature-name
```

3. Commit your changes.

```bash
git commit -m "Add new feature"
```

4. Push to your branch.

```bash
git push origin feature-name
```

5. Open a Pull Request.

---

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it.

---

## Author

**Your Name**

GitHub: https://github.com/your-username

---

## Acknowledgements

* OpenCV
* dlib
* Python Community
* Research on Eye Aspect Ratio (EAR) for drowsiness detection

---

## Screenshots

Add screenshots of your application here.

```text
Example:

+-------------------------------+
| Live Camera Feed              |
| Face Detected                 |
| Eyes Open                     |
+-------------------------------+

+-------------------------------+
| DROWSINESS ALERT!             |
| Alarm Activated               |
+-------------------------------+
```

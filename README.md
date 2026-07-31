# 🚗 Driver Drowsiness Detection System using YOLOv5

## 📌 Overview

The **Driver Drowsiness Detection System** is a real-time computer vision application developed using **Python**, **OpenCV**, **PyTorch**, and **YOLOv5**. The system detects whether a driver is **awake** or **drowsy** using a custom-trained object detection model.

The project involves collecting images through a webcam, labeling them using LabelImg, training a custom YOLOv5 model, and performing live detection through the webcam.

---

# 🎯 Features

* Real-time drowsiness detection
* Custom YOLOv5 model training
* Webcam image collection
* Image annotation using LabelImg
* Live object detection
* Supports two classes:

  * Awake
  * Drowsy
* Fast and accurate detection

---

# 🛠 Technologies Used

* Python 3.x
* PyTorch
* YOLOv5
* OpenCV
* NumPy
* Matplotlib
* LabelImg

---

# 📂 Project Structure

```text
Driver-Drowsiness-Detection/
│
├── data/
│   ├── images/
│   └── labels/
│
├── yolov5/
│
├── dataset.yml
├── requirements.txt
├── train.py
├── detect.py
├── notebook.ipynb
└── README.md
```

---

# ⚙ Installation

## Clone the Repository

```bash
git clone https://github.com/yourusername/Driver-Drowsiness-Detection.git
cd Driver-Drowsiness-Detection
```

## Install Dependencies

```bash
pip install torch torchvision torchaudio
pip install opencv-python
pip install matplotlib
pip install numpy
pip install pyqt5
pip install lxml
```

Or install everything using

```bash
pip install -r requirements.txt
```

---

# 📸 Dataset Creation

The dataset is created using the system webcam.

Classes used:

* Awake
* Drowsy

The notebook automatically captures images for each class and stores them in:

```text
data/images/
```

Each image is saved with a unique filename.

---

# 🏷 Image Annotation

The project uses **LabelImg** to annotate captured images.
<img width="1920" height="1249" alt="Sample" src="https://github.com/user-attachments/assets/65b16187-1e03-4a96-a78f-269c2ec29249" />
 

Install LabelImg:

```bash
git clone https://github.com/tzutalin/labelImg

pip install pyqt5 lxml
```

Launch LabelImg and annotate all collected images.

---

# 🧠 Model Training

Train the custom YOLOv5 model using:

```bash
python train.py --img 320 --batch 16 --epochs 500 --data dataset.yml --weights yolov5s.pt
```

Training generates model weights inside:

```text
runs/train/
```

---

# 📦 Load Custom Model

Load the trained model:

```python
model = torch.hub.load(
    'ultralytics/yolov5',
    'custom',
    path='yolov5/runs/train/exp/weights/last.pt',
    force_reload=True
)
```

---

# ▶ Run Real-Time Detection

```bash
python detect.py
```

The webcam opens automatically and displays live predictions.

Press **Q** to quit.

---

# 🔄 Workflow

```text
Collect Images
      │
      ▼
Annotate Images
      │
      ▼
Prepare Dataset
      │
      ▼
Train YOLOv5 Model
      │
      ▼
Load Trained Model
      │
      ▼
Real-Time Webcam Detection
```

---

# 📊 Classes

| Class  | Description           |
| ------ | --------------------- |
| Awake  | Driver is alert       |
| Drowsy | Driver appears sleepy |

---

# 📷 Sample Output

```text
Prediction:

Awake
Confidence: 98%

or

Drowsy
Confidence: 96%
```

---

# 🚀 Future Improvements

* Alarm notification when drowsiness is detected
* Eye blink detection
* Face landmark integration
* Mobile deployment
* Raspberry Pi implementation
* TensorRT optimization
* Driver monitoring dashboard

---

# 🤝 Contributing

Contributions are welcome!

1. Fork this repository.
2. Create a feature branch.

```bash
git checkout -b feature-name
```

3. Commit your changes.

```bash
git commit -m "Added new feature"
```

4. Push to GitHub.

```bash
git push origin feature-name
```

5. Open a Pull Request.

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Your Name**

GitHub: https://github.com/faizanalam-1457

LinkedIn: https://linkedin.com/in/faizan-alam1457

---

# 🙏 Acknowledgements

* Ultralytics YOLOv5
* PyTorch
* OpenCV
* LabelImg
* Python Community

---

## ⭐ If you found this project useful, consider giving it a star on GitHub!

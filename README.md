# 🚗 Driver Drowsiness Detection using YOLOv5

## 📌 About the Project

This is a **real-time driver drowsiness detection system** built with **Python**, **OpenCV**, **PyTorch**, and **YOLOv5**. It identifies whether a driver is **awake** or **drowsy** by running inference through a custom-trained object detection model.

The pipeline covers everything end-to-end — capturing training images from a webcam, labeling them with LabelImg, training a custom YOLOv5 detector, and finally running live detection through the webcam feed.

---

## 🎯 Key Features

- Real-time drowsiness monitoring
- Custom-trained YOLOv5 detection model
- Webcam-based dataset collection
- Manual annotation workflow using LabelImg
- Live video inference
- Two-class detection setup:
  - Awake
  - Drowsy
- Lightweight and fast inference speed

---

## 🛠 Tech Stack

- Python 3.x
- PyTorch
- YOLOv5
- OpenCV
- NumPy
- Matplotlib
- LabelImg

---

## 📂 Repository Layout

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

## ⚙ Getting Started

### Step 1 — Clone the Repo

```bash
git clone https://github.com/yourusername/Driver-Drowsiness-Detection.git
cd Driver-Drowsiness-Detection
```

### Step 2 — Install Requirements

```bash
pip install torch torchvision torchaudio
pip install opencv-python
pip install matplotlib
pip install numpy
pip install pyqt5
pip install lxml
```

Or, install everything at once:

```bash
pip install -r requirements.txt
```

---

## 📸 Building the Dataset

Training images are captured directly through the system webcam for two classes:

- Awake
- Drowsy

Each captured frame is automatically saved with a unique filename inside:

```text
data/images/
```

---

## 🏷 Annotating the Images

Once images are collected, they're labeled using **LabelImg**.

<img width="1920" height="1249" alt="Sample" src="https://github.com/user-attachments/assets/65b16187-1e03-4a96-a78f-269c2ec29249" />

**Setup LabelImg:**

```bash
git clone https://github.com/tzutalin/labelImg
pip install pyqt5 lxml
```

Open LabelImg and annotate every image in the dataset.

---

## 🧠 Training the Model

Run the following command to start training the custom YOLOv5 model:

```bash
python train.py --img 320 --batch 16 --epochs 500 --data dataset.yml --weights yolov5s.pt
```

Trained weights will be saved under:

```text
runs/train/
```

---

## 📦 Loading the Trained Model

```python
model = torch.hub.load(
    'ultralytics/yolov5',
    'custom',
    path='yolov5/runs/train/exp/weights/last.pt',
    force_reload=True
)
```

---

## ▶ Running Live Detection

```bash
python detect.py
```

This launches the webcam and shows live predictions on screen.

Press **Q** to exit.

---

## 🔄 End-to-End Workflow

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

## 📊 Detection Classes

| Class  | Meaning                |
| ------ | ----------------------- |
| Awake  | Driver is alert         |
| Drowsy | Driver appears sleepy   |

---

## 📷 Example Output

```text
Prediction:

Awake
Confidence: 98%

or

Drowsy
Confidence: 96%
```

---

## 🚀 What's Next

- Alarm/notification trigger on drowsiness detection
- Eye blink tracking
- Facial landmark integration
- Mobile app deployment
- Raspberry Pi based implementation
- TensorRT optimization for faster inference
- Full driver monitoring dashboard

---

## 🤝 How to Contribute

Contributions are always welcome!

1. Fork this repository.
2. Create a new feature branch.

```bash
git checkout -b feature-name
```

3. Commit your changes.

```bash
git commit -m "Added new feature"
```

4. Push the branch.

```bash
git push origin feature-name
```

5. Open a Pull Request.

---

## 👥 Contributors

- Faizan Alam
- Abu Saad
- Mohd Umar
- Mohd Ayan
- Shadab Firoz

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Your Name**

GitHub: https://github.com/faizanalam-1457

LinkedIn: https://linkedin.com/in/faizan-alam1457

---

## 🙏 Acknowledgements

- Ultralytics YOLOv5
- PyTorch
- OpenCV
- LabelImg
- Python Community

---

### ⭐ If this project helped you, consider giving it a star on GitHub!

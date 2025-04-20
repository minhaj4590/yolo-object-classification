# 🚀 YOLO Object Classification - HackFest Project

This repository contains an end-to-end pipeline for training and evaluating an object classification model using the YOLO (You Only Look Once) architecture. It is tailored for a small, custom dataset and utilizes Ultralytics’ implementation of YOLOv3.

---

## 🎯 Project Aim

To train and evaluate a YOLO model for **object classification** using a custom dataset. This project involves:
- Installing dependencies
- Training a YOLO model
- Testing and predicting
- Visualizing the results

---

## 📁 Directory Structure

Hackfest/ ├── Hackfest.py # Main script: installs dependencies & runs train/test ├── train.py # Contains training code ├── test.py # Loads trained model & plots predictions ├── yolov3u.pt # YOLO base model weights ├── yolo_params.yaml # YOLO-compatible dataset configuration ├── Hackfest_dataset/ │ ├── data/ │ │ ├── train/ │ │ │ ├── images/ │ │ │ └── labels/ │ │ └── test/ │ │ └── images/ ├── README.md # This file

yaml
Copy
Edit

---

## ⚙️ Step-by-Step Setup Instructions

### 1. 📦 Clone the Repository

```bash
git clone https://github.com/yourusername/yolo-object-classification.git
cd yolo-object-classification
2. ▶️ Run the Main Script
Hackfest.py handles everything for you:

bash
Copy
Edit
python Hackfest.py
This script:

Installs required dependencies

Runs train.py to train the model

Executes test.py to make predictions and visualize results

⚠️ Make sure you are connected to the internet for dependency installation.

🧠 How it Works
🔧 train.py:
Trains a YOLOv3 model using custom hyperparameters

Uses yolo_params.yaml for dataset paths and class names

Saves trained model and logs under the runs/ directory

🧪 test.py:
Loads the best trained model

Runs predictions on test set images

Plots and saves prediction results (bounding boxes, confidence scores)

📜 Dataset Format
Make sure your dataset is structured like this:

bash
Copy
Edit
Hackfest_dataset/
└── data/
    ├── train/
    │   ├── images/       # Training images (.jpg/.png)
    │   └── labels/       # YOLO-format .txt files (same name as image)
    └── test/
        └── images/       # Testing images only
🧾 yolo_params.yaml Format Example:
yaml
Copy
Edit
train: Hackfest_dataset/data/train/images
val: Hackfest_dataset/data/train/images
test: Hackfest_dataset/data/test/images

nc: 3
names: ['ClassA', 'ClassB', 'ClassC']
Update class names and count (nc) as per your dataset.

📊 Output
Trained weights saved in runs/train/exp*/weights/best.pt

Test results and prediction plots saved via test.py

✅ Requirements
If you’re not using Hackfest.py, you can install manually:

bash
Copy
Edit
pip install ultralytics matplotlib opencv-python
🧾 Notes
Make sure your YOLO annotation format is correct: each .txt label file should contain rows like:

arduino
Copy
Edit
class_id center_x center_y width height
(all normalized between 0 and 1)

📄 License
This project is licensed under the MIT License.

🙌 Acknowledgments:
Ultralytics YOLO

HackFest Challenge organizers
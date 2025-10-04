# 🚗 Driver Monitoring System using YOLOv8  

## 📖 Overview  
Have you ever seen a driver secretly use their phone while driving?  
I noticed this recently — a driver holding his phone low near the steering wheel at a red light, trying to hide it from the traffic sergeant.  

It made me realize: the real danger isn’t being caught — it’s the risk of losing focus for even a few seconds.  

That inspired me to build this small project using **YOLOv8**:  
👉 Detecting phone usage by drivers in video footage.  

This project demonstrates how computer vision can highlight risky behavior on the road and how AI can contribute to **road safety**.  

🔮 In the future, this project can be extended to detect:  
- Drowsiness  
- Seatbelt usage  
- Eating or drinking while driving  

---

## ⚙️ Features  
- Real-time detection of driver phone usage.  
- Implementation using **Google Colab** for easy reproducibility.  
- Pre-trained YOLOv8 model with transfer learning for custom dataset.  
- Demo video results uploaded for demonstration.  

---

## 📂 Project Structure  
```
├── data/              # Training / testing dataset
├── notebooks/         # Google Colab notebook(s)
├── results/           # Detection outputs and demo videos
├── README.md          # Project documentation
```

---

## 🚀 Getting Started  

### 1. Clone the Repository  
```bash
git clone https://github.com/yourusername/driver-monitoring-yolov8.git
cd driver-monitoring-yolov8
```

### 2. Open in Google Colab  
- Upload the provided **notebook** from `notebooks/` into Google Colab.  
- Make sure to enable **GPU runtime** in Colab.  

### 3. Install Dependencies  
Inside Colab, run:  
```bash
!pip install ultralytics
!pip install roboflow
```

### 4. Run Training / Detection  
- Train your model:  
```python
from ultralytics import YOLO

# Load YOLOv8 and start training
model = YOLO("yolov8n.pt")  
model.train(data="data.yaml", epochs=50, imgsz=640)
```

- Run detection on test video:  
```python
model.predict(source="driver_test_video.mp4", save=True)
```

---

## 📊 Results  
Sample output showing phone detection in driver footage:  

![output](https://github.com/user-attachments/assets/7690e61e-db77-44e8-819d-bc2ab8b01c6e)


> The model successfully highlights risky behavior like phone usage during driving.  

---

## 💡 Motivation  
This project was inspired by real-life observation:  
📱🚦 A driver trying to hide his phone from the traffic sergeant at a signal.  
It showed me that the **bigger danger is distraction, not punishment.**  

---

## 🔮 Future Scope  
- Extend to **multi-class detection**: seatbelts, drowsiness, smoking, eating.  
- Integrate with real-time **vehicle monitoring systems**.  
- Deploy on edge devices like Raspberry Pi for **in-car applications**.  

---



## 🛠️ Tech Stack  
- **Python**  
- **YOLOv8 (Ultralytics)**  
- **Google Colab**  
- **OpenCV**  

---

## ✨ Credits  
- YOLOv8 by [Ultralytics](https://github.com/ultralytics/ultralytics)  
- Dataset preprocessing via [Roboflow](https://roboflow.com/)  

---

## 📢 Connect  
If you liked this project, feel free to ⭐ the repo and share!  
Let’s work together to make **roads safer with AI.**  

#AI #YOLOv8 #ComputerVision #RoadSafety  

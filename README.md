# Electronic Component Detection using YOLOv8

🎯 **Project Overview**  
This project demonstrates real-time detection of electronic components—including resistors, capacitors, LEDs, diodes, transistors, and Zener diodes—using a custom-trained YOLOv8 model and OpenCV. Built and trained by **Hassan Mroueh**, it enables accurate, offline component recognition from a live camera feed.

---

## 📁 Project Structure

- `main.py` – Python script to run real-time inference on webcam using OpenCV and the `best.pt` model.
- `electronic-components-detection (2).ipynb` – Google Colab notebook used to train the YOLOv8 model on a public dataset from Roboflow.
- `best.pt` – Trained YOLOv8 model weights.
- `simulation-images/` – Screenshots showing sample detection results in real-world scenarios.

---

## 🧪 Run Detection Locally

After installing dependencies, run the detection:

```bash
pip install ultralytics opencv-python
python main.py
```

Ensure `best.pt` is in the same folder as `main.py`.

---

## 📥 Dataset Credits

This project uses data from the **Electronics Components Dataset** by [Jovine](https://universe.roboflow.com/jovine/electronics-components), hosted on Roboflow Universe.

**Citation:**

```bibtex
@misc{electronics-components_dataset,
    title = {Electronics components Dataset},
    type = {Open Source Dataset},
    author = {Jovine},
    howpublished = {\url{https://universe.roboflow.com/jovine/electronics-components}},
    url = {https://universe.roboflow.com/jovine/electronics-components},
    journal = {Roboflow Universe},
    publisher = {Roboflow},
    year = {2023},
    month = {sep},
    note = {visited on 2025-05-23},
}
```

---

## 📚 How to Train It Yourself

1. Visit the dataset: [Electronics Components on Roboflow](https://universe.roboflow.com/jovine/electronics-components)
2. Download the dataset in **YOLOv8 PyTorch** format.
3. Upload the ZIP to Google Colab.
4. Use this Python code to train:

```python
from ultralytics import YOLO
model = YOLO('yolov8n.pt')
model.train(data='path/to/data.yaml', epochs=50, imgsz=640)
```

5. The trained model will be saved in `runs/detect/train/weights/best.pt`.

---

## 📷 Example Predictions

You can view sample predictions in the `simulation-images/` folder:
- 📌 Resistor detection
- 📌 Breadboard circuit analysis
- 📌 Capacitor and transistor identification
- 📌 Real-time webcam usage

---

## 👤 Author

**Hassan Mroueh**  
Using YOLOv8, OpenCV, and a publicly available dataset by [Jovine](https://universe.roboflow.com/jovine/electronics-components).


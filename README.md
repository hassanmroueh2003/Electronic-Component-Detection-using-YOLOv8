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


# 🎭 DeepFake Detection (Lightweight Demo)

This project is a **simple DeepFake detection demo** that processes a video and assigns random “REAL” or “FAKE” labels to each frame.
It demonstrates how a DeepFake detection pipeline can be structured using **OpenCV**, **TensorFlow/Keras**, and **MoviePy** — ready to be extended with a trained deep learning model.

---

## 📂 Project Overview

The current implementation serves as a **template** or **prototype** for future DeepFake detection work.
Instead of using a trained model, it generates **random fake probabilities** (0–1) for each frame and overlays labels (`REAL` or `FAKE`) on the video.

---

## ⚙️ Features

✅ Reads and processes any input video file.
✅ Simulates fake detection probabilities.
✅ Annotates each frame with labels and confidence values.
✅ Saves the processed video with overlaid text.
✅ Modular and extendable design — ready for integration with real models.

---

## 🧰 Requirements

Install the required Python packages before running the code:

```bash
!pip install imageio==2.4.1
!pip install imageio-ffmpeg
!pip install opencv-python moviepy tensorflow keras
```

---

## 🧠 How It Works

1. The `DeepFake_Utils` class contains a static method:

   ```python
   DeepFake_Utils.Inference_on_video(output_path, input_path)
   ```
2. It reads each frame of the input video using OpenCV.
3. Generates a random number between 0 and 1 as a dummy “fake probability”.
4. Assigns:

   * `REAL` if probability ≤ 0.5
   * `FAKE` if probability > 0.5
5. Draws the label and probability on each frame.
6. Writes the annotated frames into a new output video.

---

## ▶️ Example Usage

```python
InputVideoPath = "/content/sample_data/Deepfake1.mp4"
OutputVideoPath = "output.mp4"

DeepFake_Utils.Inference_on_video(OutputVideoPath, InputVideoPath)
```

**Output:**
A processed video named `output.mp4` containing frame-by-frame predictions and confidence scores.

---

## 📦 Output Example

Each frame will display a label in the top-left corner:

```
REAL (0.32)
```

or

```
FAKE (0.85)
```

Green = REAL
Red = FAKE

---

## 🚀 Future Improvements

* Integrate a **pretrained CNN or Transformer model** for real DeepFake detection.
* Add **face detection and alignment** for better accuracy.
* Support **batch processing** of multiple videos.
* Visualize fake probability trends over time.

---

## 🧑‍💻 Author

**Sanvi Kumari**
💻 B.Tech in Computer Science and Engineering
🌐 Web Developer | AI & Deep Learning Enthusiast


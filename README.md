# 🎭 Real-Time Face Swap (SimSwap + ArcFace ONNX)

This repository contains an implementation of a **real-time face swapping system** powered by **SimSwap** and **ArcFace**, exported to the **ONNX format** for efficient inference.  
The project uses **ONNXRuntime** for model execution, **OpenCV** for video/image handling, and **MediaPipe** for face detection.  

The goal is to provide a **lightweight, GPU-accelerated pipeline** that can take an identity face (from a source image) and swap it seamlessly onto faces detected in live video or static images.  
It is designed to be **modular, extensible, and educational**, making it easy to adapt for research projects, demos, or experimentation with real-time face generation.

---

## ✨ Key Features
- 🚀 **ONNXRuntime GPU Acceleration**  
  Runs on NVIDIA GPUs via CUDA and TensorRT for maximum performance, with CPU fallback support.  

- 🧑‍💻 **ArcFace r100 Embedding**  
  Extracts robust identity embeddings from the source image using the ArcFace ONNX model.  

- 🎨 **SimSwap Face Generator**  
  The core generator (`simswap_256.onnx`) produces high-quality swapped faces at **256×256 resolution**.  
  (Optional: support for 512×512 for sharper but heavier results.)  

- 🎥 **Real-Time Webcam Demo**  
  Swap faces live using your webcam. Includes error handling for missed detections.  

- 🖌️ **Advanced Blending Options**  
  - **Poisson blending**: Smooth, natural integration of the swapped face into the target frame.  
  - **Feather blending**: Lightweight blending method for faster performance.  

- ⚙️ **Modular Pipeline**  
  Easily replace the face detector (e.g., SCRFD ONNX for GPU-based detection) or extend preprocessing/postprocessing steps.  

---

## 📂 Project Structure

A suggested layout for organizing the project files:


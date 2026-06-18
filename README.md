# 🚗 License Plate Detector

A professional web-based license plate detection system powered by YOLOv8 and ONNX Runtime Web.

## Features

- **Image Detection**: Upload images to detect license plates
- **Video Detection**: Process uploaded video files frame by frame
- **Live Webcam**: Real-time detection from your camera feed
- **Customizable Thresholds**: Adjust confidence and NMS thresholds
- **Download Results**: Export annotated detection images
- **No Server Required**: Everything runs client-side in the browser

## Deployment (GitHub Pages)

### 1. Convert your model to ONNX

```python
from ultralytics import YOLO
model = YOLO('best.pt')
model.export(format='onnx', opset=12, simplify=True, half=False)

# football-detection-tracking

**Object Detection & Tracking for Football (Soccer) Footage**  
Leverage computer vision to detect and track players and the ball in football videos using state-of-the-art models like YOLO and tracking algorithms such as DeepSORT or ByteTrack.

---

##  Features

- **Real-time Object Detection**: Detect players, the ball, and referees in each video frame.
- **Multi‑Object Tracking**: Track players and the ball across frames using algorithms like Deep SORT, ByteTrack, or DeepSORT-enhanced variants.
- **Flexible Architecture**: Modular implementation allowing easy swapping of detection (e.g., YOLOv5, YOLOv8) and tracking backends.
- **Visualization Tools**: Annotated video outputs with bounding boxes, IDs, and trajectories.
- **Configurable Pipelines**: Adjustable settings via configuration files or command-line arguments (e.g., detection thresholds, model paths).

---

##  Directory Structure

```

football-detection-tracking/
├── object\_detection/         # Detection module (e.g. YOLOv5, YOLOv8 models & utilities)
├── object\_tracking/          # Tracking module (e.g. DeepSORT, ByteTrack integration)
├── notebooks/                # Jupyter notebooks for demos and experiments
└── README.md                 # This documentation
````


##  Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/Niloofar1381/football-detection-tracking.git
cd football-detection-tracking
````

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Download or train detection model(s)

* Use a pre-trained YOLOv8 model (e.g. from Ultralytics), or
* Train on a dataset such as \[Roboflow’s football player detection dataset] or a \[Kaggle football‑players detection dataset] ([GitHub][1]).

### 4. Run detection & tracking

```bash
python object_tracking/run_tracking.py \
  --detect-model path/to/yolov8_model.pt \
  --video path/to/input.mp4 \
  --output path/to/output.mp4 \
  --tracker deepsort
```

*(Adjust options to match your CLI interface.)*

### 5. View results

* Output video will show bounding boxes, object IDs, and optionally trajectories.
* Logging information will appear in the console or saved to `.log` files.



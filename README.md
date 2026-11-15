# Traffic Video Object Tracking & Annotation Dataset

This repository contains frame-by-frame object tracking annotations for a traffic surveillance video, created using **CVAT (Computer Vision Annotation Tool)**.

## Overview
* **Task Type:** Multi-Object Tracking (MOT) / 2D Bounding Box Annotation
* **Annotation Tool:** CVAT (Computer Vision Annotation Tool)
* **Export Format:** CVAT for video 1.1 (`annotations.xml`)
* **Video Source:** `istockphoto-2193558699-640_adpp_i` (375+ frames)

## Annotated Classes
The dataset includes continuous track IDs across video frames for the following road participants:
* `car`
* `Bike`
* *(Add any other labels you used here, e.g., `truck`, `bus`, `auto`, `person`)*

## Repository Structure
```text
├── annotations.xml   # CVAT for video 1.1 XML file containing all bounding boxes and track IDs
└── README.md         # Project documentation
```

## How to Use
1. **Re-open in CVAT:** Create a new task in CVAT with the original video file, open the task menu, click **Upload annotations**, select **CVAT 1.1**, and upload `annotations.xml`.
2. **Convert for Training:** You can convert `annotations.xml` into standard training formats (such as **YOLO**, **COCO**, or **MOT**) using the [Datumaro](https://github.com) CLI or Python library:
   ```bash
   datum convert -if cvat -i annotations.xml -f coco -o ./coco_output
   ```

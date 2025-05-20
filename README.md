# Instance Segmentation on Simpsons Dataset using YOLOv8

This project performs instance segmentation on a custom Simpsons character dataset using the YOLOv8 model from the Ultralytics library. The goal is to detect and segment individual characters using polygon mask annotations in COCO format.

## Project Structure

- `data/` – Training and validation images and COCO-style annotations
- `yolo/` – Scripts for training and evaluation
- `notebooks/` – Optional Jupyter notebooks for visualization
- `runs/` – Output folder containing trained weights and predictions
- `results/` – Sample output images with masks and labels

## Dataset

The dataset contains images of Simpsons characters with instance segmentation labels (polygons) in COCO format. The `simpsons.yaml` file defines paths to the training and validation data and class names.

Example `simpsons.yaml` structure:

```yaml
path: data/
train: images/train
val: images/val

nc: 5
names: ['Homer', 'Bart', 'Marge', 'Lisa', 'Maggie']

```
## Installing requirements

    pip install -r requirements.txt

## Training

  yolo task=segment mode=train model=yolov8n-seg.pt data=simpsons.yaml epochs=50 imgsz=640

## Evaluation

  yolo task=segment mode=val model=runs/segment/train/weights/best.pt data=simpsons.yaml

## Inference

- Run prediction on a single image:

  yolo task=segment mode=predict model=runs/segment/train/weights/best.pt source=sample.jpg

- Run prediction on a folder of images:

  yolo task=segment mode=predict model=runs/segment/train/weights/best.pt source=data/test_images/

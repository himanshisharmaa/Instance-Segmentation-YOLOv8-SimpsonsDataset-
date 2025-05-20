# Instance Segmentation on Simpsons Dataset using YOLOv8

This project performs instance segmentation on the Simpsons character dataset using the YOLOv8 model from the Ultralytics library. The goal is to detect and segment individual characters from images.

## Project Structure

- `data/` - Contains training and validation images and annotation files
- `yolo/` - YOLOv8 model configuration and training scripts
- `notebooks/` - Jupyter notebooks for data visualization and evaluation
- `runs/` - Saved model runs and results
- `results/` - Sample predictions and visualizations

## Dataset

The Simpsons dataset includes labeled images of characters from the show, annotated for instance segmentation. Annotations are in COCO format.

## Requirements

- Python 3.8+
- Ultralytics YOLOv8
- PyTorch
- OpenCV
- Matplotlib
- Jupyter (optional for running notebooks)

Install requirements:

```bash
pip install -r requirements.txt

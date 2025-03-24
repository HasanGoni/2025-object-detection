# Object Detection

> A PyTorch-based object detection library with fastai style

## Install

```bash
pip install objdetect
```

## How to use

The library will provide simple, intuitive APIs for training and deploying object detection models.

```python
from objdetect.data import ObjectDetectionDataset
from objdetect.models import FasterRCNN
from objdetect.learner import ObjectDetectionLearner

# Create dataset
dataset = ObjectDetectionDataset.from_coco('/path/to/coco')

# Create model
model = FasterRCNN(num_classes=dataset.num_classes)

# Create learner
learn = ObjectDetectionLearner(dataset, model)

# Train
learn.fit_one_cycle(10, 1e-3)

# Predict
img = learn.predict('path/to/image.jpg')
learn.show_results(img)
```

## Features

- Fast and simple training of object detection models
- Multiple backbones (ResNet, EfficientNet, etc.)
- Multiple detection heads (Faster R-CNN, YOLO, SSD, etc.)
- Data augmentation tailored for object detection
- Integration with standard datasets (COCO, Pascal VOC, etc.)
- Visualization tools for model interpretation

## Development

This project is built with [nbdev](https://nbdev.fast.ai/). To contribute:

1. Install nbdev: `pip install nbdev`
2. Clone this repo
3. Install dev requirements: `pip install -e ".[dev]"`
4. Modify or create notebooks in the `nbs` folder
5. Run `nbdev_build_lib` to build the library
6. Run `nbdev_test` to test the library
7. Run `nbdev_build_docs` to build documentation
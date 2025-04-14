# 🧵 Fashion Item Detection & Recognition with YOLOv8

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![YOLOv8](https://img.shields.io/badge/YOLO-v8-green.svg)](https://github.com/ultralytics/ultralytics)

This project implements a fashion object detection model and can classify into 10 different categories using **YOLOv8** to identify and classify various clothing items in images, such as tops, pants, dresses, and accessories.

## Sample

![sample](https://github.com/user-attachments/assets/4b6dcd69-4031-4302-8014-ded15ebabc9f)


## ✨ Features

- Detection of 10 fashion categories including: sunglasses, hats, jackets, shirts, pants, shorts, skirts, dresses, bags, and shoes
- Preprocessing of image data and YOLO format annotations
- Custom training pipeline with YOLOv8
- Evaluation metrics and performance visualization
- Inference capabilities for new images

## 📊 Dataset

This project uses the Colorful Fashion Dataset for Object Detection, which includes:

- Images of fashion items in various settings
- YOLO format annotations (class_id, x_center, y_center, width, height)
- 10 fashion categories
- Train/validation/test splits

[Dataset Link](https://www.kaggle.com/datasets/nguyngiabol/colorful-fashion-dataset-for-object-detection)

The dataset structure is organized as follows:

```
colorful_fashion_dataset/
├── JPEGImages/           # Image files (.jpg)
├── Annotations_txt/      # YOLO format annotations (.txt)
└── ImageSets/Main/       # Train/test/val splits
    ├── trainval.txt
    └── test.txt
```

## 📈 Model Performance

After training for 40 epochs, the model achieved the following performance metrics:

| Class    | Precision | Recall | mAP@0.5 | mAP@0.5:0.95 |
| -------- | --------- | ------ | ------- | ------------ |
| All      | 0.768     | 0.766  | 0.787   | 0.545        |
| Pants    | 0.934     | 0.912  | 0.959   | 0.765        |
| Hat      | 0.812     | 0.818  | 0.830   | 0.496        |
| Shirt    | 0.786     | 0.850  | 0.836   | 0.617        |
| Dress    | 0.686     | 0.852  | 0.821   | 0.670        |
| Skirt    | 0.771     | 0.852  | 0.819   | 0.656        |
| Jacket   | 0.798     | 0.764  | 0.837   | 0.662        |
| Shorts   | 0.780     | 0.796  | 0.780   | 0.518        |
| Bag      | 0.758     | 0.721  | 0.771   | 0.455        |
| Shoe     | 0.798     | 0.812  | 0.830   | 0.468        |
| Sunglass | 0.556     | 0.280  | 0.383   | 0.144        |

## Metrics

![PR_curve](https://github.com/user-attachments/assets/6f018c1b-ac44-4f1a-97df-ca5cd199bd3f)
![confusion_matrix](https://github.com/user-attachments/assets/e6a249b7-4d5d-42b5-aef4-1b4788e45eed)
![labels](https://github.com/user-attachments/assets/afdf5e4c-a7f0-4f92-8b30-996c1a87509d)

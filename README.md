# Project_Anomaly_Segmentation
Add erfnet_pretrained.pth to checkpoint. Add everything useful that was used on Colab

# Anomaly Segmentation Eval (TAKEN FROM README.MD OF TA)

In this folder you can find some functions to evaluate your model's output. It is designed to load the ERFNet checkpoint so you need to change it when evaluating the EoMT model. The main function to look for is evalAnomaly.py that produces the Anomaly Segmentation results.

## Requirements:

It could work with the default runtime of Colab or other versions of the libraries but these are the requirements this code was tested on.

* [**Python 3.6**](https://www.python.org/): If you don't have Python3.6 in your system, I recommend installing it with [Anaconda](https://www.anaconda.com/download/#linux)
* [**PyTorch**](http://pytorch.org/): Make sure to install the Pytorch version for Python 3.6 with CUDA support (code only tested for CUDA 8.0 but it should work with higher versions).
* **Additional Python packages**: numpy, matplotlib, Pillow, torchvision and visdom (optional for --visualize flag)
* **For testing the anomaly segmentation model**: Road Anomaly, Road Obstacle, and Fishyscapes dataset. All testing images are provided here [Link](https://drive.google.com/file/d/1r2eFANvSlcUjxcerjC8l6dRa0slowMpx/view).

## Anomaly Inference:

* Anomaly Inference Command:```python evalAnomaly.py --input '/home/amarinai/segmentation/unk-dataset/RoadAnomaly21/images/*.png```. Change the dataset path ```'/home/amarinai/segmentation/unk-dataset/RoadAnomaly21/images/*.png```accordingly.

## evalAnomaly.py

This code can be used to produce anomaly segmentation results on various anomaly metrics on the validation datasets you can download [here](https://drive.google.com/file/d/1zcayoIIJztxKuHOIjmSjGoQBDy4RdETr/view?usp=drive_link)

**Examples:**
```
python evalAnomaly.py --input "/content/drive/MyDrive/Anomaly_Validation_Datasets/Validation_Dataset/RoadAnomaly21/images/*.png"
python evalAnomaly.py --input "/content/drive/MyDrive/Anomaly_Validation_Datasets/Validation_Dataset/RoadObsticle21/images/*.webp" 
python evalAnomaly.py --input "/content/drive/MyDrive/Anomaly_Validation_Datasets/Validation_Dataset/FS_LostFound_full/images/*.png"
python evalAnomaly.py --input "/content/drive/MyDrive/Anomaly_Validation_Datasets/Validation_Dataset/fs_static/images/*.jpg"
python evalAnomaly.py --input "/content/drive/MyDrive/Anomaly_Validation_Datasets/Validation_Dataset/RoadAnomaly/images/*.jpg" 
```


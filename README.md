This guide will direct you about how to install and use this model in google colaboratory. The locations will need to be changed to be used on a local system. Ensure that you have all the dependencies.

# Installation
Create a directory named BacteriaDetection in your google drive.
In the directory, create a new colab notebook.
Mount your drive to the notebook by running the cell below


```python
from google.colab import drive
drive.mount('/content/drive')
```


Navigate to the directory by running the cell below


```python
%cd /content/drive/MyDrive/BacteriaDetection
```

    [Errno 2] No such file or directory: '/content/drive/MyDrive/BacteriaDetection'
    /Users/karan/Desktop/Codes/BacteriaDetection/BacteriaDetection


Clone this repository to the current directory by running the cell below


```python
!git clone https://github.com/jhakaran1/BacteriaDetection.git
```

    Cloning into 'BacteriaDetection'...
    remote: Enumerating objects: 90, done.[K
    remote: Counting objects: 100% (60/60), done.[K
    remote: Compressing objects: 100% (43/43), done.[K
    remote: Total 90 (delta 26), reused 48 (delta 16), pack-reused 30[K
    Receiving objects: 100% (90/90), 163.58 MiB | 12.28 MiB/s, done.
    Resolving deltas: 100% (36/36), done.
    Updating files: 100% (17/17), done.


Navigate to the directory BacteriaDetection/YoloV5L


```python
%cd BacteriaDetection/YoloV5L/
```

    /Users/karan/Desktop/Codes/BacteriaDetection/BacteriaDetection/BacteriaDetection/YoloV5L


Clone the yolov5 repository and install requirements.txt in a Python>=3.8.0 environment


```python
!git clone https://github.com/ultralytics/yolov5  # clone
%cd yolov5
%pip install -qr requirements.txt  # install
```

    Cloning into 'yolov5'...
    remote: Enumerating objects: 15921, done.[K
    remote: Counting objects: 100% (41/41), done.[K
    remote: Compressing objects: 100% (28/28), done.[K
    remote: Total 15921 (delta 17), reused 28 (delta 13), pack-reused 15880[K
    Receiving objects: 100% (15921/15921), 14.66 MiB | 13.01 MiB/s, done.
    Resolving deltas: 100% (10916/10916), done.
    /Users/karan/Desktop/Codes/BacteriaDetection/BacteriaDetection/BacteriaDetection/YoloV5L/yolov5
    [31mERROR: pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.
    spyder 5.3.3 requires pyqt5<5.16, which is not installed.
    spyder 5.3.3 requires pyqtwebengine<5.16, which is not installed.
    daal4py 2021.6.0 requires daal==2021.4.0, which is not installed.
    anaconda-project 0.11.1 requires ruamel-yaml, which is not installed.
    numba 0.55.1 requires numpy<1.22,>=1.18, but you have numpy 1.22.4 which is incompatible.
    conda-repo-cli 1.0.20 requires clyent==1.2.1, but you have clyent 1.2.2 which is incompatible.
    conda-repo-cli 1.0.20 requires nbformat==5.4.0, but you have nbformat 5.9.2 which is incompatible.[0m[31m
    [0mNote: you may need to restart the kernel to use updated packages.


Move detect_new.py from "YoloV5L" directory to "yolov5" folder.

Now you are ready to use the model for detecting cells in microfluidic channels. In the drive go to Detect.ipynb and follow the instructions to run the model on your images.

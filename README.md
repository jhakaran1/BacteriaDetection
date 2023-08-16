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


Clone this repository to the current directory by running the cell below


```python
!git clone https://github.com/jhakaran1/BacteriaDetection.git
```


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



Move detect_new.py from "YoloV5L" directory to "yolov5" folder.

Now you are ready to use the model for detecting cells in microfluidic channels. In the drive go to Detect.ipynb and follow the instructions to run the model on your images.

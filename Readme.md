{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": []
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "source": [
        "This guide will direct you about how to install and use this model in google colaboratory. The locations will need to be changed to be used on a local system. Ensure that you have all the dependencies."
      ],
      "metadata": {
        "id": "y-CcwF0EexZg"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "# Installation\n",
        "Create a directory named BacteriaDetection in your google drive.\n",
        "In the directory, create a new colab notebook.\n",
        "Mount your drive to the notebook by running the cell below"
      ],
      "metadata": {
        "id": "KgW5axmEgqqY"
      }
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "nL_O5DrcWsJ2",
        "outputId": "3cec1b00-dddb-4095-beef-650ec7a52b74"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Mounted at /content/drive\n"
          ]
        }
      ],
      "source": [
        "from google.colab import drive\n",
        "drive.mount('/content/drive')"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "\n",
        "Navigate to the directory by running the cell below"
      ],
      "metadata": {
        "id": "GTIIJelpXjfp"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "%cd /content/drive/MyDrive/BacteriaDetection"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "TcCdCPlrW4T6",
        "outputId": "362f9f8e-b59e-4f1b-f07c-8fc6af025db4"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "/content/drive/MyDrive/BacteriaDetectioTest\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "Clone this repository to the current directory by running the cell below"
      ],
      "metadata": {
        "id": "ofrphiq4h409"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "!git clone https://github.com/jhakaran1/BacteriaDetection.git"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "4HlGfrWwW_gP",
        "outputId": "1a97d4fd-3800-4210-bf28-8edcd8d255f6"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Cloning into 'BacteriaDetection'...\n",
            "remote: Enumerating objects: 51, done.\u001b[K\n",
            "remote: Counting objects: 100% (21/21), done.\u001b[K\n",
            "remote: Compressing objects: 100% (15/15), done.\u001b[K\n",
            "remote: Total 51 (delta 6), reused 17 (delta 5), pack-reused 30\u001b[K\n",
            "Receiving objects: 100% (51/51), 163.47 MiB | 13.63 MiB/s, done.\n",
            "Resolving deltas: 100% (16/16), done.\n",
            "Updating files: 100% (14/14), done.\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "Navigate to the directory BacteriaDetection/YoloV5L"
      ],
      "metadata": {
        "id": "QZxPUj7OiKQ1"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "%cd BacteriaDetection/YoloV5L/"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "1Ddph078iE3y",
        "outputId": "7f4b9426-d51f-427d-9aeb-e4ca2ae97499"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "/content/drive/MyDrive/BacteriaDetectioTest/BacteriaDetection/YoloV5L\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "Clone the yolov5 repository and install requirements.txt in a Python>=3.8.0 environment"
      ],
      "metadata": {
        "id": "1N6b2zJ1iZGl"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "!git clone https://github.com/ultralytics/yolov5  # clone\n",
        "%cd yolov5\n",
        "%pip install -qr requirements.txt  # install"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "6w39zCyqXLWg",
        "outputId": "aef17fb8-7276-4fb3-c7f7-de3d6e952f09"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Cloning into 'yolov5'...\n",
            "remote: Enumerating objects: 15921, done.\u001b[K\n",
            "remote: Counting objects: 100% (41/41), done.\u001b[K\n",
            "remote: Compressing objects: 100% (28/28), done.\u001b[K\n",
            "remote: Total 15921 (delta 17), reused 28 (delta 13), pack-reused 15880\u001b[K\n",
            "Receiving objects: 100% (15921/15921), 14.66 MiB | 11.18 MiB/s, done.\n",
            "Resolving deltas: 100% (10916/10916), done.\n",
            "Updating files: 100% (142/142), done.\n",
            "/content/drive/MyDrive/BacteriaDetectioTest/BacteriaDetection/YoloV5L/yolov5\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m188.5/188.5 kB\u001b[0m \u001b[31m2.4 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m612.1/612.1 kB\u001b[0m \u001b[31m6.6 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m62.7/62.7 kB\u001b[0m \u001b[31m5.0 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25h"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "Now you are ready to use the model for detecting cells in microfluidic channels. In the drive go to Detect.ipynb and follow the instructions to run the model on your images."
      ],
      "metadata": {
        "id": "HKjsxq_vjFLs"
      }
    }
  ]
}
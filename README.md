# Car detector

Python script for detecting a car in video and saving the ROI, which in this case is the car, to disk. 

## Getting Started

### Prerequisites

It is necessary to have installed imutils, numpy and opencv.

### Installing

Download the source code directly from Github and unzip or clone it using 

```
git clone https://github.com/hlxsrc/car_detection.git
```

Once cloned or unzipped change into the main folder

```
cd car_detection
```

## Program usage

### Arguments 

The necessary arguments to run the program are

* "-p" or "--prototxt" which is the path to Caffe 'deploy' prototxt file.
* "-m" or "--model" which is the path to Caffe pre-trained model.
* "-c" or "--confidence" this is the minimum probability to filter weak detections, default is "0.2".
* "-v", "--video" the path to the video file.
* "-o", "--output" the path to the output directory where the captures of the ROI will be stored.

### Usage

This is an example of the usage

```
python car_detection_filevideo.py \
--prototxt MobileNetSSD_deploy.prototxt.txt \
--model MobileNetSSD_deploy.caffemodel \
--confidence 0.7 \
--video /path/to/the/video.mp4 \
--output output/
```

## Testing

Once the program is running, you can choose between taking a capture of the ROI or quit the program, using the following keys:

* "k" for taking a capture
* "q" to quit the program


## Acknowledgments

This program is based on
* [Real-time Object Detection](https://www.pyimagesearch.com/2017/09/18/real-time-object-detection-with-deep-learning-and-opencv/) - Created by Adrian Rosebrock 
* [How to build a custom face recognition dataset](https://www.pyimagesearch.com/2018/06/11/how-to-build-a-custom-face-recognition-dataset/) - Created by Adrian Rosebrock
* [Model](https://github.com/chuanqi305/MobileNet-SSD) - Trained by chuanqi305


## Notes

* MobileNet SSD was first trained to detect 20 objects, in this scenario we are just interested in cars. 
* Bounding box and label are deactivated by default, they are included in the code and can be uncommented.
* The use of this script is intended for creating a simple car database which will be used for Deep Learning. 

# TensorFlow Object Counting API
made to count any kind object on a pretrained source or trained models


### Object Tracking Mode (TensorFlow implementation):
<p align="center">
  <img src="https://user-images.githubusercontent.com/22610163/70389634-4682ea00-19d3-11ea-84a2-3996a43e98fe.gif" | width=430> <img src="https://user-images.githubusercontent.com/22610163/70389738-6bc42800-19d4-11ea-971f-f19cb5b90140.gif" | width=430>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/22610163/70389764-e9883380-19d4-11ea-8c54-80935811c3fa.gif" | width=680>
</p>

-Counting module was  built on top of [this approach](https://github.com/kcg2015/Vehicle-Detection-and-Tracking).

---

### Object Counting On Single Image (TensorFlow implementation):
<p align="center">
<img src="https://user-images.githubusercontent.com/22610163/47524870-7c830e80-d8a4-11e8-8fd1-741193615a04.png" | width=750></p>

---

### Object Counting based R-CNN ([Keras and TensorFlow implementation]

<p align="center">
<img src="https://user-images.githubusercontent.com/22610163/57969852-0569b080-7983-11e9-8051-07d6766ca0e4.png" | width=750></p>

### Object Segmentation & Counting based Mask R-CNN ([Keras and TensorFlow implementation]

<p align="center">
<img src="https://user-images.githubusercontent.com/22610163/57969871-1c100780-7983-11e9-9660-7b8571b01ff7.png" | width=750></p>

---




#### 1.1) For detecting, tracking and counting *the pedestrians* with disabled color prediction

*Usage of "Cumulative Counting Mode" for the "pedestrian counting" case:*

    fps = 30 # change it with your input video fps
    width = 626 # change it with your input video width
    height = 360 # change it with your input vide height
    is_color_recognition_enabled = 0 # set it to 1 for enabling the color prediction for the detected objects
    roi = 385 # roi line position
    deviation = 1 # the constant that represents the object counting area

    object_counting_api.cumulative_object_counting_x_axis(input_video, detection_graph, category_index, is_color_recognition_enabled, fps, width, height, roi, deviation) # counting all the objects
    
*Result of the "pedestrian counting" case:*


**Source code of "pedestrian counting case-study": [pedestrian_counting.py](https://github.com/ahmetozlu/tensorflow_object_counting_api/blob/master/pedestrian_counting.py)**


### 2.) Usage of "Real-Time Counting Mode"

#### 2.1) For detecting, tracking and counting the *targeted object/s* with disabled color prediction
 
 *Usage of "the targeted object is bicycle":*
 
    is_color_recognition_enabled = 0 # set it to 1 for enabling the color prediction for the detected objects
    targeted_objects = "bicycle"
    fps = 24 # change it with your input video fps
    width = 854 # change it with your input video width
    height = 480 # change it with your input vide height    

    object_counting_api.targeted_object_counting(input_video, detection_graph, category_index, is_color_recognition_enabled, targeted_objects, fps, width, height) # targeted objects counting
    
 

   
 

 
*Usage of "detecting, counting and tracking all the objects":*

    is_color_prediction_enabled = 0 # set it to 1 for enabling the color prediction for the detected objects
    fps = 24 # change it with your input video fps
    width = 854 # change it with your input video width
    height = 480 # change it with your input vide height    

    object_counting_api.object_counting(input_video, detection_graph, category_index, is_color_recognition_enabled, fps, width, height) # counting all the objects
 

---
*Usage of "detecting, counting and tracking **the multiple targeted objects**":*

    targeted_objects = "person, bicycle" # (for counting targeted objects) change it with your targeted objects
    fps = 25 # change it with your input video fps
    width = 1280 # change it with your input video width
    height = 720 # change it with your input video height
    is_color_recognition_enabled = 0

    object_counting_api.targeted_object_counting(input_video, detection_graph, category_index, is_color_recognition_enabled, targeted_objects, fps, width, height) # targeted objects counting
---
 
#### 2.2) For detecting, tracking and counting "all the objects with disabled color prediction"

*Usage of detecting, counting and tracking "all the objects with disabled color prediction":*
    
    is_color_prediction_enabled = 0 # set it to 1 for enabling the color prediction for the detected objects
    fps = 24 # change it with your input video fps
    width = 854 # change it with your input video width
    height = 480 # change it with your input vide height    

    object_counting_api.object_counting(input_video, detection_graph, category_index, is_color_recognition_enabled, fps, width, height) # counting all the objects


*Usage of detecting, counting and tracking "all the objects with enabled color prediction":*

    is_color_prediction_enabled = 1 # set it to 1 for enabling the color prediction for the detected objects
    fps = 24 # change it with your input video fps
    width = 854 # change it with your input video width
    height = 480 # change it with your input vide height    

    object_counting_api.object_counting(input_video, detection_graph, category_index, is_color_recognition_enabled, fps, width, height) # counting all the objects
    


- Detect just the targeted objects
- Detect all the objects
- Count just the targeted objects
- Count all the objects
- Predict color of the targeted objects
- Predict color of all the objects
- Predict speed of the targeted objects
- Predict speed of all the objects
- Print out the detection-counting result in a .csv file as an analysis report
- Save and store detected objects as new images under [detected_object folder](www)
- Select, download and use state of the art [models that are trained by Google Brain Team](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/detection_model_zoo.md)
- Use [your own trained models](https://www.tensorflow.org/guide/keras) or [a fine-tuned model](https://github.com/Hvass-Labs/TensorFlow-Tutorials/blob/master/10_Fine-Tuning.ipynb) to detect spesific object/s
- Save detection and counting results as a new video or show detection and counting results in real time
- Process images or videos depending on your requirements

Here are some cool architectural design features of TensorFlow Object Counting API:

- Lightweigth, runs in real-time
- Scalable and well-designed framework, easy usage
- Gets "Pythonic Approach" advantages
- It supports REST Architecture and RESTful Web Services






## Installation

### Dependencies

Tensorflow Object Counting API depends on the following libraries:

- TensorFlow Object Detection API
- Protobuf 3.0.0
- Python-tk
- Pillow 1.0
- lxml
- tf Slim (which is included in the "tensorflow/models/research/" checkout)
- Jupyter notebook
- Matplotlib
- Tensorflow
- Cython
- contextlib2
- cocoapi









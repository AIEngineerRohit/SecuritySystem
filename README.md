Security System with a Warning Signal based on Object Detection, Computer Vision.

To start -
1. Download the Repo
2. Create a python environment with 3.6 or if you already have an environment use it.
3. Install the requirements.txt file. Command # pip install -r requiremnts.txt
4. Run hand_detection.py and Enjoy.

<h1>Image classification and object detection</h1>

Image classification in computer vision takes an image and predicts the object in an image, while object detection not only predicts the object but also finds their location in terms of bounding boxes. For example, when we build a swimming pool classifier, we take an input image and predict whether it contains a pool, while an object detection model would also tell us the location of the pool.

<img src="https://developers.arcgis.com/assets/img/python-graphics/class_detection.png">

-Probablity that there is an object
-Height of the bounding box
-Width of the bounding box
-Horizontal coordinate of the center point of the bounding box
-Vertical coordinate of the center point of the bounding box.

This is just one of the conventions of specifying output. Different models and implementations may have different formats, but the idea is the same, which is to output the probablity and the location of the object.

<h1>Single-Shot Detector (SSD)</h1>

SSD has two components: a backbone model and SSD head. Backbone model usually is a pre-trained image classification network as a feature extractor. This is typically a network like ResNet trained on ImageNet from which the final fully connected classification layer has been removed. We are thus left with a deep neural network that is able to extract semantic meaning from the input image while preserving the spatial structure of the image albeit at a lower resolution. For ResNet34, the backbone results in a 256 7x7 feature maps for an input image. We will explain what feature and feature map are later on. The SSD head is just one or more convolutional layers added to this backbone and the outputs are interpreted as the bounding boxes and classes of objects in the spatial location of the final layers activations.

In the figure below, the first few layers (white boxes) are the backbone, the last few layers (blue boxes) represent the SSD head.

<img src = "https://cdn-images-1.medium.com/max/1000/1*GmJiirxTSuSVrh-r7gtJdA.png">



# Object Detection using OpenVINO
In this repo, we perform a step-by-step demonstration of object detection on images and video using OpenVINO™. We use a pre-trained network "mobilenet-ssd" and the model is running on the Intel® Distribution of OpenVINO™ toolkit Inference Engine. The inference will be executed using CPU(s).

# Inference engine API integration flow
1. Load the plugin
2. Read the model IR.The Intel® Distribution of OpenVINO™ toolkit includes the Model Optimizer used to convert and optimize trained models into the Intermediate Representation (IR) model files, and the Inference Engine that uses the IR model files to run inference on hardware devices.
3. Load the model into the plugin
6. Prepare the input
7. Run inference
8. Process the output

# Input preprocessing
1.  Resize image dimensions form image to model's input W x H:<br>
    image = cv2.resize(image, (w, h))
   
2. Change data layout from (H x W x C) to (C x H x W)<br>
    image = image.transpose((2, 0, 1))

3. Reshape to match input dimensions<br>
    image = image.reshape((n, c, h, w))

# Dependencies
 - OS
 - CV2
 - Time
 - Openvino.inference_engine 
 - Matplotlib

# Inference
 - Inference 1

![inference_1](https://user-images.githubusercontent.com/48753146/164156014-49f60159-8029-4485-8eb3-fc2241c39efe.png)

 - Inference 2

![inference_2](https://user-images.githubusercontent.com/48753146/164156122-9154a641-3bde-4b51-8632-c3f660810094.png)

 - Inference 3
 
https://user-images.githubusercontent.com/48753146/164156102-7cf470c7-b030-4f44-8779-4323892bcd2e.mp4

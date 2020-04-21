# Compliance Automation : ID card verification

# Problem Statement

> *"Build a Computer Vision solution that estimates visibility of ID card inside an image"*

![/Compliance%20Automation%20ID%20card%20verification/IMG_20200414_071347.jpg](/Compliance%20Automation%20ID%20card%20verification/IMG_20200414_071347.jpg)

Full visibility

![/Compliance%20Automation%20ID%20card%20verification/IMG_20200414_071352.jpg](/Compliance%20Automation%20ID%20card%20verification/IMG_20200414_071352.jpg)

Partial visibility

![/Compliance%20Automation%20ID%20card%20verification/IMG_20200414_071358.jpg](/Compliance%20Automation%20ID%20card%20verification/IMG_20200414_071358.jpg)

No visibility

---

# Potential Solutions

## Object Detection Approach

![/Compliance%20Automation%20ID%20card%20verification/7287BE96-9E59-4018-9345-2B12FA0A5EE8.jpeg](/Compliance%20Automation%20ID%20card%20verification/7287BE96-9E59-4018-9345-2B12FA0A5EE8.jpeg)

Bound box when ID card is detected

![/Compliance%20Automation%20ID%20card%20verification/IMG_20200414_071358%201.jpg](/Compliance%20Automation%20ID%20card%20verification/IMG_20200414_071358%201.jpg)

No bounding box signifies absence of ID card

- Single class object detection, ID card is the object class
- Model is expected to learn how to recognize ID card and locate them in an image.
- Challenges for implementation
    - Costly manual tagging of ID cards
    - Object detections are designed to detect objects even if the object is occluded, but in our problem statement we want to classify images with Id card with with occlusion and with occlusion separately.

## ID Card Boundary Detection

- How it works
- What are it's limitations
- Challenges for implementation
- Sample image with edge detection

## Image Classification

### CNN Classification

- We separate the dataset into three classes

![/Compliance%20Automation%20ID%20card%20verification/class_wise_pics_2.png](/Compliance%20Automation%20ID%20card%20verification/class_wise_pics_2.png)

![/Compliance%20Automation%20ID%20card%20verification/class_wise_pics_1.png](/Compliance%20Automation%20ID%20card%20verification/class_wise_pics_1.png)

![/Compliance%20Automation%20ID%20card%20verification/class_wise_pics_2%201.png](/Compliance%20Automation%20ID%20card%20verification/class_wise_pics_2%201.png)

- 2 stage approach
    - We divide the problem into two parts, the thought process behind such design is that multi-class classification problems need to have similar task across all the classes. In this cases we are not classifying types of ID card, that problem would be a typical multi-class problem
    - In our cases, classifying image as not visible class needs global features and classifying full visible and partially visible class needs local (geometrical) features. Hence it makes it is better to train to different models to learn these tasks and cascade them.

    ![/Compliance%20Automation%20ID%20card%20verification/IMG_0171.jpg](/Compliance%20Automation%20ID%20card%20verification/IMG_0171.jpg)

    - 

- GradCam output for ID classification

![/Compliance%20Automation%20ID%20card%20verification/download.png](/Compliance%20Automation%20ID%20card%20verification/download.png)

![/Compliance%20Automation%20ID%20card%20verification/gradcam1.png](/Compliance%20Automation%20ID%20card%20verification/gradcam1.png)

![/Compliance%20Automation%20ID%20card%20verification/gradcam3.png](/Compliance%20Automation%20ID%20card%20verification/gradcam3.png)

### HoG + SVM Classification

- How it works
- What are it's limitation
- Challenges
- Sample feature map of HoG

### Hybrid Approach

- CNN with edges and thresholding as input channels

---

# Conclusion

-

# FaceRecognitionApplication
An android application for real time face recognition, an application of Computer Vision.

The images of the people to be recognized are saved in the internal storage of the device. Using those images the people are classified.

## Tech Stack Used
- Android (Kotlin)
- ML Kit
- TensorflowLite (CV Algorithm Implemented)

## Working
- PREREQUISITE: Download the "Images" folder in your android device and store it in the internal storage

1. Scan the `images` folder present in the internal storage. Next, parse all the images present within `images` folder and store   
the names of sub directories within `images`. For every image, collect bounding box coordinates using MLKit.
  
2. Finally, we have a list of cropped `Bitmap` of the faces present in the images. Next, feed the cropped `Bitmap` to the FaceNet   
model and get the embeddings. Now, we create a `HashMap<String,FloatArray>` object where we store the names of   
the sub directories as keys and the embeddings as their corresponding values. 

This entire procedure is carried out only on the app's startup. The steps below will execute on each camera frame.

## Implementation

![image](https://user-images.githubusercontent.com/81557355/207809017-c0374895-3d05-48fe-bde0-ac10eafdd31c.png)

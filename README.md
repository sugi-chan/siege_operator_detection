# Rainbow Six Siege object detector

## Background
I play on an team with some friends in the tactical shooter Rainbow Six Siege, we make strategies, practice them, dissect our games, and track metrics. While not the most mechanically skilled, we make up for it with good preparation and can do fairly well against more skilled opponents because of it.

## Pipeline
While my current work is a long ways away from automating our stat collection, it is a good example of how to, fairly quickly, build a tailored end to end deep learning pipeline using an object detection + facial recognition models. The pipeline will have two main parts, first an object detection network to detect Rainbow Six Siege characters (operators) in the frame and then feed those outputs into a second model for classification. The end goal is to be able to run the pipeline over images and or video to detect which operator is in the frame.

-Build appropriate dataset for object detection (used screenshots and Labelimg python library to generate)
-Train object detection model
-Gather data for facial recognition
-facial_recognition library for facial recognition 
-Combine the two models to predict on images/video

## Notes
As of now the this repository is more or less a clone of https://github.com/experiencor/basic-yolo-keras

the only real difference is I have modified the utils.py file for prediction of operators faces using the face_recognition python library. 

~~the related datasets are around 3gb, so message me if you want a copy, but overall not hard to create~~

link to dataset [here](https://drive.google.com/open?id=16BoenC_F4PFCd6BCxk7H6jxjFXBbSAoi). These are the annotations and xmls which are suitable for this Keras implementation or standard tensorflow detection pipelines. Annotations I believe are called `person` still.


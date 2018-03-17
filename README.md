# face_detection_sliding_windows
A simple face detection algorithm with sliding window detector

This is a face detection method introduced in [Dalal and Triggs 2005](https://lear.inrialpes.fr/people/triggs/pubs/Dalal-cvpr05.pdf). The method has the following steps:
1. load 36 x 36 images with face as positive training data, and load random images with face as negative training data;
2. normalize them, and produce the histograms of oriented gradient for both images set;
3. build a linear classifier for the positive and negative HoG features using support vector machine, with low true negative rate;
4. for the test set, scale the image to smaller ones and run through the linear classifier. All the combined bounding box and confidence level builds the detector.

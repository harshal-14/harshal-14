---
title: "Bicycle Tracking Using Kalman Filter"
excerpt: "Occlusion handling for tracking using Linear Kalman Filter <br/><img src='/images/track_083.png'>"
collection: portfolio
---

This project focuses on utilizing the Kalman filter to track a bicycle's movement in a surveillance video captured from a stationary camera. The video contains several challenges, including linear movement, abrupt turns, occlusion by objects (e.g., light posts), and occasional issues with object detection. We aim to enhance the tracking accuracy and robustness by implementing the Kalman filter.

**Dataset**
Viraat Dataset: The project utilizes the Viraat dataset, a comprehensive collection of video footage from a surveillance camera.
About the dataset A Large-scale Benchmark Dataset for Event Recognition in Surveillance Video" by Sangmin Oh, Anthony Hoogs, Amitha Perera, Naresh Cuntoor, Chia-Chih Chen, Jong Taek Lee, Saurajit Mukherjee, J.K. Aggarwal, Hyungtae Lee, Larry Davis, Eran Swears, Xiaoyang Wang, Qiang Ji, Kishore Reddy, Mubarak Shah, Carl Vondrick, Hamed Pirsiavash, Deva Ramanan, Jenny Yuen, Antonio Torralba, Bi Song, Anesco Fong, Amit Roy-Chowdhury, and Mita Desai, in Proceedings of IEEE Comptuer Vision and Pattern Recognition (CVPR), 2011. Access Link.

**Object Detection**
YOLOv4: Object detection is performed using YOLOv4, a state-of-the-art real-time object detection system. YOLOv4 identifies the bicycle in the video frames, providing bounding box information.

**Challenges**
Dynamic Scenarios: The project addresses various challenges, including changes in object size (bounding box), temporary loss of object tracking, and object disappearance due to occlusion. These scenarios are common in real-world surveillance videos.

**Kalman Filter Implementation**
The Kalman filter plays a pivotal role in improving object tracking in challenging scenarios. Here's how it works:
Prediction: When the object is not detected in a frame, the Kalman filter predicts the object's position based on its previous state and a motion model. This prediction helps maintain tracking continuity even when the object is temporarily hidden.
Correction: When the object is detected, the Kalman filter corrects the predicted position using the measurement information (e.g., bounding box coordinates). This ensures accurate tracking and reduces the impact of noise in object detection.
Robustness: The Kalman filter's ability to predict and correct enables it to handle occlusion, object disappearance, and changes in object size effectively. It significantly improves the robustness and reliability of the tracking system.

Code can be found on my [Github](https://github.com/Lucifer2700/Kalman_filters)

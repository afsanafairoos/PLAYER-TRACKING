SC549 Neural Networks – Assignment 3
Player Tracking in Football Videos
CSC2451
1. Project Overview
This project implements an automated football player tracking system using deep learning. The system integrates:
•	Detection: Ultralytics YOLOv8n
•	Pose Estimation: YOLOv8n-Pose (17 COCO keypoints)
•	Tracking: ByteTrack multi-object tracking
All experiments were executed on CUDA (GPU acceleration).

2. Dataset and Processing
•	Total videos: 6
•	Total frames processed: 961
•	Videos contain multiple players under varying lighting and occlusion conditions.
Processing pipeline:
Video → Frame Extraction → Detection → Pose Estimation → Tracking → Metrics

3. Results Summary
Detection Performance
•	Total detections: 10,188
•	Average detections per frame: 10.6 players
•	Total frames analyzed: 961
The detector successfully identified multiple players per frame with stable performance across clips.

Pose Estimation Performance
•	Total poses detected: 4,682
•	Total keypoints detected: 51,412
•	Average keypoints per pose: 10.98 / 17
This indicates moderate pose quality. Some keypoints (especially lower body joints) were missed due to occlusion and motion blur.

Tracking Performance
•	Total unique players tracked: 494
ByteTrack maintained consistent tracking IDs across frames, demonstrating stable multi-object tracking performance.

4. Discussion
Strengths
•	Real-time GPU-based processing
•	Accurate multi-player detection
•	Stable tracking across frames
•	Large number of tracked player instances
Limitations
•	Average keypoints per pose (10.98/17) suggests partial occlusions
•	Distant players reduce pose accuracy
•	Model pretrained on COCO dataset, not football-specific

5. Conclusion
The system successfully performs end-to-end football player detection, pose estimation, and tracking using YOLOv8n and ByteTrack. Across 961 frames, the model detected over 10,000 player instances and tracked 494 unique players.
The results demonstrate that YOLOv8n provides an effective balance between speed and detection accuracy, making it suitable for real-time sports analytics applications.

 





	 

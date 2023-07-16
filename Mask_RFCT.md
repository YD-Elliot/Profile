# Mask RFCT: Recursive Fully Convolutional Tracker for Video Instance Segmentation
#### paper link: https://ieeexplore.ieee.org/abstract/document/10105756

**· Abstract:** Video instance segmentation has recently attracted a lot of attention due to the challenge of simultaneous segmentation and tracking in video clips. In this work, we propose a new video instance segmentation method, called Mask RFCT, which performs tracking via a precise feature vector matching by generating feature vectors from a recursive fully convolutional tracking branch. Our main contribution is the novel recursive fully convolutional tracker (RFCT) that generates corresponding feature vector for each instance within a bounding-box, which will be used for the following instance category assignment as tracking process. Model evaluation is conducted on YOUTUBE-VIS dataset. It shows that our Mask RFCT outperforms the baseline model, MaskTrack RCNN, obtaining an absolute gain of 2.8% for mean AP and 2.65% for mean AR. And we also conduct comparison experiments on different trackers we proposed and the baseline. We hope our work will provide a new method for architecture modification and instance tracking

<img width="901" alt="截屏2023-07-16 09 55 47" src="https://github.com/Elliot-YD/Profile/assets/67949876/9db0b7cd-5832-45b8-a8b6-c8a2db394a10">

**· RFCTracker:**
Based on the ConvTracker we proposed above, inspired by the recursive feedback connection in RFP of DetectoRS [3], we introduce a Recursive Connection to the ConvTracker, which transfers the output of the two conv-module back to the input, performing a second feature extraction by convolution operation, as shown in Figure 3. In figure 3, the red arrow denotes such recursive connection while the two gray modules in the gray dashed box denotes two convolutional modules mentioned above. We unroll the gray dashed box into colorful boxes in the lower part in the figure, where green dashed box and orange box denote two identical convolutional modules with the purple line represents this consistency. And the blue block denotes a global average pooling operation.
<img width="449" alt="截屏2023-07-16 09 56 03" src="https://github.com/Elliot-YD/Profile/assets/67949876/634e0bfe-3990-4b06-8ee3-dfa30262dcab">

**· Evaluation:**
Now the evaluation of algorithms for video instance segmentation task on YOUTUBE-VIS dataset is performed on the test server, while the metrics are defined in VIS to measure score, APs and ARs, leveraging segmentation for each frame and tracking across frames. Metrics are set as follows: the score is equal to the mAP value; AP, AP50 and AP75 for average precision measurement; AR1 and AR10 for average recall measurement.
<img width="799" alt="截屏2023-07-16 09 57 47" src="https://github.com/Elliot-YD/Profile/assets/67949876/546aa956-36d3-4f63-80b1-47901c2cdf8f">

**· Inferences:**
These results show that our Mask RFCT has the ability to detect, segment and track instances under various scenarios for video instance segmentation task with a relatively excellent performance.
<img width="930" alt="截屏2023-07-16 09 58 30" src="https://github.com/Elliot-YD/Profile/assets/67949876/328f2633-315d-4413-84db-b40bed0a5c65">

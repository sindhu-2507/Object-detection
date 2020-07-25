# Object-detection

The input will be a video.
Video is a sequence of frames. So we read frames per a particular instant of time and apply YOLO algorithm on them.
YOLO or You look only once is an alorithm which detects multiple objects in a frame in a single pass.
Each sliding window contain 2 or more anchors and for each anchor the probability that an object is present is estimated along with the bounding box
After that we filter boxes that is we take those boxes which has probability > threshold.
After that we apply Non-max suppresion.
Non-max suppression:- We eliminate the boxes with high IOU(Instersection over union) with the main bounding box(the bounding box with highest probability that there is an object
The result will be like this:
![image](https://user-images.githubusercontent.com/55240071/88453917-fafd4d80-ce88-11ea-9a8e-abe8e9c4e272.png)

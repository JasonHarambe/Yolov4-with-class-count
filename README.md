# Yolov4 with Class Count Displayed in Video
source: https://github.com/hunglc007/tensorflow-yolov4-tflite \
source: https://github.com/theAIGuysCode/yolov4-custom-functions

## Steps to run:
1. Clone the repo
#### Get pre-trained weight
2. wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights
3. %cd /content/Yolov4-with-class-count
##### convert pre-trained weight to Tensorflow format
4. !python save_model.py --weights /content/yolov4.weights --output ./checkpoints/yolov4-416 --input_size 416 --model yolov4 


## Detection:

### image
!python detect.py --weights ./checkpoints/yolov4-416 --size 416 --model yolov4 --image ./data/kite.jpg --output /content/result.jpg --count
### video
!python detectvideo.py --weights ./checkpoints/yolov4-416 --size 416 --model yolov4 --video /content/demo.mp4 --output /content/result.avi --count

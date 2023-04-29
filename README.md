# YOLOv7-Pose-on-Custom-Dataset:

## Keypoint detection on custom dataset. We have 1 class - Glass and it have 4 keypoints. In this this tutorial we will train our yolov7 model to detect these 4 custom keypoints

![image](https://user-images.githubusercontent.com/60029146/235298070-9b18bd05-64f6-4957-8c2b-f8e6faeacd13.png)

![image](https://user-images.githubusercontent.com/60029146/235298504-be7c9cdb-4368-4d13-b87d-c5d066bd08ab.png)





# Data Prepration:

Install Docker on your system if you haven't already. You can download it from the official website: https://www.docker.com/get-started

Now,Installing coco-annotator using docker:

    git clone https://github.com/jsbroks/coco-annotator.git 

    cd coco-annotator 

    docker-compose up

    http://localhost:5000/

    Learn how to annotate: https://www.youtube.com/watch?v=OMJRcjnMMok&t=1s  


### Next step is to convert json format annotations into YOLO format. 

    Refernce for conversion:  https://github.com/WongKinYiu/yolov7/issues/1103
    

### Now, Dataset is ready. Clone this github repo: 

        git clone https://github.com/AarohiSingla/YOLOv7-POSE-on-Custom-Dataset

        cd YOLOv7-POSE-on-Custom-Dataset

        pip install -r requirements.txt
        
        Place your dataset folder in this repo.
        
### Make all the changes which are mentioned in this video: https://youtu.be/OP-oiDsEVzc
        
For Training: 

      !python train.py --data data/custom_kpts.yaml --cfg cfg/yolov7-w6-pose_custom.yaml --hyp data/hyp.pose.yaml --device 0 --kpt-label --epochs 600
            
For Keypoint Detection: 

     !python detect.py --weights runs/train/exp3/weights/best.pt --kpt-label --source 1.jpg --conf 0.030 --iou 0.30



Reference: 

        https://github.com/WongKinYiu/yolov7/tree/pose

        https://github.com/ruiz-manuel/yolov7-pose-custom               

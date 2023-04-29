# YOLOv7-POSE-on-Custom-Dataset
Keypoint detection on custom dataset. We have 1 class - Glass and it have 4 keypoints. Ithis this tutorial we will train our yolov7 model to detect these 4 custom keypoints
![1](https://user-images.githubusercontent.com/60029146/235296038-85241cc6-c3e6-4666-bd47-02e5d107624b.jpg)

# Data Prepration:

Install Docker on your system if you haven't already. You can download it from the official website: https://www.docker.com/get-started

Now,Installing coco-annotator using docker:

    git clone https://github.com/jsbroks/coco-annotator.git 

    cd coco-annotator 

    docker-compose up

    http://localhost:5000/

    Learn how to annotate: https://www.youtube.com/watch?v=OMJRcjnMMok&t=1s  


Next step is to convert json format annotations into YOLO format. 

    Ref for conversion: https://github.com/WongKinYiu/yolov7/issues/1103

git clone 

![5](https://user-images.githubusercontent.com/60029146/235296118-d8b17771-da40-4285-b68e-a71a10938297.jpg)



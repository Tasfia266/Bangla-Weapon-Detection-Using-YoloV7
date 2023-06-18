# Bangla-Weapon-Detection-Using-YoloV7
This project focuses on detecting three types of local Bangladeshi weapons-1. Gun 2. Sharp Object and 3.Stick using the YoloV7 object detection algorithm. 
# Table of Contents:
# 1. Installation 
# 2. Usage  
# 3. Dataset 
# 4. Training 
# 5. Evaluation 
# 6. Result
# Installation: 
Clone this repository on Google Colab using-
# !git clone https://github.com/WongKinYiu/yolov7.git 
 Change the directory to the project folder: 
# %cd yolov7 
 Install the required YoloV7x weights: 
 # !wget https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7x.pt
 # 2. Usage
 Modify the configuration file (yolov7x-custom.yaml) with your desired settings and paths 
 # 3. Dataset 
 The dataset used for training the model is not included in this repository for further research purposes. You need to prepare your own dataset of Bangla weapon images with corresponding bounding box annotations in YOLO format. Make sure to have a balanced distribution of gun, sharp object, and stick images.
# 4. Training
Start the training process by: 
!python train.py --device 0 --batch-size 8 --epochs 2000 --img 224 224 --data data/custom_data.yaml --hyp data/hyp.scratch.custom.yaml --cfg cfg/training/yolov7x-custom.yaml --weights yolov7x.pt --name yolov7x-custom 
# 5. Evaluate
To evaluate the model's performance, use the following command: 
!python detect.py --weights runs/train/yolov7x-custom7/weights/last.pt --conf 0.5 --img-size 640 --source /content/drive/MyDrive/IMG20230513225131.jpg --no-trace 
# 6. Result
![img1015yolov4](https://github.com/Tasfia266/Bangla-Weapon-Detection-Using-YoloV7/assets/76652458/953e17da-bb3a-42ef-a840-0b6071c5e2d0)
![img100yolov4](https://github.com/Tasfia266/Bangla-Weapon-Detection-Using-YoloV7/assets/76652458/95d58413-0f4a-420a-a4a3-486cde3a8a54)
![img1015yolov4](https://github.com/Tasfia266/Bangla-Weapon-Detection-Using-YoloV7/assets/76652458/00e4abcc-6849-4508-a071-b07b8b5807ed)
![img1016yolov4](https://github.com/Tasfia266/Bangla-Weapon-Detection-Using-YoloV7/assets/76652458/85e744eb-224b-4b7f-96fa-3521a6922dcc)
![img255yolov4](https://github.com/Tasfia266/Bangla-Weapon-Detection-Using-YoloV7/assets/76652458/14b5f880-3db6-4ff0-886f-b26b7cb6b35d)


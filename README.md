# Custom-YOLO with Tensorflow 2.x
#BOHOL #Philippines #Scuba diving #Sea ecology #App #Flask
<p align="center"><img src="/detection/1.gif" width="600"\></p>

## My Custom weights
Download : https://drive.google.com/file/d/1-L5U2JCJG73HMfHJNIBsK9123N1yaHqf/view
```bash
# weights → tf
python save_model.py --weights ./data/yolov4-obj_best.weights --output ./checkpoints/bohol-416 --input_size 416 --model yolov4
```

## Dataset Statistics
created a 16 category saltwater fish dataset with roughly 200 images for each class.  
16개의 클래스, 클래스 별 약 200장의 이미지 라벨링.  
거북이 클래스 불균형..

<p align="center">
  <img src="/classes/0.jpg" width="80"/>
  <img src="/classes/1.jpg" width="80"/>
  <img src="/classes/2.jpg" width="80"/>
  <img src="/classes/3.jpg" width="80"/>
  <img src="/classes/4.jpg" width="80"/>
  <img src="/classes/5.jpg" width="80"/>
  <img src="/classes/6.jpg" width="80"/>
  <img src="/classes/7.jpg" width="80"/>
</p>

<p align="center">
  <img src="/classes/8.jpg" width="80"/>
  <img src="/classes/9.jpg" width="80"/>
  <img src="/classes/10.jpg" width="80"/>
  <img src="/classes/11.jpg" width="80"/>
  <img src="/classes/12.jpg" width="80"/>
  <img src="/classes/13.jpg" width="80"/>
  <img src="/classes/14.jpg" width="80"/>
  <img src="/classes/15.jpg" width="80"/>
</p>

Class_id  |                 Name                | Count |
--------- | :---------------------------------: | :----: |
0         |      Green_sea_turtle               | 630 |
1         |      Anthias                        | 287 |
2         |      Blonde_naso_tang               | 210 |
3         |      Blue_damsel                    | 208 |
4         |      Brown_tang                     | 248 |
5         |      Domino_damsel                  | 259 |
6         |      Foxface_rabbitfish             | 227 |
7         |      Jackfish                       | 254 |
8         |      Lionfish                       | 315 |
9         |      Regal_angelfish                | 320 |
10        |      Scissortail_sergeant_major_fish        | 221 |
11        |      Sergeant_major_fish            | 183 |
12        |      Snowflake_moray                | 342 |
13        |      Three_stripes_damsel           | 271 |
14        |      Tomato_clown                   | 193 |
15        |      Yellow_boxfish                 | 308 |
　        |      Total                   | 4476 |
  
## mAP (mean average precision)
<p align="left"><img src="/mAP/7.PNG" width="520"\></p>

## **Test images**
```bash
# image
python detect.py --weights ./checkpoints/bohol-416 --size 416 --model yolov4 --images ./data/images/img1.jpg
```
<p align="center">
  <img src="/detection/detection1.png" width="440"/>
  <img src="/detection/detection2.png" width="440"/>
</p>

<p align="center">
  <img src="/detection/detection3.png" width="440"/>
  <img src="/detection/detection4.png" width="440"/>
</p>

<p align="center">
  <img src="/detection/detection5.png" width="440"/>
  <img src="/detection/detection6.png" width="440"/>
</p>

<p align="center">
  <img src="/detection/detection7.png" width="440"/>
  <img src="/detection/detection8.png" width="440"/>
</p>

## **Test videos**
```bash
# video
python detect_video.py --weights ./checkpoints/bohol-416 --size 416 --model yolov4 --video ./data/video/vid1.mp4 --output ./detections/best2/vid1.avi
```
<p align="center">
  <img src="/detection/2.gif" width="440"/>
  <img src="/detection/3.gif" width="440"/>
</p>

<p align="center">
  <img src="/detection/4.gif" width="440"/>
  <img src="/detection/6.gif" width="440"/>
</p>

<p align="center">
  <img src="/detection/5.gif" width="440"/>
  <img src="/detection/7.gif" width="440"/>
</p>

<p align="center">
  <img src="/detection/8.gif" width="440"/>
  <img src="/detection/9.gif" width="440"/>
</p>

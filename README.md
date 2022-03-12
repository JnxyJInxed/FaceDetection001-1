# FaceDetection001-1
Test Code to make sure the environtment is suitable to run YOLO without CPU

## SETUP
<!--   Change current_path on the code to <working directory> 

  ![image](https://user-images.githubusercontent.com/64402575/157387253-16204722-f290-47df-a919-69322dbfdfb0.png)

OR -->
  
Remake darknet using:
  
  ### 1. Clone darknet
    !git clone https://github.com/AlexeyAB/darknet

    %cd darknet
  ### 2. Change makefile to have OPENCV and LIBSO enabled for NON GPU
    !sed -i 's/OPENCV=0/OPENCV=1/' Makefile
    !sed -i 's/LIBSO=0/LIBSO=1/' Makefile

  ### 3. Make darknet
    !make

  ### 4. Get model Weight
   download https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights and copy 'yolov4.weights' to '/darknet/'
  
  ### 5. Install requirement.txt
      pip install Requirement.txt
   
  ### 6. Run the test0x.py
   copy the test0x.py to /darknet/ and run :D
  
## NOTE
### Darknet Installation Parameter
to check the darknet installation, put this command on Powersheel window on darknet instllation directory
>     darknet.exe detector test cfg/coco.data cfg/yolov4.cfg yolov4.weights -thresh 0.25
and enter some image test path for the input, example
>      data/person.jpg
if installation succesfull, the detection of test image will return detection result, example:
> [('dog',
  '91.28',
  (107.40998840332031,
   368.1647033691406,
   112.43595886230469,
   97.14092254638672)),
 ('person',
  '92.95',
  (186.889404296875, 286.2784118652344, 69.9059066772461, 336.72027587890625)),
 ('horse',
  '93.02',
  (403.2359619140625,
   293.5936279296875,
   157.2364044189453,
   250.5433807373047))]time: 20.5 ms (started: 2022-03-09 06:06:51 +00:00)

### Basic Architecture Parameter
Once the program is running, open http://127.0.0.1:800.
Check wether the server return empty array (no detection), detection result and succesfull message, etc

## LINK TO COLLAB DEMO (online NO GPU)
https://colab.research.google.com/drive/1ccW44_NvrsnADvlRGVCa7cBdCnsc7Lm8?usp=sharing

## SNAPSHOOT OF Darknet on local CPU:
### Detection result
![Capture](https://user-images.githubusercontent.com/64402575/158035414-013f64f2-f8d5-4a4e-8cec-1c6cb72e8e6f.PNG)
![Capture2](https://user-images.githubusercontent.com/64402575/158035413-07ffc019-98fe-43f6-82c0-03020893f924.PNG)
![Capture3](https://user-images.githubusercontent.com/64402575/158035410-c6bb9005-f022-43e3-864b-cacd5f54e36a.PNG)

### Program Succesfull 'run' result
![image](https://user-images.githubusercontent.com/64402575/158035383-4d017db3-7ea3-4ba3-8645-0d5771250de5.png)
![Capture5](https://user-images.githubusercontent.com/64402575/158035400-5ef3553e-3d75-4230-ae5e-27b3393d9690.PNG)

### Program FAILED 'run' result
![Capture4](https://user-images.githubusercontent.com/64402575/158035406-1b34bfd5-d897-4d32-a6b9-865dec691311.PNG)
#### notes by Nabilala

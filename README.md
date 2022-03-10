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
    !wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id=1V3vsIaxAlGWvK4Aar9bAiK5U0QFttKwq' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id=1V3vsIaxAlGWvK4Aar9bAiK5U0QFttKwq" -O yolov4-csp.weights && rm -rf /tmp/cookies.txt
  
## NOTE
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
   
## LINK TO COLLAB DEMO
https://colab.research.google.com/drive/1ccW44_NvrsnADvlRGVCa7cBdCnsc7Lm8?usp=sharing

#### notes by Nabilala

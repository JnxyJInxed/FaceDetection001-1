# FaceDetection001-1
Test Code to make sure the environtment is suitable to run YOLO without CPU

## SETUP
  Change current_path on the code to <working directory> 

  ![image](https://user-images.githubusercontent.com/64402575/157387253-16204722-f290-47df-a919-69322dbfdfb0.png)

OR
  
Remake darknet using:
  
  ### clone darknet repo
  !git clone https://github.com/AlexeyAB/darknet install_directory

  %cd install_directory/darknet
  ### change makefile to have OPENCV and LIBSO enabled for NON GPU
  !sed -i 's/OPENCV=0/OPENCV=1/' Makefile
  
  !sed -i 's/LIBSO=0/LIBSO=1/' Makefile

  ### make darknet
  !make

  
## Note
  

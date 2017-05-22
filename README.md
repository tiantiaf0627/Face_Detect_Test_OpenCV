# Face_Detect_Test_OpenCV
Script to test OpenCV API for face detection using Camera(Raspberry PI 3)

To connect PI camera to Raspberry PI Ubuntu Mate follow the steps below:

A. Prepare

1. Install Ubuntu-Mate
2. Then open a terminal on Ubuntu-Mate
3. sudo apt-get update
4. sudo apt-get upgrade
5. sudo apt-get install build-essential cmake pkg-config
6. sudo apt-get install build-essential
7. sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
8. sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev

B. Clone Package from Git

1. cd /opt
2. git clone https://github.com/Itseez/opencv.git
3. git clone https://github.com/Itseez/opencv_contrib.git
4. cd opencv
5. git checkout 3.1.0
6. cd /opt/opencv_contrib
7. git checkout 3.1.0
8. cd /opt/opencv

C. Pre-Build

1. cd /opt/opencv
2. mkdir release
3. cd release
4. cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D OPENCV_EXTRA_MODULES_PATH=/opt/opencv_contrib/modules /opt/opencv/

D. Make and Install(It will take like 1 hour and half, take a good break while making process)

1. sudo make
2. sudo make install
3. Check the version by type: pkg-config --modversion opencv

----------------------------------------------------

Run the code:

1. Paste the code into the Desktop of your Ubuntu system
2. Open terminal
3. cd Desktop
4. python face_detect.py

You would be able to see the camera screen and detected output on screen streaming and terminal
Frame Rate is about 10-12 frames per second.


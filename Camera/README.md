# Camera Calibration

Camera calibration: A practical guide (theory with code). Compilation of theory from OpenCV, Andrew zisserman book and few online sources. I have tried my best to simplify things and explained in very practical manner.
theory can be found in the folder Documents :)
dependencies: OpenCV, numpy, python 2 (Becuase I use ROS ;))

# How to use the code
1. Add your images to the Data folder (remember to remove the image which added to test the code)
2. edit the checker board pattern accordingly.
3. Code is explained here : https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_calib3d/py_calibration/py_calibration.html

# Examples
Below examples shows the detected checkerboard corners  
![Example](https://user-images.githubusercontent.com/50611671/170954115-0d5f20df-e53d-4d50-a4e8-b1153e5ab502.PNG)
![Example_1](https://user-images.githubusercontent.com/50611671/170954125-75c5efbe-eaa7-40f0-9f8e-87e71da25fbc.PNG)

# Outputs
camera matrix:
 [745.12738779   0.         694.35211524]
 [  0.         745.22677241 383.93278083]
 [  0.           0.           1.        ]
 
 distorsion coefficients: [-0.0287999   0.029206   -0.00073055 -0.00219651 -0.01077339]
 
 # Comparison: OpenCV, Matlab, factory defualt for azure (Robot-guided in my case)
 Several images at different depth in steps of approx 200mm starting  approx 400mm from the
camera were used for camera calibration. The estimated camera intrinsic parameters
using OpenCV, Matlab along with values in the robot-guided data set is provided in
tab. 4.1. Image size 1280×720.

![CV_Matlab](https://user-images.githubusercontent.com/50611671/170957565-375d28f7-3b73-4ad4-82e3-707b0f92f813.PNG)

There are slight differences in camera parameters estimated by OpenCV and Matlab for same set of images. Interesting!



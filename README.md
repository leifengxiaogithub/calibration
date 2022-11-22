#Coordinate data pre acquisition
The first section（Line1-58） of this code file solves the coordinate value of the intersection of the ray of each pixel point with the plane where the calibration plate is located, according to the idea of pixel-by-pixel calibration, which is saved in the camera_coordinate variable;
Line6-17：Load camera internal parameters and RT matrix of each calibration board;
Line19: Load the world coordinates of corners;
Line21-25: Load the phase map corresponding to each calibration board；
Line26-36: Estimating the equation of each calibration plate plane in camera coordinate system by least square method;
Line37-49: Solve the equation of ray corresponding to each pixel;
Line50-58: Coordinate of intersection point obtained by solving equation of joint ray and plane;

#Pixel-wise calibration process
Line59-80: This part uses the least square method to calibrate the parameters to be obtained, and finally stores them in 'Calibration_Table.mat'.

#Pixel-wise calibration error analysis
Line82-100: Evaluate the calibration errors of different pixels and store them in the relevant variables；

#Error visualization
Line102-115: Draw the frequency distribution histogram of errors, and grade the pixels with different errors. Finally, save the grades in 'Label_Table.mat'.

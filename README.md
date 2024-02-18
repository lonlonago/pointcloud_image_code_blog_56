#  Function overview 

##  1. Implement the algorithm 

   There is a direct implementation of the fitting cylinder algorithm in the Matlab point cloud toolbox. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596238
  ```  
 The function uses M-estimator sample consistency (MSAC) algorithm to find the cylinder from the point cloud. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596238
  ```  
 Use the 1 × 3 reference direction input vector to specify additional direction constraints for the cylinder to be fitted. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596238
  ```  
 Distinguish between inner and outer points of the output fit. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596238
  ```  
 In addition, returns the average error of the distance from the Inlier point to the model. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596238
  ```  
 Use additional options specified by one or more names and values for parameters. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574596238
  ```  
#  III. Display of results 

 ![avatar]( 20210618203519792.png) 

#  IV. Reference link 

 Matlab point cloud toolbox - Fit cylinder to 3-D point cloud 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Implement the algorithm 

   In the Matlab point cloud toolbox, there is a direct implementation of the RANSAC fitting plane algorithm, without having to write fancy implementation code yourself (it seems like you are so powerful). 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574548292
  ```  
 Fit a point cloud with the maximum allowable distance from an independent point to the plane. The function returns a geometric model describing the plane. The function uses the M-Estimator Sample Consistency (MSAC) algorithm to find the plane. The MSAC algorithm is a variant of the Random Sample Consistency (RANSAC) algorithm. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574548292
  ```  
 The direction constraint is added when fitting the plane, and the direction vector is an additional direction constraint specified by the 1 × 3 vector input. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574548292
  ```  
 Sets the angle threshold between the specified constraint direction 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574548292
  ```  
 Output inner and outer points 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574548292
  ```  
 Returns the average error of the distance from the Inlier point to the model. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574548292
  ```  
#  III. Display of results 

 ![avatar]( 2021061418353063.png) 

#  IV. Reference link 

 [1] matlab点云工具箱——Fit plane to 3-D point cloud [2] RANSAC介绍（Matlab版直线拟合+平面拟合） 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

   See: matlab RANSAC fitting plane 

#  Code implementation 

 RansacPlaneFit.m 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574598484
  ```  
 main.m 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574598484
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574598484
  ```  
 ![avatar]( ceafc75572ec4484a9000f50f061baed.png) 

#  IV. Test data 

 Link: https://pan.baidu.com/s/1cw1pkWh1ov6s9RI2KZtRyA Extraction code: 34b3 



--------------------------------------------------------------------------------

#  I. Overview of algorithms 

   RANSAC is a robust fitting algorithm that can be used to estimate model parameters in datasets. For fitting quadratic polynomial curves, the steps of the RANSAC algorithm are as follows: 

 1. Randomly select a small number of data points, assuming they are data points that fit the quadratic polynomial curve. 2. Fit a quadratic polynomial curve from these data points. 3. Calculate the distance from all points in the dataset to this curve. If the distance is less than the given threshold, these points are considered to be points that fit the quadratic polynomial curve. 4. If the number of eligible points is greater than a certain threshold, then refit the quadratic polynomial curve and update the set of eligible points; otherwise, repeat step 1. Repeat steps 1-4 multiple times and select the quadratic polynomial curve that corresponds to the largest number of eligible points as the final fitting result. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574577035
  ```  
#  III. Display of results 

 ![avatar]( 8abbf882fed34b78901f0c5ca3cb9395.png) 

#  IV. Relevant links 

 [1] matlab 点云最小二乘拟合多项式曲线 



--------------------------------------------------------------------------------

#  Function overview 

 Algorithm principle: matlab least squares fitting space sphere 

##  1. Algorithm overview 

   Fitting a sphere from a 3D point cloud 

##  2. Main functions 

 Overloaded function 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595763
  ```  
   Given a distance threshold, the function returns a geometric model describing the sphere. The function uses the M-Estimator Sample Consistency (MSAC) algorithm to find the sphere. The MSAC algorithm is a variant of the Random Sampling Consistency (RANSAC) algorithm. Overloaded Function 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595763
  ```  
   Returns the inner and outer point indices, overloading function 3: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595763
  ```  
   Using any of the previous syntax, returns the average error of the distance from the Inlier point to the model. Overload function 4: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595763
  ```  
   Use the name-value, corresponding to the other options specified by the parameter. 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595763
  ```  
#  III. Display of results 

 ![avatar]( adc4f0d008f048448b5a8ff078e86c23.png) 

 1. Primitive point cloud  

 2. Fitting results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595763
  ```  
 ![avatar]( 9cd3a0fa5a164bab95f90ce7766dc148.png) 

 3. Inner point  

 ![avatar]( a4670fd812714d6a8311e69ba153e66c.png) 

 4. Outer point 5. Fitting result  

#  IV. Parameter analysis 

##  input parameter 

##  Name-value corresponding parameter 

##  output parameter 

#  V. Reference links 

>  Matlab point cloud toolbox - pcfitsphere 



--------------------------------------------------------------------------------

#  I. Overview of algorithms 

##  1. Implementation process 

 1. First, a small number of points are randomly selected from the point cloud, which will be used to fit the line. 

 2. Compute a model of a straight line passing through these points and use that model to calculate the distance from all points in the point cloud to that line. 

 3. Set a distance threshold and define all points in the point cloud that are less than the distance from the straight line as interior points. 

 4. If the number of interior points is greater than a certain threshold (e.g. 50%), use all interior points to refit the straight line model; otherwise, return to step 1. 

 5. Repeat steps 2 through 4 until the maximum number of iterations is reached or the stop condition is satisfied. 

 6. The resulting straight line model is what is required. 

##  2. Parameter analysis 

>  A, b, c represent the coordinates of a point on the line, d, e, f represent the direction vector of the line. 

#  Code implementation 

 RansacLineFit.m 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595289
  ```  
 main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595289
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595289
  ```  
 ![avatar]( 52e4e7e0b68f43b8918887b8f5bac3d0.png) 

#  IV. Relevant links 

 [1] matlab RANSAC拟合直线 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574547421
  ```  
   Model fitting to noisy data using the Random Sample Consistency (RANSAC) algorithm M-Estimator Sample Consistency (MSAC) algorithm. Specify the function FitFcn to fit the model, and the function disFcn to calculate the distance from the model to the data. The RANSAC function uses sampleSize to get a random sample from your data and the fit function to maximize the number of interior points. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574547421
  ```  
 In addition, specify one or more name and value pair parameters. 

 input parameter 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574547421
  ```  
 output parameter 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574547421
  ```  
#  III. Display of results 

 ![avatar]( 2e6e1e2bfcf545c0bd5546e99dba81a9.png) 

#  IV. Reference link 

 [1] matlab 点云工具箱——ransac [2] 最小二乘拟合直线 



--------------------------------------------------------------------------------

#  Function overview 

   Read 3D surface mesh data from STL or PLY files 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524823
  ```  
   Reads surface mesh data from an STL or PLY file with the specified filename and returns it as a surface mesh object. 

##  2. Input and output parameters 

##  3. Insufficient 

 These properties cannot be read from an STL file: 

#  Second, read in the PLY file 

##  1. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524823
  ```  
##  2. Results display 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524823
  ```  
 ![avatar]( db0b8125e90c4af28e255bd42fec6260.png) 

#  Third, read in the STL file 

##  1. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524823
  ```  
##  2. Results display 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524823
  ```  
 ![avatar]( ce52d3790bde40f5ba0859df045d5604.png) 

#  Fourth, a warning!!! 

   Copy and paste the code to run directly, and do not read other content of the blog. If you report an error, you will directly open "Why did I report an error, what kind of garbage code is this"??? readSurfaceMesh is a new function in matlab2022b and above, so why do some bosses make mistakes?? Why ask?????  



--------------------------------------------------------------------------------

#  I. Overview 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574579943
  ```  
    Load the data into array A. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574579943
  ```  
    Load data from the system clipboard rather than from a file. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574579943
  ```  
    Interpret delimiterIn as a column separator in ASCII file filename or clipboard data. You can use delimiterIn with any of the input parameters in the above syntax. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574579943
  ```  
    Load the data from the ASCII file filename or clipboard and read the numeric data starting from the headerlinesIn + 1 line. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574579943
  ```  
    Using any of the input parameters from the previous syntax, the delimiter in the input ASCII file detected is additionally returned in delimiterOut, as well as the number of header lines detected in headerlinesOut. 

##  2. Input parameters 

##  3. Output parameters 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574579943
  ```  
#  III. Display of results 

 ![avatar]( 77bf6324e1224cc5957b43e1df519cd8.png) 

#  IV. Reference link 

 Load data from a file 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

   The function determines the visible point in the point cloud from the specified viewpoint using the following steps. 1. Associates the point cloud with the coordinate system centered at the viewpoint. 2. Performs inversion using a spherical projection. 

 3. Calculate the convex hull of the transformed point cloud and viewpoint, and the point inside the convex hull is the visible point. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095745899
  ```  
   Removes hidden points from the point cloud ptCloudIn. This function removes hidden points when the point cloud is viewed from the specified viewpoint. Determining the visibility of a point is useful for shadow casting, reconstruction, and camera placement. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095745899
  ```  
 Specifies the radius scale of the spherical projection. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095745899
  ```  
 Returns the index of the point visible from the specified viewpoint, using any combination of input parameters from the previous syntax. 

 input parameter 

 output parameter 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095745899
  ```  
#  III. Display of results 

 ![avatar]( 5c47ce1b59d0431ca59613e32c465df4.png) 

#  IV. Reference link 

 Matlab point cloud toolbox - removeHiddenPoints removeHiddenPoints is a new function in matlab2023a and above.  



--------------------------------------------------------------------------------

#  First, the main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574549013
  ```  
 Removes a point with an inf or nan coordinate value from the point cloud and returns the index of the valid point. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574549013
  ```  
#  III. Display of results 

 ![avatar]( 20210605162621697.png) 

#  IV. Reference link 

 Matlab Point Cloud Toolbox - Remove invalid points from point cloud 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

   1. For each point on the scan line, the function computes these three features. 

 2. If a point satisfies all the characteristics of the calculation, then it is a curb point. 

 3. If the road angle is specified as input, the function will use RANSAC polynomial fitting to further fine-tune the feature edge points and return candidate edge points. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574543364
  ```  
   Split an index of feature curb points from an ordered point cloud containing points on a road. Curbs usually define the boundary of a road and form the edge of a sidewalk. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574543364
  ```  
 Specifies the road angles. The function uses these road angles to further process characteristic curb points and returns candidate curb points. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574543364
  ```  
 Specifies the edge point to split from the previous point cloud frame. This function uses the previous kerb points to improve robustness when the input point cloud is occluded. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574543364
  ```  
 Returns the segmented curb point in the road point cloud as a pointCloud object using any combination of input parameters from the previous syntax. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574543364
  ```  
 In addition to using any parameter combination from the previous syntax, one or more name-value parameters are used to specify options. For example, HeightLimits = [0.1 0.3] specifies the minimum and maximum heights of road curbs of 0.1 and 0.3 meters, respectively. 

 input parameter 

>  Road angles can be calculated by using the detectRoadAngles function, or they can be entered into the function manually. When road angles are specified, the function processes characteristic curb points using a RANSAC polynomial fit to return candidate curb points. 

 Name-value corresponding parameter 

>   

 output parameter 

##  3. References 

>  [1] YIHUAN ZHANG, JUN WANG, XIAONIAN WANG, et al. Road-Segmentation-Based Curb Detection Method for Self-Driving via a 3D-LiDAR Sensor[J]. IEEE transactions on intelligent transportation systems,2018,19(12):3981-3991. DOI:10.1109/TITS.2018.2789462. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574543364
  ```  
#  III. Display of results 

 ![avatar]( 72ce05c6b1944989be5ac5ba5ebf0a05.png) 

#  IV. Reference link 

 Matlab point cloud toolbox - segmentCurbPoints 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

   Write the 3D point cloud to a PLY or PCD file. 

##  2. Main functions 

 Overloaded function 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574539024
  ```  
   Writes the point cloud object ptCloud to the PLY or PCD file specified by the input filename. Overload function 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574539024
  ```  
   Writes the pointCloud object ptCloud to a PLY file in the specified format. 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574539024
  ```  
#  III. Parameter analysis 

##  input parameter 

#  Point cloud storage objects 

   pointCloud objects create point cloud data from a set of points in a 3D coordinate system. These points typically represent the and geometric coordinates of a sample surface or environment. Each point can also be represented with additional information, such as RGB color. Point cloud data is stored as an object with properties listed in properties. Use object functions to retrieve, select, and delete the desired points from the point cloud data. 

##  1. Main function 

 Overloaded function 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574539024
  ```  
   Returns a point cloud object with coordinates specified by xyzPoints. Overload function 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574539024
  ```  
   Create a pointCloud object whose properties are specified as one or more name, value, and parameter pairs. For example, pointCloud (xyzPoints, 'Color', [0 0 0]) sets the color property of point xyzPoints to [0 0 0]. Enclose each property name in quotes. Any property that is not specified has a default value. 

##  2. Input parameters 

##  3. Output parameters 

##  4、properties 

##  5. Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574539024
  ```  
##  6. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574539024
  ```  
 ![avatar]( 1efe771517934a11870c096945dd4db4.png) 

#  V. Reference links 

 [1] matlab点云工具箱——pcwrite [2] matlab点云工具箱——pointCloud 



--------------------------------------------------------------------------------

#  First, the main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574535731
  ```  
    Write the triangulation TR to the binary STL file filename. The triangulation can be a triangulation object or a 2D delaunayTriangulation object. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574535731
  ```  
    Also specifies the file format to write to the file. fileformat can be'binary ' (default) or'text'. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574535731
  ```  
    Use one or more of the above syntax's Name, Value pair parameters to specify additional options for writing to STL files. For example, stlwrite (TR, 'stlbinary', 'Attribute', attributes) also writes a uint16 attribute vector for each triangle in the TR. 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574535731
  ```  
#  III. Parameter analysis 

##  1. Input parameters 

##  2. Name-value parameters 

 示例： stlwrite(TR,'stltext','SolidIndex',solidIDs) 

    Specify an optional, comma-separated Name, Value pair group parameter. Name is the parameter name and Value is the corresponding value. Name must be enclosed in single quotes (’ ') . You can specify name-value pair group parameters in any order, such as Name1, Value1, Name2, Value2. 

#  IV. Remarks 

    This function was introduced in Matlab R2018b. 



--------------------------------------------------------------------------------

#  First, the SMRF algorithm 

##  1. Algorithm overview 

    The Simple Morphological Filtering (SMRF) algorithm [1] divides point cloud data into ground and non-ground points. The algorithm is divided into three stages: 

 Minimum Surface Creation 

 Surface Map Segmentation 

 Point Cloud Segmentation 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574586131
  ```  
    Split the input point cloud, ptCloud, into ground and non-ground points, and return the ground point index groundPtsIdx. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574586131
  ```  
    Specifies the size of the grid element. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574586131
  ```  
    Returns ground and non-ground points. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574586131
  ```  
    Use one or more name-value parameters to specify options. For example, 'ElevationThreshold', 0.4 sets the height threshold to identify non-ground points to 0.4. 

##  3. References 

>  [1] Pingel, Thomas J., Keith C. Clarke, and William A. McBride. “An Improved Simple Morphological Filter for the Terrain Classification of Airborne LIDAR Data.” ISPRS Journal of Photogrammetry and Remote Sensing 77 (March 2013): 21–30. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574586131
  ```  
#  III. Parameter analysis 

##  input parameter 

##  Name value corresponding parameter 

>  The default value is: 18. The default value is for aerial LiDAR data. For better performance on ground data, you need to set MaxWindowRadius to a smaller value, such as 8. 

>  Default values apply to aerial LiDAR data. To get the best results on ground data, set ElevationThreshold to a smaller value, such as 0.1. 

##  output parameter 

#  IV. Display of results 

##  1. Primitive point cloud 

 ![avatar]( 7a04746079f24aa9aac6d834f2af66ab.png) 

##  2. Segmentation results 

 ![avatar]( c1004a69c02e45be93ae31fe60412707.png) 

#  V. Reference links 

 Matlab point cloud toolbox - segmentGroundSMRF 



--------------------------------------------------------------------------------

#  First, grammar 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
#  II. Description 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
    Returns the moving average of the elements of the vector using a fixed window length determined in a heuristic manner. Slides the window down the length of the vector to calculate the average of the elements in each window. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
   Perform operations along dimension dim of A. For example, if A is a matrix, smoothdata (A, 2) smooths every row of data in A. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
   Specify a smoothing method for any of the above syntaxes. For example, B = smoothdata (A, 'sgolay') smooths the data in A using a Savitzky-golay filter. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
   Specifies the window length used by the smoothing method. For example, smoothdata (A, 'movmedian', 5) smooths the data in A by finding the median of the five-element sliding window. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
    Specifies how to handle NaN values when using any of the above syntaxes. 'Omitnan' will ignore NaN values, and'includenan 'will include NaN values when computed in each window. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
    Use one or more name-value pairs to specify additional parameters for smoothing. For example, if t is a time value vector, smoothdata (A, 'SamplePoints', t) smooths the data in A relative to the time in t. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
   Returns the moving window length. 

#  III. Examples 

##  1. Use a moving average to smooth the data 

    Create a vector with noisy data and smooth the data using a moving average. Plot the original data source and the smoothed data. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
 ![avatar]( c74a30492996479f8dceecacae3119d5.png) 

##  2. Matrix with noisy data 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
 ![avatar]( 2d61677d9b4242d5b760a510ac2facdb.png) 

##  3. Gaussian filter 

 Smoothes noisy data vectors using a Gaussian weighted moving average filter. Displays the window length used by the filter. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
 ![avatar]( 53edee15c72449dd918702e9fbec2786.png) 

##  4. Vectors containing NaN 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574513332
  ```  
 ![avatar]( 62f17e9f75374addb8751f85606a29a7.png) 

#  IV. Input parameters 

 ![avatar]( 45c2c836c97348fc876390976144d45c.png) 

#  Name-value pair group parameters 

 ![avatar]( 42d29e6684c9488ca1ef958a63b7baf5.png) 

#  VI. Output parameters 

 ![avatar]( 863773eea2964a3483e48d828f981243.png) 

#  VII. Reference link 

 [1] Smooth noisy data [2] 数据平滑方法的原理和应用 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

   Segmentation of ground points from organized lidar data 

##  2. Main functions 

 Overloaded function 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574555090
  ```  
   Split organized 3D LiDAR data into ground and non-ground sections. The LiDAR sensor must be mounted horizontally so that all ground points closest to the sensor are observed in the LiDAR scan. Overload Function 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574555090
  ```  
   Set properties using one or more name-value pairs. Enclose each property name in quotation marks 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574555090
  ```  
#  III. Display of results 

 ![avatar]( a542bb829d8c4e1b9efe30c47b54834d.png) 

#  IV. Parameter analysis 

##  input parameter 

##  Name-value corresponding parameter 

##  output parameter 

#  V. Reference links 

>  Matlab Point Cloud Toolbox - segmentGroundFromLidarData 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

   The spherical rotation method triangulates a set of points by rolling a sphere of radius over a cloud of points. The algorithm consists of the following steps: 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589340
  ```  
   Use the ball-pivot method to build a curved mesh from point cloud data. The function also returns the radius used in the reconstruction. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589340
  ```  
 Also specify the radius of the ball pivot reconstruction method. 

##  3. Input and output parameters 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589340
  ```  
#  III. Display of results 

##  1. Primitive point cloud 

 ![avatar]( 439153fccedd4413b2849bb38ea84dc6.png) 

##  2. Reconstruction results 

 ![avatar]( 11b576f47bd04d4bb384982ad2235843.png) 

#  Fourth, a warning!!! 

   Copy and paste the code to run directly, and do not read other content of the blog. If you report an error, you will directly open "Why did I report an error, what kind of garbage code is this"??? pc2surfacemesh is a new function in matlab2022b and above, so why do some bosses make mistakes?? Why ask?????  



--------------------------------------------------------------------------------

#  I. SVD 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595460
  ```  
    Returns the singular values of a matrix, in descending order. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595460
  ```  
    Perform a singular value decomposition of the matrix, therefore. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595460
  ```  
    Generate a reduced decomposition for the matrix. 

    Reduced decomposition removes additional zero-valued rows or columns from the singular-valued diagonal matrix S, as well as columns in U or V that are multiplied by those zero-valued columns in the expression A = USV '. Removing these zero-valued columns and columns reduces execution time and storage requirements without affecting the accuracy of the decomposition. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595460
  ```  
    Generate another reduced decomposition for the m × n matrix A: 

##  2. Input and output parameters 

    For m > n m × n matrix A, the reduced factorizations svd (A, 'econ') and svd (A, 0) compute only the first n columns of U. In this case, the columns of U are orthogonal, and U is an m × n matrix that satisfies. For complete factorizations, svd (A) returns U in the form of a satisfied m × m unitary matrix. The range of columns A with corresponding non-zero singular values in U forms a set of standard orthogonal basis vectors. Different computers and versions ® MATLAB can generate different singular vectors that remain numerically accurate. The corresponding columns in U and V can be flipped over, as this does not affect the value of the expression A = USV '. 

 - For an m × n matrix A, the reduced decomposition svd (A, 'econ') will return S as a square of order min ([m, n]). - For a complete decomposition, svd (A) will return S of the same size as A. - If m > n, svd (A, 0) will return S as a square of order min ([m, n]). - If m < n, svd (A, 0) will return S of the same size as A. 

    For an m × n matrix A with m < n, the reduced decomposition svd (A, 'econ') computes only the first m columns of V. In this case, the columns of V are orthogonal, and V is an n × m matrix that satisfies. For a complete decomposition, svd (A) returns V in the form of an n × n unitary matrix that satisfies. Zero spaces with no corresponding non-zero singular values in V form a set of standard orthogonal basis vectors. Different computers and MATLAB versions can generate different singular vectors, which remain numerically accurate. The corresponding columns in U and V can be flipped over, as this does not affect the value of the expression A = USV '. 

#  Code example 

##  1. The singular value of the matrix 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595460
  ```  
 Calculation result 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595460
  ```  
##  2. Singular Value Decomposition 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595460
  ```  
##  3. Matrix rank, column space, and zero space 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574595460
  ```  
#  III. Applications in point clouds 

 [1] matlab 计算点云的曲率 [2] matlab 点云最小二乘拟合平面（SVD法） [3] matlab 点云最小二乘拟合平面(PCA法) [4] matlab 最小二乘拟合空间直线 [5] matlab 点云配准——SVD分解求变换矩阵 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

   See: Three-point fixed circle derivation formula. 

#  Code implementation 

 ThreePoint2Circle.m 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574559163
  ```  
 main.m 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574559163
  ```  
#  III. Display of results 

 ![avatar]( 6633e97975ec461f9c3f50dbc8c517ee.png) 



--------------------------------------------------------------------------------


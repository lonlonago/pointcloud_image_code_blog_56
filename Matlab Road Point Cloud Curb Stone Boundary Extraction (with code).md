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


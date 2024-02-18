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


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


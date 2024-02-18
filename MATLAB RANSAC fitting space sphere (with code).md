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


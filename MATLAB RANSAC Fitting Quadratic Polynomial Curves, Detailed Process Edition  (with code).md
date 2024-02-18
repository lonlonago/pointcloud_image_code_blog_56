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


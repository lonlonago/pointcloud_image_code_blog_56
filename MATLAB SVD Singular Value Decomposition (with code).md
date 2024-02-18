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


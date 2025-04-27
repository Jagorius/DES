# Differential Evolution Strategy - DES

This repository is an implementation of the Differential Evolution Strategy (DES), an algorithm that is a crossover between Differential Evolution (DE) and CMA-ES. The method is competitive against CMA-ES in performing both local and global optimization. DES models the dynamics of changes in the distributions of the generated populations in the CMA-ES algorithm, without having to estimate or approximate the actual covariance matrix. DES maintains time complexity linear to the number of dimensions for a range of different objective functions and also has an experimentally validated tendency to fit the contours of the objective function.

[Toward a Matrix-Free Covariance Matrix Adaptation Evolution Strategy
](https://ieeexplore.ieee.org/document/8673614)

## Installation:
Impemenation of the DES algorithm is available in R language in the form of the file DES.R. However, the following packages need to be installed:
```bash
install.packages("https://cran.r-project.org/src/contrib/Archive/ringbuffer/ringbuffer_1.1.tar.gz", repos=NULL)
```

## Installation cec2017 benchmark:
Package cec2017 provides R wrappers for the C implementation of 30 CEC2017 benchmark functions. Functions 1 to 30 available in dimensions 10, 30, 50, 100.
```R
install.packages("https://staff.elka.pw.edu.pl/~djagodzi/cec2017/cec2017_0.3.0.tar.gz")
```

## Usage cec2017 benchmark:
Example of the use of the DES algorithm on the CEC2017 optimisation benchmark functions.
```R
#30 dimensions, function 1
DES(rep(0,10),fn=function(x){cec2017(1,x)}) 

#100 dimensions, function 30
DES(rep(0,100),fn=function(x){cec2017(30,x)}) 
```
## License
The use of the DES method for scientific purposes requires citation to: [Toward a Matrix-Free Covariance Matrix Adaptation Evolution Strategy in IEEE Transactions on Evolutionary Computation, doi: 10.1109/TEVC.2019.2907266](https://ieeexplore.ieee.org/document/8673614)
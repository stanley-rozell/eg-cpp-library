---
title: example::LinearRegressionModel
summary: Linear Regression Model. 

---

# example::LinearRegressionModel



Linear Regression Model. 
<br /> `#include <linear_regression_model.h>`

## Public Functions

|                | Name           |
| -------------- | -------------- |
| | **[LinearRegressionModel](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/#function-linearregressionmodel)**(const arma::mat & x, const arma::mat & z)<br>Constructs and fits a new [LinearRegressionModel](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/).  |
| | **[LinearRegressionModel](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/#function-linearregressionmodel)**(const arma::mat & C, const arma::vec & d, const arma::mat & R)<br>Constructs a new [LinearRegressionModel](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/).  |
| auto | **[C](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/#function-c)**() const<br>get output matrix (C)  |
| auto | **[d](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/#function-d)**() const<br>get output bias (d)  |
| auto | **[R](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/#function-r)**() const<br>get measurement noise covariance (R)  |
| auto | **[simulate](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/#function-simulate)**(const arma::mat & x, bool add_noise =false)<br>simulates linear regression model  |

## Public Attributes

|                | Name           |
| -------------- | -------------- |
| const size_t | **[n_x](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/#variable-n_x)** <br>number of input channels  |
| const size_t | **[n_y](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/#variable-n_y)** <br>number of output channels  |

## Protected Attributes

|                | Name           |
| -------------- | -------------- |
| arma::mat | **[C_](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/#variable-c_)** <br>output matrix  |
| arma::vec | **[d_](/eg-cpp-library/docs/api/classes/classexample_1_1_linear_regression_model/#variable-d_)** <br>output bias  |

## Public Function Details

### **LinearRegressionModel**

```cpp
LinearRegressionModel(
    const arma::mat & x,
    const arma::mat & z
)
```



**Parameters**:

  * **x** Input data [n_x x n_t] 
  * **z** Measured output data [n_y x n_t] 


Given input/output data, constructs and fits a new Linear Regression Model:

{{< katex display >}} \mathbf{y}_t = \mathbf{C} \mathbf{x}_{t} + \mathbf{d} {{< /katex >}}

{{< katex display >}} \mathbf{z}_t \sim \mathcal{N}\left(\mathbf{y}_t , \mathbf{R} \right) {{< /katex >}}

where {{<katex>}} \mathbf{x}_{t} {{</katex>}}, {{<katex>}} \mathbf{y}_{t} {{</katex>}}, and {{<katex>}} \mathbf{z}_{t} {{</katex>}} the input, output, and measurement, respectively; {{<katex>}} \mathbf{C} {{</katex>}} is the output matrix; {{<katex>}} \mathbf{d} {{</katex>}} is the output bias; and {{<katex>}} \mathbf{R} {{</katex>}} is the covariance of the assumed Gaussian measurement noise.


### **LinearRegressionModel**

```cpp
LinearRegressionModel(
    const arma::mat & C,
    const arma::vec & d,
    const arma::mat & R
)
```



**Parameters**:

  * **C** output matrix 
  * **d** output bias 
  * **R** measurement noise covariance 


Constructs a new Linear Regression Model from parameters:

{{< katex display >}} \mathbf{y}_t = \mathbf{C} \mathbf{x}_{t} + \mathbf{d} {{< /katex >}}

{{< katex display >}} \mathbf{z}_t \sim \mathcal{N}\left(\mathbf{y}_t , \mathbf{R} \right) {{< /katex >}}

where {{<katex>}} \mathbf{x}_{t} {{</katex>}}, {{<katex>}} \mathbf{y}_{t} {{</katex>}}, and {{<katex>}} \mathbf{z}_{t} {{</katex>}} the input, output, and measurement, respectively; {{<katex>}} \mathbf{C} {{</katex>}} is the output matrix; {{<katex>}} \mathbf{d} {{</katex>}} is the output bias; and {{<katex>}} \mathbf{R} {{</katex>}} is the covariance of the assumed Gaussian measurement noise.


### **C**

```cpp
inline auto C() const
```



### **d**

```cpp
inline auto d() const
```



### **R**

```cpp
inline auto R() const
```



### **simulate**

```cpp
auto simulate(
    const arma::mat & x,
    bool add_noise =false
)
```



**Parameters**:

  * **x** input data 
  * **add_noise** whether to add measurement noise


**Return**: model output 

## Public Attribute Details

### **n_x**

```cpp
const size_t n_x;
```



### **n_y**

```cpp
const size_t n_y;
```



## Protected Attribute Details

### **C_**

```cpp
arma::mat C_;
```



### **d_**

```cpp
arma::vec d_;
```



-------------------------------

Updated on 26 February 2021 at 23:10:57 CST

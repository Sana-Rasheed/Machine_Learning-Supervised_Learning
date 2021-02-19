# Course - Supervised Learning 

##### NOTE: 
1. Your code MUST execute without any errors. 
2. You can add more lines in your code as required.

## Section 1: Basic Statistical Concepts

### Question 1 
**The dataset is loaded for you. Perform the following tasks:**  
1. Compute basic statistical measures for each of the variables from the freeny dataset.  
2. Construct a correlation matrix for all the variables in the freeny dataset.  
3. Create a new variable price.income.ratio constructed as a ratio of price.index and income.level. Print its summary statistics.  


```R
library(datasets)
```


```R
head(freeny)
```


<table>
<thead><tr><th></th><th scope=col>y</th><th scope=col>lag.quarterly.revenue</th><th scope=col>price.index</th><th scope=col>income.level</th><th scope=col>market.potential</th></tr></thead>
<tbody>
	<tr><th scope=row>1962.25</th><td>8.79236</td><td>8.79636</td><td>4.70997</td><td>5.82110</td><td>12.9699</td></tr>
	<tr><th scope=row>1962.5</th><td>8.79137</td><td>8.79236</td><td>4.70217</td><td>5.82558</td><td>12.9733</td></tr>
	<tr><th scope=row>1962.75</th><td>8.81486</td><td>8.79137</td><td>4.68944</td><td>5.83112</td><td>12.9774</td></tr>
	<tr><th scope=row>1963</th><td>8.81301</td><td>8.81486</td><td>4.68558</td><td>5.84046</td><td>12.9806</td></tr>
	<tr><th scope=row>1963.25</th><td>8.90751</td><td>8.81301</td><td>4.64019</td><td>5.85036</td><td>12.9831</td></tr>
	<tr><th scope=row>1963.5</th><td>8.93673</td><td>8.90751</td><td>4.62553</td><td>5.86464</td><td>12.9854</td></tr>
</tbody>
</table>




```R

```


```R

```


```R

```

### Good Job! You are done with the section!

## Section 2: Machine Learning: Regression Analysis

### Question 1
**Based on the observations acquired from the above exercise:**  
1. Construct a linear regression model using y as dependent variable and top 2 variables with the highest correlation with y as dependent variable.  
2. Calculate the r-squared value for the constructed model.  
3. Use half the dataset for training and the remaining for testing.  
4. Generate in-sample and out-sample predictions and compute variance of residuals [hint: residual= y_predicted - y_observed]  
5. Plot the actual and predicted results for y variable.  


```R

```


```R

```


```R

```

### Good Job! You are done with the section!

## Section 3: Machine Learning: Logistic Regression

## Question 1  
**Construct a logistic regression model using the Smarket dataset:**  
1. Your task is to predict the direction [Up: 1, Down:0].  
2. Use a combination of variables that produces the lowest residual variance.  
3. Plot the predicted vs. actual values.  
4. Construct variable importance plot for all the variables.  


```R
# install.packages('ISLR')
require('ISLR')
head(Smarket)
```


<table>
<thead><tr><th scope=col>Year</th><th scope=col>Lag1</th><th scope=col>Lag2</th><th scope=col>Lag3</th><th scope=col>Lag4</th><th scope=col>Lag5</th><th scope=col>Volume</th><th scope=col>Today</th><th scope=col>Direction</th></tr></thead>
<tbody>
	<tr><td>2001  </td><td> 0.381</td><td>-0.192</td><td>-2.624</td><td>-1.055</td><td> 5.010</td><td>1.1913</td><td> 0.959</td><td>Up    </td></tr>
	<tr><td>2001  </td><td> 0.959</td><td> 0.381</td><td>-0.192</td><td>-2.624</td><td>-1.055</td><td>1.2965</td><td> 1.032</td><td>Up    </td></tr>
	<tr><td>2001  </td><td> 1.032</td><td> 0.959</td><td> 0.381</td><td>-0.192</td><td>-2.624</td><td>1.4112</td><td>-0.623</td><td>Down  </td></tr>
	<tr><td>2001  </td><td>-0.623</td><td> 1.032</td><td> 0.959</td><td> 0.381</td><td>-0.192</td><td>1.2760</td><td> 0.614</td><td>Up    </td></tr>
	<tr><td>2001  </td><td> 0.614</td><td>-0.623</td><td> 1.032</td><td> 0.959</td><td> 0.381</td><td>1.2057</td><td> 0.213</td><td>Up    </td></tr>
	<tr><td>2001  </td><td> 0.213</td><td> 0.614</td><td>-0.623</td><td> 1.032</td><td> 0.959</td><td>1.3491</td><td> 1.392</td><td>Up    </td></tr>
</tbody>
</table>




```R

```


```R

```


```R

```


```R

```


```R

```

### Good Job! You are done with the section!

## Section 4: Machine Learning: Decision Trees and Random Forests

## Question 1  
**Construct a decision tree for the following dataset:**  
1. Your task is to predict whether the sales will be High or Low.  
2. You need to transform the Sale variable into binary variable: For sales less than 7.5, assign a value of Low and High otherwise. You will also need to transform ShelveLoc, Urban and US variables into binary variables.    
3. Generate a decision tree and plot the diagram for the tree and plot predicted vs. actual results.  
4. Attempt a random forest regression on the same dataset. Which model produces better results?  


```R
head(Carseats)
```


<table>
<thead><tr><th scope=col>Sales</th><th scope=col>CompPrice</th><th scope=col>Income</th><th scope=col>Advertising</th><th scope=col>Population</th><th scope=col>Price</th><th scope=col>ShelveLoc</th><th scope=col>Age</th><th scope=col>Education</th><th scope=col>Urban</th><th scope=col>US</th></tr></thead>
<tbody>
	<tr><td> 9.50 </td><td>138   </td><td> 73   </td><td>11    </td><td>276   </td><td>120   </td><td>Bad   </td><td>42    </td><td>17    </td><td>Yes   </td><td>Yes   </td></tr>
	<tr><td>11.22 </td><td>111   </td><td> 48   </td><td>16    </td><td>260   </td><td> 83   </td><td>Good  </td><td>65    </td><td>10    </td><td>Yes   </td><td>Yes   </td></tr>
	<tr><td>10.06 </td><td>113   </td><td> 35   </td><td>10    </td><td>269   </td><td> 80   </td><td>Medium</td><td>59    </td><td>12    </td><td>Yes   </td><td>Yes   </td></tr>
	<tr><td> 7.40 </td><td>117   </td><td>100   </td><td> 4    </td><td>466   </td><td> 97   </td><td>Medium</td><td>55    </td><td>14    </td><td>Yes   </td><td>Yes   </td></tr>
	<tr><td> 4.15 </td><td>141   </td><td> 64   </td><td> 3    </td><td>340   </td><td>128   </td><td>Bad   </td><td>38    </td><td>13    </td><td>Yes   </td><td>No    </td></tr>
	<tr><td>10.81 </td><td>124   </td><td>113   </td><td>13    </td><td>501   </td><td> 72   </td><td>Bad   </td><td>78    </td><td>16    </td><td>No    </td><td>Yes   </td></tr>
</tbody>
</table>




```R

```


```R

```


```R

```

### Good Job! You are done with the section!

## Section 5: Neural Networks

## Question 1  
**Construct a neural network for the same dataset:**  
1. Your task is to predict whether the sales will be High or Low.  
2. Perform necessary data transformations as required.      
3. Generate neural network with 3 layers and 2,3,4 nodes respectively.    
4. Plot the nn.


```R
# install.packages('neuralnets')
```


```R

```


```R

```


```R

```

### Good Job! You are done with the section!

## Section 6: Performance Evaluation

## Question 1  
**For the above decision tree, logistic regression and neural network models:**  
1. Construct a confusion matrix.  
2. Plot out the ROC and AUC cruves.   
3. For the datasets of Carseats, which model produced the highest accuracy with lowest variance?  


```R

```


```R

```


```R

```


```R

```


```R

```

## Good Job! You are done with the course!

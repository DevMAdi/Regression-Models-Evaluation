## 	R Squared for simple, multiple regression
![enter image description here](https://github.com/DevMAdi/Regression-Models-Evaluation/blob/master/Screenshot%20%282615%29.png?raw=true)
we get SSres called as **sum of square of residuals** which is

    SUM(yi-ŷi)square

![enter image description here](https://github.com/DevMAdi/Regression-Models-Evaluation/blob/master/Screenshot%20%282628%29.png?raw=true)
we get SStot called as **total sum of square** which is 

    SUM(yi-yavg)square
Now

    R(square) = 1 - (SSres/SStot)

->> value range -1 to 1. ideal = 1. more close to 1, the better
->> we are fitting line to minimize SSres.
->> yavg also line. By minimizing SSres, we are trying to find best line.
->> how good is your bestline compared to avg. line
->> OLE will never let R(sq) decrease. as we add more var. it will always increase
**->> R(sq) is biased.**

# 	Adjusted R Squared
![enter image description here](https://github.com/DevMAdi/Regression-Models-Evaluation/blob/master/Screenshot%20%282629%29.png?raw=true)
by adding new var. to regression model. R sq. will never minimize, 
even though it helps our model or not. This is because modal always find slight corr. between depend var(y) and new var(x3). so never decrease

**solution**: Adjusted R Squared
![enter image description here](https://github.com/DevMAdi/Regression-Models-Evaluation/blob/master/Screenshot%20%282630%29.png?raw=true)
by introducing new var. we increase R(Sq). as shown in diagram
but no. of P increase in denominator. Thus 2nd term keeps track of good o/p,

// if new var helps lot
-> R(sq) will increase lot & so more impact & so adj. R(sq) will increase
// if new var does not help
-> R(sq) will be same/slight increase & P(no. of regressor) will increase in denominator & so denominator. part will make adj.R(sq). will bring down its value


**practical implementation**
[click here](https://github.com/DevMAdi/Regression-Models/tree/master/Multiple%20Linear%20Regression)
-> when we used regressor.summary() in **back elimination** process.
we got P-value that we compared with SL value
we also got R(Sq). & adj. R(Sq). value. based upon them. we can find best model

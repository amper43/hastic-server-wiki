You can make your model on Python

# Workflow

Imagine you have a jupyter notebook...

Come somewhere, import something.. hz dont know

# Custom Model Class

* First of all download analyzed dataset on jupyter and turn to it in notebook.
![](https://wmpics.pics/di-M7BE.jpg)

* Add needed libs and modules from hastic analytics. 

![](https://wmpics.pics/di-VEZW.jpg)

* So, now you have CustomModel class, which has two main metods: fit and predict.
Segments is passed to the method "fit", in which you can process labeled patterns, extract the necessary information
and use it for prediction. The method "predict" is used to analyze the whole dataset. Using the parameters and data of the first method, you can evaluate your time series, for example, look for anomalies, similar patterns or predict next values.

* Select segments in any way you like. For example:

![](https://wmpics.pics/di-PCD4.jpg)

* Use the CustomModel and its methods to get the result!

![](https://wmpics.pics/di-FANB.jpg)
```

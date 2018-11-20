You can write your own model using Python
https://github.com/hastic/hastic-server/blob/master/analytics/analytics/models/custom_model.py

# Workflow

Imagine you have a model of a specific device where you know some insights about it`s work.
Lets say you monitor a solar panel. You know that the generation of energy at a specific moment 
depends on the sun. You have a model of sun shining. And you have noise and clouds. Lets make a pattern
where you detect anomaly behavior.

We assume that you use Grafana for monitoring. We suggest to install https://github.com/CorpGlory/grafana-data-exporter 
for extracting data from dashboards. 

And lets use Jupyter for designing your model. 

# Custom Model Class

* First of all download analyzed dataset on jupyter and turn to it in notebook.
![](https://wmpics.pics/di-M7BE.jpg)

* Add needed libs and modules from hastic analytics. 

![](https://wmpics.pics/di-VEZW.jpg)

* So, now you have CustomModel class, which has two main methods: fit and predict.
Segments are passed to the method `fit`, in which you can process labeled patterns, extract the necessary information
and use it for prediction. The method `predict` is used to analyze the whole dataset. Using the parameters and data of the first method, you can evaluate your time series, for example, look for anomalies, similar patterns or predict next values.

* Select segments in any way you like. For example:

![](https://wmpics.pics/di-PCD4.jpg)

* Use the CustomModel and its methods to get the result!

![](https://wmpics.pics/di-FANB.jpg)
```

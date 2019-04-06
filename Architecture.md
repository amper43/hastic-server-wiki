# Abstract

Server consist of `analytics` and `server` connected by [zmq](http://zeromq.org/).

Server sends tasks like `LEARN` or `DETECT` and analytics tries to handle workload in async and multi-threaded manner. 

![image](https://user-images.githubusercontent.com/1989898/48625595-c00efb00-e9c0-11e8-9191-b9a207ab8b06.png)

Please see more about how project evolved: 
* https://hastic.io/blog/2018/09/05/Hastic-on-monitorama-2018/ -- first version of architecture 
* https://hastic.io/blog/2019/03/01/Grafanacon-2019/ -- beta version where we introduced support of multiple datasources and async model and [grafana-datasource-kit](https://github.com/CorpGlory/grafana-datasource-kit)
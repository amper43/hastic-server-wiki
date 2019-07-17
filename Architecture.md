# Abstract

Server consist of `analytics` and `server` connected by [zmq](http://zeromq.org/).

Server sends tasks like `LEARN` or `DETECT` and analytics tries to handle workload in async and multi-threaded manner. 

![image](https://user-images.githubusercontent.com/5675912/61381707-23d12700-a8b4-11e9-9da0-539f05387511.png)

Please see more about how project evolved: 
* https://hastic.io/blog/2018/09/05/Hastic-on-monitorama-2018/ -- first version of architecture 
* https://hastic.io/blog/2019/03/01/Grafanacon-2019/ -- beta version where we introduced support of multiple datasources and async model and [grafana-datasource-kit](https://github.com/CorpGlory/grafana-datasource-kit)
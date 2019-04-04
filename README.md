# ELK-Tutorial

# Elastic Search 
  Elastic search is a indexing and querying based over apache's lucene engine.</br>
  It helps download link: [elastic search](https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.7.0.tar.gz) 

```
  cd elasticsearch
  bin/elasticsearch
```

You can check if elasticsearch is up and running at localhost:9200 </br>
Open another terminal and proceed for kibana. </br>
Kibana helps visualizing data using after querying using elastic search.


# kibana
download link: [kibana](https://www.elastic.co/downloads/kibana)

```
  cd kibana
  bin/kibana
```
You can access kibana GUI at localhost:5601 </br>
Logstash helps normazling data from various data soruces such as apache, log events, sql and other data sources. </br>
Also, logstash enhances data us varius filters such as geoip, grok, matcher and many more.
Open another terminal and proceed for logstash


# Logstash

download link: [logstash](https://www.elastic.co/downloads/logstash) <br>
download sample-data from [logs](https://github.com/Alakazam03/ELK-Tutorial/blob/master/logs.zip)<br>
unzip the logs into a folder </br>
download apache.conf file from github repo [apache.conf](https://github.com/Alakazam03/ELK-Tutorial/blob/master/apache.conf)

Now open apache.conf in text editor and change the path field to location of log we downloaded above. </br>
In apache.conf, change <br>
> file{
    path => path_of_logs_file
   .
   .
  }

```
  cd logstash
  bin/logstash -f file_path/apache.conf
```


# Indexing

  * Open kibana in your browser, default localhost:5601.
  * Go to mangament
  * Select index patterns under kibana
  * Create Index Patterns
  * Type logstash-* and click on next step
  * Select @timestamp
  
  ![Screenshot](https://user-images.githubusercontent.com/23367724/55173780-4ffc5700-51a2-11e9-8407-3d300d9a3701.png) <!-- .element height="20%" width="20%" -->
  
  ![Screenshot](https://user-images.githubusercontent.com/23367724/55176701-a324d880-51a7-11e9-9d7f-1c053dbb63e5.png)
  
# Kibana console

  * Go to Discover, you will see your index pattern 
  * As it shows data fro last 15 minutes, we have to change the time range
  * You can see your data 
  
  ![Screenshot](https://user-images.githubusercontent.com/23367724/55173750-47a41c00-51a2-11e9-80a0-16ec90279292.png)
  
  ![Screenshot](https://user-images.githubusercontent.com/23367724/55173780-4ffc5700-51a2-11e9-8407-3d300d9a3701.png)
  
  
# New visualization
  
  * Go to visualization
  * select add new filter and choose data table
  * select paramters as specified in figure. You are free to explore.
  * Save the visualization with a name 
  * Add 2-3 other visualizations and save them
  
   ![Screenshot](https://user-images.githubusercontent.com/23367724/55173182-41fa0680-51a1-11e9-9ae5-72662d551c58.png)
   
   ![Screenshot](https://user-images.githubusercontent.com/23367724/55174241-12e49480-51a3-11e9-8f3f-860752bf5dc6.png)
  
# Dashboard
  
  * Go to dashboard
  * Select add from above. You will see all of your saved visualizations.
  * Select from them and create a dashboard
  
  ![Screenshot](https://user-images.githubusercontent.com/23367724/55172773-90f36c00-51a0-11e9-997c-ae4aa7db9ba6.png)
  
  
 # References 
 
  * https://www.elastic.co
  

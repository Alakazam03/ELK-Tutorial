# ELK-Tutorial

# elastic search 
  download link: [elastic search](https://www.elastic.co/downloads/elasticsearch)

```
  cd elasticsearch
  bin/elasticsearch
```
explore elasticsearch/config for changing port
check if running at localhost:9200


# kibana
download link: [kibana](https://www.elastic.co/downloads/kibana)

```
  cd kibana
  bin/kibana
```
access kibana GUI at localhost:5601


# logstash

download link: [logstash](https://www.elastic.co/downloads/logstash)

```
  cd logstash
  bin/logstash -f location/apache.conf
```

# Indexing

  * Go to mangament
  * Select index patterns under kibana
  * Create Index Patterns
  * Type logstash-* and click on next step
  * Select @timestamp
  
# Kibana visualizations

  * Go to Discover, you will see your index pattern 
  * As it shows data fro last 15 minutes, we have to change the time range
  * You can see your data 
  
# New visualization
  
  * Go to visualization
  * select add new filter and choose data table
  * select paramters as specified in figure. You are free to explore.
  * Save the visualization with a name 
  * Add 2-3 other visualizations and save them
  
# Dashboard
  
  * Go to dashboard
  * Select add from above. You will see all of your saved visualizations.
  * Select from them and create a dashboard
  

# Task1:

## About:

This folder contains a docker-compose file that starts 5 services. Those services are:

1. Nginx: as a web server that serve several static webpages.
2. Elasticsearch
3. Filebeat
4. Logstash
5. Kibana 

Nginx generates some log files which are stored in ES. Filebeat take the logs generated by Nginx and push them to Logstash. Logstash make some modifacations and pudh the records to ES to save them.

We will use Kibana as our dashboard.


## How to use:

- Make sure that you are at the same directory where "vagrant file" is and run ```docker-compose up --build -d```

- You can access the application usign the url ``` localhost:9999 ``` 
- You can access Kibana dashboard usign the url ``` localhost:5601 ``` 
- Elasticsearch url ``` localhost:9200 ``` 

# ELK-Filebeat-for-nginx-application-log
ELFK (elasticsearch, logstash, filebeat, kibana) Log analysis solution for nginx server log and application log

# Installation

1. First Install Elasticsearch, Logstash, Kibana, Filebeat  
2. Run Elasticsearch and Kibana  
3. Setup Logstash  
4. Run Logstash and Filebeat  

### Version
6.3.5

# Filebeat
Filebeat collects the following log files:

1. Nginx:
  - access.log
  - error.log
2. Application:
  - appplication.log contains log level DEBUG, INFO, ERROR
  - error.log only contains log level ERROR
  


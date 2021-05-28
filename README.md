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

# Logstash
Convert unstructured logs into structured log files.

# Application
  * Use spring boot default log format(Unstructured log)
  * Use JSON format application log(Structured log)

## Steps to run the application


1. Start the elk stack, navigate to the elk-configs folder
```
./filebeat -e -c filebeat.yml -d "publish"
```
2. Start the logstash
```
./logstash -f ../config/logstash.conf
```
3. Start the kibana
```
./kibana --allow-root
```
4. Start the logging application
```
mvn spring-boot:run 
```
5. Login to kibana at http://localhost:5601
6. Import indexes and other ELK config using elk-configs/elkSavedObjects.json
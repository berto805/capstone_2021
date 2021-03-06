# Graylog

CSU Channel Island Capstone 2021
by Heberto Rosales


# Introduction
Is a software tool that helps manage logs. Its a great way to centralize logs. Many companies under utilize their existing administration tools because they use too many. Graylog provides ways to simplify all that extra work of maintaining so many tools. 

Graylog allows organizations to have a centralized log location for all the logs being generated inside individual servers. Inside a server you can have different types of logs such as apache, php, mysql, application, etc. With the proper configuration on the server we are able collect very useful logs tailored for each organization's requirements. This can minimize who has access to the servers and instead provide developers or users a better way to look at logs. For example, users accessing the server see raw data that is generally difficult and time consuming to parse manually. By using Graylog, you can see live data and also run custom queries for better searches in order to quickly identify any issues or security incidents.

# Software

For this project I've used Google Cloud Platform.

* Apache
* Rsyslog
* Graylog
* WordPress

# Process Flow

1. The end user hits the Apache servers that are serving Wordpress websites. 
2. Then Apache servers send its apache logs to Graylog
3. Graylog ingests the logs
4. Apache Logs are then parse by a pipeline and stored in their designated stream

In order for apache to send logs we need to configure it on the apache config file. The logformat that im using is here as followed (hyphens will be displayed if output is not available):
* %v - the name of the server being used 
* %h - this is the IP of the client 
* %u - userid of the person requesting the information 
* %t - the timestamp of when the request was made 
* %r - the request line from the client 

Graylog the management log tool. In the console I’ve created some pipelines and Streams to help dissect my data. Pipelines are used as code to parse the data coming in. Streams are used to route messages into categories

# Future Implementation

Graylog is a powerful tool that offers ways to help companies in grow and secure systems. I would like to work on several implementations with this tool:
1. Configure PHP to forward logs to Graylog
2. Configure MySQL to forward logs to Graylog
3. Create pipelines that will help alerting when there is a cyber security threat
4. Create a graph that will help in the analytics portion which will provide geographical and most visited websites data.
5. Create a dashboard for Security Incidents that will assist administrators with identifying the origin of the threats

# Conclusion

Graylog can greatly minimize the tools used in corporate environments. Why would companies waste time cross training new and existing employees with several tools when Graylog can provide that and more on a budget. Graylog is a user friendly tool that will help users disect and troubleshoot issues quickly. With all the functionalities provided by Graylog you can create graphs, charts, tables, alerts and many more. Configuring the servers properly can go a long way in Graylog. Overall having a centralized location for storing logs is crucial in any corporate IT environment as having to use several tools to find the same data will inevitably cause issues for IT personnel. 


# Refrences
1. http://httpd.apache.org/docs/
2. https://docs.graylog.org/docs/streams
3. https://docs.graylog.org/docs/pipelines
4. https://docs.graylog.org/docs/pipelines#
5. https://en.wikipedia.org/wiki/Rsyslog
6. https://en.wikipedia.org/wiki/WordPress
7. https://en.wikipedia.org/wiki/Apache

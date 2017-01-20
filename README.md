# 设计目标

将分布式服务日志汇总到1个服务器上

# 实现步骤

**STEP1.安装ELK**
	
	http://knes1.github.io/blog/2015/2015-08-16-manage-spring-boot-logs-with-elasticsearch-kibana-and-logstash.html
	https://www.elastic.co/downloads/elasticsearch
	https://www.elastic.co/downloads/kibana
	https://www.elastic.co/downloads/logstash
	

**STEP2.配置**

#####2.1配置config/elasticsearch.yml######
	
	network.host：绑定的IP
	http.port:绑定的HTTP访问端口，可以是一个具体值也可以是一个范围，若是范围则找到第一个未被占用的端口号为止，默认值为9200
	transport.tcp.port：绑定的集群端口，可以是一个具体值也可以是一个范围，若是范围则找到第一个未被占用的端口号为止，默认值为9300。
	注意：集群端口这个配置项在yml中没有，需自己配置，不然会占用9300端口，可能产生冲突。

#####2.2编写/bin/logstash.conf文件######

	https://www.elastic.co/guide/en/logstash/current/plugins-inputs-file.html

#####2.3配置config/kibana.yml######
	
	主要需要配置以下三项
	server.port:端口
	server.host:ip
	elasticsearch.url:http://{ip}:{port}

**STEP3.使用**
	
	http://kibana.logstash.es/content

**STEP4.注意点**
	
	注意点1：logstash file plugin directory
	http://stackoverflow.com/questions/38045951/how-to-provide-folder-location-in-logstash-config-file-as-input
	

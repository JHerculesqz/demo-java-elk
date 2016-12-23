# 设计目标

将分布式服务日志汇总到1个服务器上

# 实现步骤

**STEP1.安装、配置ELK**
	
	http://knes1.github.io/blog/2015/2015-08-16-manage-spring-boot-logs-with-elasticsearch-kibana-and-logstash.html
	https://www.elastic.co/downloads/elasticsearch
	https://www.elastic.co/downloads/kibana
	https://www.elastic.co/downloads/logstash
	https://www.elastic.co/guide/en/logstash/current/plugins-inputs-file.html

**STEP2.注意点**
	
	注意点1：logstash file plugin directory
	http://stackoverflow.com/questions/38045951/how-to-provide-folder-location-in-logstash-config-file-as-input
	

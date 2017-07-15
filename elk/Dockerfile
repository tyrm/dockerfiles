FROM sebp/elk

WORKDIR ${LOGSTASH_HOME}
RUN gosu logstash bin/logstash-plugin install logstash-filter-geoip
RUN gosu logstash bin/logstash-plugin install logstash-filter-grok
RUN gosu logstash bin/logstash-plugin install logstash-filter-json
RUN gosu logstash bin/logstash-plugin install logstash-filter-oui

COPY conf/11-nginx.conf /etc/logstash/conf.d/11-nginx.conf

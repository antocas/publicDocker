from 'amazon/opendistro-for-elasticsearch:0.8.0'

RUN echo "node.master: false" >> /usr/share/elasticsearch/config/elasticsearch.yml
RUN echo "node.data: true" >> /usr/share/elasticsearch/config/elasticsearch.yml
RUN echo "node.ingest: true" >> /usr/share/elasticsearch/config/elasticsearch.yml
RUN echo "cluster.remote.connect: false" >> /usr/share/elasticsearch/config/elasticsearch.yml
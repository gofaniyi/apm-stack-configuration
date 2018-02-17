# APM Stack Configuration
This is project consists of the configuration file to setup an application performance monitoring system with Elastic APM on Docker.
Stack consists of Elastic Search, Kibana and APM Server.

For more information, read up here: [Elastic APM](https://www.elastic.co/solutions/apm)

# Pre-requisites
  - Docker

# Setup
Clone this repo into a folder
```bash
git clone git@github.com:gofaniyi/apm-stack-configuration.git
cd apm-stack-configuration
docker-compose -f dev.yml up -d
```

# Additional Info

To confirm your ElasticSearch docker instance is running:
```bash
curl http://localhost:9200
{
  "name" : "VXq60kq",
  "cluster_name" : "docker-cluster",
  "cluster_uuid" : "fTO5-3_nSBOd1qKJT2zZhA",
  "version" : {
    "number" : "6.2.1",
    "build_hash" : "7299dc3",
    "build_date" : "2018-02-07T19:34:26.990113Z",
    "build_snapshot" : false,
    "lucene_version" : "7.2.1",
    "minimum_wire_compatibility_version" : "5.6.0",
    "minimum_index_compatibility_version" : "5.0.0"
  },
  "tagline" : "You Know, for Search"
}
```

To confirm your Kibana docker instance is running:
```bash
curl http://localhost:5601
<script>var hashRoute = '/app/kibana';
var defaultRoute = '/app/kibana';

var hash = window.location.hash;
if (hash.length) {
  window.location = hashRoute + hash;
} else {
  window.location = defaultRoute;
}</script>
```

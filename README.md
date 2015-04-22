# hello.docker.logstash

A quick experiment evaluating the various [docker images for an ELK stack](https://registry.hub.docker.com/search?q=elk), i.e. Elasticsearch, Logstash, Kibana with

- [qnib/elk](https://registry.hub.docker.com/u/qnib/elk/)
- [willdurand/elk](https://registry.hub.docker.com/u/willdurand/elk/)
- [sebp/elk](https://registry.hub.docker.com/u/sebp/elk/)
- ...

For now i checked `sebp/elk` which looks good.

## Prerequisites

You should have installed

- [VirtualBox](https://www.virtualbox.org/) (v4.3.26)
- [vagrant](https://www.vagrantup.com/) (v1.7.2)

## How to use

Just go `vagrant up` and after vagrant and docker have done their magic you should be able to access running instances of 

- Kibana at [http://localhost:5601](http://localhost:5601),
- Elasticsearch at [http://localhost:9200](http://localhost:9200) and
- Logstash at [http://localhost:5000](http://localhost:5000) which receives logs from logstash forwarders
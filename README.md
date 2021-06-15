# Introduction to Elasticsearch

This is a practical introduction to elasticsearch. It contains basic examples and exercises to get started.

## Prerequisites

You will need a couple tools to complete the practical exercises,
choose one of the two options to set up your environment.

The presentation slides can be found [here](https://jamesfer.github.io/intro-elasticsearch-training)

### Using docker (recommended)

  1. Install docker (if not already installed): [official doc](https://www.docker.com/products/docker-desktop)
  2. Run `docker-compose up` to start the Elasticsearch cluster
  3. Verify elasticsearch is running (in a new tab): `curl localhost:9200`
  4. Navigate to `http://localhost:5601` in your browser to verify that kibana is running

To stop elasticsearch, press `Ctrl-C` in the terminal window running docker.

### Install on your machine

If you choose not to follow the recommended installation.

  1. Find version [7.13.2](https://www.elastic.co/downloads/past-releases) for Elasticsearch and Kibana
  2. Follow the installation instructions
    - [Elasticserch](https://www.elastic.co/downloads/elasticsearch)
    - [Kibana](https://www.elastic.co/downloads/kibana)

# KindRed

A Kind cluster with its small fam of tools from the open source community, for POCs, testing, and whatever you want.

## Available tools

Here's the list of the services that are available in this repo:

- [Loki](https://grafana.com/oss/loki/)
- [Grafana](https://grafana.com/grafana/)
- [OpenTelemetry](https://opentelemetry.io/) (work in progress, just for the logs at the moment)
- [Envoy](https://www.envoyproxy.io/) (the configuration provided deploys a minimal API Gateway connected to an echo service)

Additionally, an echo service and a log generator will be deployed automatically at every start-up.

## Usage

The start-up script will create a Kind cluster named `kindred`, with three nodes. **Make sure you have Kind installed on your machine.**

To initialize the whole KindRed of services, run:

    ./start.sh -a

Otherwise, if you want to select only the services you need, run:

    ./start.sh

And follow the instructions prompted.

To delete the cluster, simply run:

    kind delete cluster --name kindred

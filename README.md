HomematicIP Prometheus Exporter
===============================

[![Build Status](https://travis-ci.org/auhlig/homematicip-exporter.svg?branch=master)](https://travis-ci.org/auhlig/homematicip-exporter)
[![Docker Repository](https://img.shields.io/docker/pulls/auhlig/homematicip-exporter.svg?maxAge=604800)](https://hub.docker.com/r/auhlig/homematicip-exporter/)


Expose Prometheus metrics from HomematicIP devices using [coreGreenberet/homematicip-rest-api](https://github.com/coreGreenberet/homematicip-rest-api). 

### Getting started

1. Generate an auth token for the HomematicIP Access Point before using this exporter. Instructions on how to generate an Homematic IP auth token can be found [here](https://github.com/coreGreenberet/homematicip-rest-api#usage).
2. Pass the path to the config file via flag `--config-file=<path-to-file>` or alternatively use `--auth-token` and `--access-point`.

### Usage

```
exporter.py [-h] [--metric-port METRIC_PORT]
                 [--config-file CONFIG_FILE]
                 [--collect-interval-seconds COLLECT_INTERVAL_SECONDS]
                 [--auth-token AUTH_TOKEN] 
                 [--access-point ACCESS_POINT]
                 [--enable-event-metrics ENABLE_EVENT_METRICS]
                 [--log-level LOG_LEVEL]

HomematicIP Prometheus Exporter

optional arguments:
  -h, --help            show this help message and exit
  --metric-port METRIC_PORT
                        port to expose the metrics on (default: 8000)
  --config-file CONFIG_FILE
                        path to the configuration file (default:
                        /etc/homematicip-rest-api/config.ini)
  --collect-interval-seconds COLLECT_INTERVAL_SECONDS
                        collection interval in seconds (default: 30)
  --auth-token AUTH_TOKEN
                        homematic IP auth token (default: None)
  --access-point ACCESS_POINT
                        homematic IP access point id (default: None)
  --enable-event-metrics ENABLE_EVENT_METRICS
                        collect event metrics (default: False)
  --log-level LOG_LEVEL
                        log level (default: 30)
```

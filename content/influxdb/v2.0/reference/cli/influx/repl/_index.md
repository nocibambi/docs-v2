---
title: influx repl
description: >
  The `influx repl` command opens an interactive read-eval-print-loop (REPL)
  from which you can run Flux commands.
menu:
  influxdb_2_0_ref:
    name: influx repl
    parent: influx
weight: 101
aliases:
  - /v2.0/reference/cli/influx/repl/
influxdb/v2.0/tags: [query]
---

The `influx repl` command opens an interactive read-eval-print-loop (REPL)
from which you can run Flux commands.

## Usage
```
influx repl [flags]
```

{{% note %}}
Use **ctrl + d** to exit the REPL.
{{% /note %}}

To use the Flux REPL, you must first authenticate with a [token](/v2.0/security/tokens/view-tokens/).

## Flags
| Flag |                  | Description                                                           | Input type | {{< cli/mapped >}}   |
|:---- |:---              |:-----------                                                           |:----------:|:------------------   |
|      | `--configs-path` | Path to `influx` CLI configurations (default `~/.influxdbv2/configs`) | string     |`INFLUX_CONFIGS_PATH` |
| `-h` | `--help`         | Help for the `repl` command                                           |            |                      |
|      | `--host`         | HTTP address of InfluxDB (default `http://localhost:9999`)            | string     | `INFLUX_HOST`        |
| `-o` | `--org`          | Organization name                                                     | string     | `INFLUX_ORG`         |
|      | `--org-id`       | Organization ID                                                       | string     | `INFLUX_ORG_ID`      |
|      | `--skip-verify`  | Skip TLS certificate verification                                     |            |                      |
| `-t` | `--token`        | Authentication token                                                  | string     | `INFLUX_TOKEN`       |
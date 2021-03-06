# dafka-filter

![Version: 0.0.8](https://img.shields.io/badge/Version-0.0.8-informational?style=flat-square)

A Helm Chart for Dafka Filter

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| name | string | `"kafka-stream-filter"` | name for this stream |
| port | int | `3000` | the port to use |
| replicaCount | int | `1` | pod count |
| sourceTopic | string | `nil` | source topic |
| filters | string | `nil` | filters |
| destinationTopic | string | `nil` | destination topic |
| image.name | string | `"osskit/dafka-filter"` | the image name to use |
| image.tag | string | `"0.1"` | the image tag to use |
| startupProbe.initialDelaySeconds | int | `60` |  |
| startupProbe.httpGet.path | string | `"/ready"` | the path for startup check |
| startupProbe.httpGet.port | int | `3000` |  |
| livenessProbe.initialDelaySeconds | int | `30` |  |
| livenessProbe.httpGet.path | string | `"/ready"` | the path for liveness check |
| livenessProbe.httpGet.port | int | `3000` |  |
| readinessProbe.httpGet.path | string | `"/ready"` | the path for readiness check |
| readinessProbe.httpGet.port | int | `3000` |  |
| resources.requests.cpu | string | `"50m"` | cpu requests |
| resources.requests.memory | string | `"100Mi"` | memory requests |
| resources.limits.cpu | string | `"200m"` | cpu limits |
| resources.limits.memory | string | `"400Mi"` | memory limits |
| metrics.enabled | bool | `true` | should prometheus scrape this server |
| metrics.path | string | `"/metrics"` | a path prometheus should scrape metrics from |
| auth.enabled | bool | `false` | should use authentication |
| auth.saslUsername | string | `nil` | sasl username |
| auth.saslPassword | string | `nil` | sasl password (not encrypted) |
| auth.secrets.useOpaqueSecrets | bool | `true` | should mount secrets to opaque secrets |
| auth.secrets.useTrustsore | bool | `false` | should use truststore |
| auth.secrets.gcp.saslPasswordResource | string | `nil` | gcp secret resource for sasl password |
| auth.secrets.gcp.truststoreResource | string | `nil` | gcp secret resource for truststore file |
| auth.secrets.gcp.truststorePasswordResource | string | `nil` | gcp secret resource for truststore password |
| auth.secrets.vault.saslPasswordSecretPath | string | `nil` | vault secret path for sasl password |
| auth.secrets.vault.saslPasswordSecretKey | string | `nil` | vault secret key for sasl password |
| auth.secrets.vault.truststoreSecretPath | string | `nil` | vault secret path for truststore file |
| auth.secrets.vault.truststoreSecretKey | string | `nil` | vault secret key for truststore file |
| auth.secrets.vault.truststorePasswordSecretPath | string | `nil` | vault secret path for truststore password |
| auth.secrets.vault.truststorePasswordSecretKey | string | `nil` | vault secret key for truststore password |


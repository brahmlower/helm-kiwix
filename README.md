
# Kiwix Helm Chart

A helm chart for [kiwix](https://kiwix.org/en/).

## Installing the Chart

```
helm repo add brahmlower-kiwix https://brahmlower.github.io/helm-kiwix
helm install kiwix brahmlower-kiwix/kiwix
```

## Contributing

### Values Schema Generation

Schema generation via [helm-values](https://github.com/brahmlower/helm-values).
```
helm plugin install https://github.com/brahmlower/helm-values
```

Update the schema and docs:
```
helm values schema .
helm values docs .
```

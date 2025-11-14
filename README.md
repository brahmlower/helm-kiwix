
# Kiwix Helm Chart

A helm chart for [kiwix](https://kiwix.org/en/).

## Installing the Chart

```
helm repo add brahmlower-kiwix https://brahmlower.github.io/helm-kiwix
helm install kiwix brahmlower-kiwix/kiwix
```

## Contributing

## Values Schema Generation

Schema generation via [helm-schema](https://github.com/dadav/helm-schema).
```
helm plugin install https://github.com/dadav/helm-schema
```

Update the schema with:
```
helm schema -rap
```

Validate the values against the schema:
```
helm lint --strict ./charts/kiwix
```

## Docs Generation

Docs generation via [helm-docs](https://github.com/norwoodj/helm-docs)
```
brew install norwoodj/tap/helm-docs
```

Update the schema with:
```
helm-docs
```

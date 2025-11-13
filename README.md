
# Kiwix Helm Chart

A helm chart for [kiwix](https://kiwix.org/en/).

## Installing the Chart

```
helm repo add brahmlower-kiwix https://brahmlower.github.io/helm-kiwix
helm install kiwix brahmlower-kiwix/kiwix
```

## Configuration

Example configuration:

```yaml
args: ["/data/zims/*"]

volumeMounts:
- name: kiwix-data
  mountPath: "/data/zims"
  readOnly: true

volumes:
- name: kiwix-data
  persistentVolumeClaim:
    claimName: kiwix-data

volumeClaimTemplates:
- metadata:
    name: kiwix-data
  spec:
    storageClassName: my-storage-class
    accessModes:
      - ReadWriteOnce
    resources:
      requests:
        storage: 3Gi

ingress:
  enabled: true
  hosts:
    - host: kiwix.example.com
      paths:
        - path: /
          pathType: ImplementationSpecific
  tls:
    - secretName: kiwix
      hosts:
        - kiwix.example.com
```

See the values.yaml file for more options.

Better docs to come.

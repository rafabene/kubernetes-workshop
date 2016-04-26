# Managing application configurations and secrets

```
kubectl create secret generic certs --from-file=tls/
```

```
kubectl describe secrets certs
```

```
kubectl create configmap nginx-proxy --from-file=nginx/proxy.conf
```

```
kubectl describe configmaps nginx-proxy
```

```
kubectl create -f monolith-secure-pod.yaml
```

```
kubectl get pods
```

```
kubectl port-forward monolith-secure 10443:443
```

```
curl --cacert kubernetes/tls/ca.pem https://127.0.0.1:10443
```

```
kubectl logs -c nginx monolith-secure
```
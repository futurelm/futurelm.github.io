### clean evicted all pods  
```
kubectl get po -A |grep Evicted|awk '{system ("kubectl delete po "$2" -n "$1)}'
```

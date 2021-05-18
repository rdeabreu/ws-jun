# ws-may

## Dynamic Packet capture

```
kubectl label $(kubectl get pod -o name --no-headers) sec=quarantine
```
```
calicoctl create -f capture.yaml
```
```
calicoctl get packetcapture
```
```
calicoctl delete -f capture.yaml
```
```
calicoctl captured-packets copy attacker-pcap -d "/tmp"
```

## Cleanup:

Delete the rogue application

```
kubectl delete -f alert.yaml
```
```
kubectl delete -f policies.yaml
```
```
kubectl delete -f https://installer.calicocloud.io/storefront-demo.yaml
```

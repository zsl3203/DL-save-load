# prerequisite
running k8s cluster, for detail please visit `https://github.com/zsl3203/summer`

# deploy PV and PVC
```
kubectl apply -f pv.yaml
kubectl apply -f pvc.yaml
```
# run the deep learning job
```
kubectl apply -f rnn-test.yaml
```
# save and load
the output logs and DL-models are saved under dir `/mnt/data`
to load the model data and continue training, simply deploy the DL job again
```
kubectl delete pods rnn-test
kubectl apply -f rnn-test.yaml
```
# Comparison b/w both

`oc create -f pod.yaml`{{execute}}
`oc get pods --show-labels`{{execute}}

We want condition like And OR 
Replicaset Should Capture Pods which have either Label app=myapp1 Or app=myapp2

## Create a ReplicaSet
`cat replicaSet1.yaml`{{execute}}

See the selector Section use Set based Selection

`oc create -f replicaSet1.yaml`{{execute}}

## View Pods

`oc get pods --show-labels`{{execute}} 

No New Pods are created due to set based approach of Replica Sets


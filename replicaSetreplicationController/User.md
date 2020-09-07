# Replication Controller

### Clone repo 
`git clone https://github.com/cloudpassion1801/openshiftResources.git`{{execute}}

`cd openshiftResources`{{execute}}

### Create 2 Pods 
`oc create -f pod.yaml`{{execute}}

See the labels of Pods
`oc get pods --show-labels`{{execute}}

2 Type of lAbels are present 
app=myapp1,tier=frontend
app=myapp2,tier=frontend

### View Replication Controller Yaml 
`cat replicationController.yml`{{execute}}

--> Selects all pods with selector app=myapp1 & replicas =3

`oc create -f replicationController.yml`{{execute}}

View New Pods created
`oc get pods --show-labels`{{execute}}
Verify it has only triggered 2 more pods .. Acquired a previous Pod 
`oc describe pod testpod2 | grep Controlled`{{execute}}
Verify it is controlled by replication Controller


## Clear Resources
`oc delete rc my-rc`{{execute}}
`oc get pods --show-labels`{{execute}}
Verify 3 Pods are deleted

`oc delete pod testpod1`{{execute}}

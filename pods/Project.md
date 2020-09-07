# Understanding Pods

## Clone beow repo 
`git clone https://github.com/cloudpassion1801/openshiftResources.git`{{execute}}
Change Directory

`cd openshiftResources `{{execute}}

## View Pod Yaml 

`cat pod.yaml`{{execute}} 

Verify names of Pods 
Find Image to be used in both Pods
Find Command to be executed in Both Pods

## Create Pod
`oc create -f pod.yaml`{{execute}}


## Get all Pods
` oc get pods`{{execute}}

Verify Name of Both pods is same as given in Yaml .
Verify the status and wait till status is running

## See Pod details
`oc describe pod testpod1`{{execute}}
`oc get pod testpod1 -o yaml`{{execute}}

Change Commandd of First Pod 
`oc edit pod testpod1`{{execute}}

## Verify Pod Logs
`oc logs testpod1`{{execue}}

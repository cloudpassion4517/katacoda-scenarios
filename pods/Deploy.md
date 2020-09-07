# STart a new  build
`oc start-build ruby-ex`{{execute}}

# Watch a build 
`oc logs -f bc/ruby-ex`{{execute}}

# Interacting directly with the container is simple with oc rsh
oc rsh podName

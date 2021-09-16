# Expscreen
I have specified the pod-anti affinity rules in order to provide fault tolerance and would create a resource Pod-Disruption-Budget and set to the value so that all the pods aren't deleted when there is a Node drain to upgrade or other maintainence activities 

I Choose the deployment startegy type : RollingUpdate, to avoid all pods get evicted while implementing any change(for ex : new image version)

I have assumed nginx as Ingress controller to expose the services, added annotation class in the nginx api object

For High Availabilty and resilience I would have opted for Horizontol-Pod-AutoScaling to scale the applications based on the resource metrics or custom metrics and Cluster-Autoscaler to scale the cluster If the pods'aren't getting placed due to the insufficient resources

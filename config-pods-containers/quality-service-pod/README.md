When Kubernetes creates a Pod it assigns one of these QoS classes to the Pod:

Guaranteed
Burstable
BestEffort


For a Pod to be given a QoS class of Guaranteed:

Every Container in the Pod must have a memory limit and a memory request, and they must be the same.
Every Container in the Pod must have a cpu limit and a cpu request, and they must be the same.


A Pod is given a QoS class of Burstable if:

The Pod does not meet the criteria for QoS class Guaranteed.
At least one Container in the Pod has a memory or cpu request.


For a Pod to be given a QoS class of BestEffort, the Containers in the Pod must not have any memory or cpu limits or requests.

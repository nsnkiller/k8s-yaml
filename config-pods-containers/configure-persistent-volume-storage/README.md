how to configure a Pod to use a PersistentVolumeClaim for storage

1.A cluster administrator creates a PersistentVolume that is backed by physical storage. The administrator does not associate the volume with any Pod.

2.A cluster user creates a PersistentVolumeClaim, which gets automatically bound to a suitable PersistentVolume.

3.The user creates a Pod that uses the PersistentVolumeClaim as storage.

1. The Dockerfile adds the ceph rbd client into the kube-controler-manager image, for the official image does not include the rbd which 
casuses the Error "creating rbd image: executable file not found in $PATH"

2. kube-controller-manager.yaml change the official image to the new image above mentioned

3. Make the new kube-controller-manager.yaml into the /etc/kubernetes/manifests/

4. Restart the kubelet, the new pod kube-controller-manager will be restarted using the new image.


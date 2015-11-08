# Introduction:

  Google Compute Engine (GCE) is the Infrastructure as a Service (IaaS) 
  component of Google Cloud Platform which is built on the global infrastructure 
  that runs Google's search engine, Gmail, YouTube and other services. Google Compute
  Engine enables users to launch virtual machines (VMs) on demand.
  
# Starting Point:
*A place that marks the beginning of a journey *

1. Start by creating a GCE account.
2. Build up an VM image instance of your choice.
  (I had choosen f1.micro image for my reference and coreos image instance)

3.*Switch into root user*: 
```sh
sudo -s
cd home
```

4.*Install the kubernetesv1.0 compressed file:*
```sh
wget https://github.com/GoogleCloudPlatform/kubernetes/releases/download/v1.0.1/kubernetes.tar.gz
```

5.*Untar the kubernetes package:*
```
tar -xvf kubernetes.tar.gz
```

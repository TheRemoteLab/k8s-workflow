# Introduction:

  Amazon Web Services (AWS), is a collection of remote computing services,
  also called web services, that make up a cloud-computing platform offered by Amazon.com.
  It is one of the amazing and most popular cloud services used by multiple companies around the globe.
  
# Starting Point:


1. Start by creating an AWS account.
2. Build up an EC2 image instance of your choice.
  (I had choosen t2.micro image for my reference) 
3. After creating your instance, use
```sh
ssh -i "secret.pem" ubuntu@45.67.23.14 
```
to login into your instance. 

PS:
If you have any problem regarding logging into your instance,
try rebooting your instance from aws console.

4.*Switch into root user*: 
```sh
sudo -s
```

5.Ensure these packages are installed
ssh,docker.io,curl

If not,
```sh
apt-get install docker.io && curl && ssh
```

6.*Generate Public and Private Keys,so that you could automatically ssh into 127.0.0.1,*
```
ssh-keygen -t rsa
cat /root/.ssh/id_rsa.pub >> /root/.ssh/authorized_keys
```

7.*Install the kubernetesv1.0 compressed file:*
```sh
wget https://github.com/GoogleCloudPlatform/kubernetes/releases/download/v1.0.1/kubernetes.tar.gz
```

8.*Untar the kubernetes package:*
```
tar -xvf kubernetes.tar.gz
```

9.*Download the latest binaries on kubernetes path:*
```
cd kubernetes/cluster/ubuntu
./build.sh
```

10.*Change the config-default.sh accordingly*
```sh
cd
vi kubernetes/cluster/ubuntu/config-default.sh
export nodes="root@127.0.0.1"
export roles="ai"
export NUM_MINIONS=${NUM_MINIONS:-1}
```

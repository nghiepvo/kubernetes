# Kubernetes tutorial

1. Environment.
  - Ubuntu 18.10 x2 (include master and node)
2. Install.
  - Kubernetes 1.13.2
  (run for both)
  
  > sudo apt update 
  
  > sudo apt upgrade
  
  > sudo apt install docker.io
  
  > docker --version
  
  > sudo systemctl enable docker
  
  > curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add
  
  > sudo apt-add-repository "deb http://apt.kubernetes.io/ kubernetes-xenial main"
  
  > sudo apt install kubeadm
  
  > kubeadm version
  
  *if the ubuntu os run on virtual PC:*
  
  > sudo swapoff -a
  
  (run on master)
  *if the ubuntu os run on virtual PC:*
  
  > sudo hostnamectl set-hostname master
  
  (run on node)
  *if the ubuntu os run on virtual PC:*
  > hostnamectl set-hostname node
  
   (run on master)
   
  > sudo kubeadm init --pod-network-cidr=10.244.0.0/16
  
  > mkdir -p $HOME/.kube
  
  > sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
  
  > sudo chown $(id -u):$(id -g) $HOME/.kube/config
  
   print token to join on master.
  
  > kubeadm token create --print-join-command
  
  > kubectl get nodes
  
  Install Network
  > sudo kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml
  
  > kubectl get pods --all-namespaces
  
  2. Create a domain free on https://www.freenom.com/ and ssl free on https://www.sslforfree.com
  
  we will have these image below:
  
![image01](https://user-images.githubusercontent.com/47117818/51857573-31760d00-2365-11e9-9ee5-0801da12fa65.png)

![image](https://user-images.githubusercontent.com/47117818/51857768-acd7be80-2365-11e9-98ee-323e7ee77183.png)

![image](https://user-images.githubusercontent.com/47117818/51857826-d264c800-2365-11e9-8551-8f125074ac52.png)

![image](https://user-images.githubusercontent.com/47117818/51857617-4b175480-2365-11e9-8e54-11893d895b78.png)


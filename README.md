# ignite_minikube

following are the helpful commands


  git clone https://github.com/shub0011/ignite_minikube.git
  
  cd ignite_minikube/
  
  kubectl create -f ignite.yaml
  
  kubectl describe deployment ignite
  
  kubectl describe pods ignite
  
  kubectl describe service ignite
  
  kubectl get pods
  
  kubectl logs ignite-6f5bf7b95d-65h94
  
  kubectl exec -it ignite-6f5bf7b95d-65h94 -- tail /opt/ignite/apache-ignite-fabric-2.4.0-bin/work/log/ignite-fcd8154d.0.log
  
  minikube service ignite --url
  
  export IGNITE_EP=$(minikube service ignite --url)
  
  curl $IGNITE_EP/ignite\?cmd\=top
  
  curl $IGNITE_EP/ignite\?cmd\=getorcreate\&cacheName\=test
  
  curl $IGNITE_EP/ignite\?cmd\=put\&key\=key\&val\=value\&cacheName\=test
  
  curl $IGNITE_EP/ignite\?cmd\=get\&key\=key\&cacheName\=test
  

  #Pre requisite commands (macos)

  brew install kubectl
  
  brew install minikube
  
  minikube start
  
  kubectl cluster-info
  
  minikube dashboard


#The image we are using : 

https://hub.docker.com/r/alpert/ignite (1M pulls)

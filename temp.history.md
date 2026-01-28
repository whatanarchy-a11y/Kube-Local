350  kubectl get svc -A -o wide
  351  kubectl get pod -A -o wide
  352  kubectl get node -A -o wide
  353  kubectl get ns -A -o wide
  354  clear
  355  kubectl get pod -A -o wide
  356  kubectl get pod -A -o wide | grep 'my-'
  357  kubectl get pod -A -o wide | egrep 'my-'
  358  kubectl get pod -A -o wide | egrep 'hpa'
  359  kubectl run --help
  360  kubectl run my-first-pod --image stacksimplify/kubenginx:1.0.0
  361  kubectl get pod -A -o wide | egrep 'my-'
  362  kubectl get pod -A -o wide | grep 'my-'
  363  kubectl get pod -A -o wide
  364  sudo crictl images
  365  sudo crictl images | grep 'stack'
  366  sudo crictl images | grep 'kong'
  367  kubectl get pod my-first-pod -o wide
  368  kubectl get pod my-first-pod
  369  clear
  370  kubectl describe pod my-first-pod
  371  kubectl get pod my-first-pod
  372  kubectl run myapp --image nginx
  373  kubectl get pods -o wide
  374  kubectl get pods -A -o wide
  375  kubectl -v=v8 get pods -A -o wide
  376  kubectl -v=6 get pods -A -o wide
  377  kubectl -v=9 get pods -A -o wide
  378  kubectl -v=9 get pods -A -o wide | grep 'generateName|managedFields'
  379  kubectl -v=9 get pods -A -o wide | egrep 'generateName|managedFields'
  380  kubectl run myapp --image apache2
  381  kubectl run myapp1 --image apache2
  382  kubectl get pods -A -o wide
  383  kubectl get pods -A -o wide | grep 'my'
  384  kubectl scale -h
  385  kubectl scale deployment myapp --replicas=3
  386  kubectl get pods -A -o wide | grep 'my'
  387  kubectl -n default get deploy myapp
  388  kubectl -n default create deployment myapp --image=ubuntu/apache2:2.4-20.04_beta
  389  kubectl get pods -A -o wide | grep 'my'
  390  kubectl run mypod --image=nginx --restart=Never
  391  kubectl run mypod --image=apache2 --restart=Never
  392  kubectl run mypod1 --image=apache2 --restart=Never
  393  kubectl get pods -A -o wide | grep 'my'
  394  kubectl run mypod1 --image=ubuntu/apache2:2.4-20.04_beta --restart=Never
  395  kubectl run mypod2 --image=ubuntu/apache2:2.4-20.04_beta --restart=Never
  396  kubectl get pods -A -o wide | grep 'my'
  397  kubectl get pods -A -o wide
  398  kubectl get pods -A -o wide | grep 'my'
  399  kubectl create deployment myapp --image=nginx
  400  kubectl create deployment myapp1 --image=nginx
  401  kubectl get pods -A -o wide | grep 'my'
  402  kubectl get pods,dp -A -o wide | grep 'my'
  403  kubectl get pods,deploy -A -o wide | grep 'my'
  404  kubectl get deploy -A -o wide | grep 'my'
  405  kubectl get deploy -A -o wide
  406  kubectl get deploy,rs,pod | grep my
  407  kubectl get deploy,rs,pod | grep 'my'
  408  kubectl get deployments
  409  kubectl get pods
  410  kubectl get po
  411  kubectl get pod
  412  kubectl get deploy -A -o wide
  413  kubectl get deploy -A -o wide | grep my
  414  kubectl delete pod myapp
  415  kubectl get deploy -A -o wide | grep my
  416  kubectl get pods -A -o wide | grep my
  417  kubectl delete pod myp*
  418  kubectl delete pod mypod
  419  kubectl delete pod mypod1
  420  kubectl get pods -A -o wide | grep my
  421  kubectl expose -h
  422  history
  423  ls -al
  424  pwd
  425  get deploy -A -o wide | grep my
  426  kubectl get pods -A -o wide | grep my
  427  kubectl delete pod my-first-pod
  428  kubectl get pods -A -o wide | grep my
  429  kubectl run my-first-pod --image stacksimplify/kubenginx:1.0.0
  430  kubectl get pods -A -o wide | grep my
  431  kubectl expose pod my-first-pod --type=NodePort --port=80 --name=my-first-service
  432  kubectl get svc -A -o wide | grep my
  433  kubectl get service
  434  clear
  435  kubectl get service
  436  kubectl get nodes -o wide
  437  kubectl expose pod my-first-pod --type=NodePort --port=81 --name=my-first-service2
  438  kubectl get nodes -o wide
  439  kubectl get service
  440  kubectl expose pod my-first-pod --type=NodePort --port=81 --target-port=80 --name=my-first-service3
  441  kubectl get service
  442  kubectl expose pod my-first-pod --type=NodePort --port=81 --target-port=8000 --name=my-first-service4
  443  kubectl get service
  444  kubectl expose pod my-first-pod --type=NodePort --target-port=80 --name=my-first-service5
  445  kubectl expose pod my-first-pod --type=NodePort --port=8000 --target-port=8000 --name=my-first-service6
  446  kubectl get service
  447  kubectl expose pod my-first-pod --type=NodePort --port=80 --target-port=80 --name=my-first-service7
  448  kubectl get service
  449  kubectl get po
  450  kubectl logs -h
  451  kubectl logs mypod1
  452  kubectl logs mypod2
  453  clear
  454  kubectl get po
  455  kubectl logs mypod2
  456  kubectl logs myapp1
  457  kubectl logs nginx
  458  kubectl logs my-first-pod
  459  kubectl logs -f my-first-pod
  460  kubectl get po
  461  clear
  462  kubectl get po
  463  kubectl exec -it my-first-pod -- /bin/bash
  464  kubectl exec -it myapp1 -- /bin/bash
  465  kubectl exec -it mypod2 -- /bin/bash
  466  clear
  467  kubectl get po
  468  kubectl exec -it whoami-b85fc56b4-75gbn -- /bin/bash
  469  kubectl exec -it whoami-b85fc56b4-75gbn
  470  kubectl exec -it whoami-b85fc56b4-75gbn -- /sh
  471  kubectl exec -it whoami-b85fc56b4-75gbn ls
  472  kubectl get po
  473  kubectl exec -it mypod2 ls
  474  kubectl exec -it mypod2 -- ls
  475  kubectl exec -it mypod2 -- env
  476  history
  477  kubectl get pod my-first-pod -o yaml
  478  cd wo*
  479  ls -al
  480  sudo vi ./backup.yaml
  481  ls -al
  482  kubectl apply -f ./backup.yaml
  483  kubectl get po
  484  kubectl get svc
  485  ls -al
  486  pwd
  487  kubectl get service my-first-service -o yaml
  488  sudo vi ./svcbkp.yaml
  489  ls -al
  490  kubectl apply -f ./svcbkp.yaml
  491  kubectl get svc
  492  sudo vi ./svcbkp.yaml
  493  kubectl apply -f ./svcbkp.yaml
  494  kubectl get svc
  495  ls -al
  496  sudo vi ./backup.yaml
  497  kubectl apply -f ./backup.yaml
  498  kubectl get po
  499  kubectl get all
  500  kubectl delete svc my-first-service2
  501  kubectl delete svc my-first-service3
  502  kubectl get all
  503  kubectl get deploy,rs,pod | grep my
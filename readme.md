
K8s(minikube) setup for https://github.com/panasyg/taskcafe

Requirements:
-Linux OS
-Installed: firewalld, kubernetes(minikube), git, daemonize.

/ git clone https://github.com/panasyg/taskcafe-k8s.git && cd taskcafe-k8s

/ kubectl apply -f ./ 

/ sudo firewall-cmd --permanent --zone=public --add-port=3333/tcp && sudo firewall-cmd --reload

/ kubectl port-forward --address=0.0.0.0 service/taskcafe-lb 3333:3333 &

http://your-vm-ip(or just localhost if locally):3333/

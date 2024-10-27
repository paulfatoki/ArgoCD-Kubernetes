# start your minkube by running the command below
minikube start

# the command above get ur single node cluster ready coipled with the kubernetes cli interface call kubectl

# now run the command below

minikube status

minikube
type: Control Plan
create ns argocd
install argocd on kubernetes cluster
#to install argo cd on kubernetes c;uster

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
to get the pods for argocd: kubectl get pods -n argocd
kubectl get svc -n argocd
argocd-server port fowarding 
to get password - kubectl -n argocd get secret argocd-initial-admin-secret -o yaml or
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
to create another pod - kubectl run web1  --image=nginx --dry-run=client -o yaml > pod.yaml
to create a pod kubectl apply -f pod.yaml
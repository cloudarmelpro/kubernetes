Kubernetes provides:
- Declarative Deployment
- Resource Management
- Resiliency and Self Healing
- Service Discovery and Networking
- Load Balancing
- Storage Orchestration
- Vendor Neutrality
- Horizontal Pod Autoscaling
- Configuration Management
- Rolling Updates
- Extensibility

kubectl
Kubectl config current-context
kubectl apply -f deployments.yaml

<!-- En live stream -->
kubectl logs pod—name -f
kubectl port-forward pod-name 8000:5001

<!-- L’importance de label, vous pouvz supprimer tout le pod dans un specifique label comme ca -->
kubectl delete pod -l 'app.kubernetes.io/app=grade-submission'

<!-- Logs container dans un pod si on a plusieur container -->
kubectl logs podname -c grade-submission-portal -f
kubectl delete pods --all

<!-- Port pour acceder l'application sur minikube -->
minikube service grade-submission-portal-service -n cours-tow --url

<!-- Set namespace Use to groupe resources and manage them in difference space -->
kubectl get pods
kubectl config set-context --current --namespace=grade-submission

<!-- Roulout, pour faire de come back -->
kubectl roulout ......
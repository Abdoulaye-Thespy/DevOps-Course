# Kubernetes
Un système d'orchestration de conteneurs bourré de fonctionnalités pour automatiser le déploiement de notre application
Nous permet de faire évoluer facilement notre application et d'expédier du nouveau code.
# Pods
Les conteneurs ont souvent besoin de communiquer entre eux. Il n'est pas rare de voir un déploiement impliquant quelques conteneurs à déployer.
Les pods de Kubernetes sont des abstractions de plusieurs conteneurs et sont également éphémères.
# Services
Les applications sont souvent déployées avec plusieurs replicas. Cela permet d'équilibrer les charges et de réaliser une mise à l'échelle horizontale.

Les Services sont une abstraction d'un ensemble de pods pour les exposer via un réseau.

# AWS EKS 
C'est un service que nous pouvons utiliser pour configurer Kubernetes.

Le fichier deployment.yaml est utilisé pour spécifier comment nos pods doivent être créés.

Le fichier service.yaml est utilisé pour spécifier comment nos pods sont exposés.

# Pour le deployment:

## Cluster Kubernetes avec Amazon EKS
1. Creer un cluster EKS
2. Configurez kubectl pour fonctionner avec votre cluster EKS
3. Utilisez kubectl pour charger le fichier deployment.yaml dans EKS
4. Utilisez kubectl pour charger le fichier service.yaml dans EKS
5. Utilisez kubectl pour confirmer votre deploiement
- Bind your cluster on EKS to kubectl
- kubectl apply - crée le déploiement et le service
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
- `kubectl get pods` shows the pods in the cluster.
- `kubectl describe services` shows services in a cluster.
`kubectl cluster-info` shows cluster info

`kubectl exec -it {pod_name} sh` to get in the pod and debug.

## Other container orchestration strategies
###  AWS ECS 
- Integrate well with AWS.
- Only available on AWS.
- Easy to setup.

###  AWS Fargate
- Outil AWS qui permet de rationaliser le déploiement de conteneurs vers ECS et EKS.

### Docker Swam
- Une option pour exécuter simplement le conteneur manuellement avec Docker. Parfois, il est tentant de choisir un outil tout nouveau qui peut conduire à des architectures trop compliquées.

# Reverse Proxy.
- Analogy in real world: A reverse proxy is like a front desk in a hotel, we can use it to contact electricians and IT persons in case we have a problem in our hotel room.
- Analogy in IT word: A front-end, communicates with and doesn't care what's behind the reverse proxy since the reverse proxy handles that one for it, and all it does is to communicate with the reverse proxy.

## setup reverse proxy in k8s 
- Ingress/Egress is similar to AWS security goups, all about which IP can access the ressources and on which port ?
## Self healing and and horizontal scaling
- kubectl autoscale deployment <NAME> --cpu-percent=<CPU_PERCENTAGE> --min=<MIN_REPLICAS> --max=<MAX_REPLICAS>
- kubectl get hpa

# Using logs

# Project:

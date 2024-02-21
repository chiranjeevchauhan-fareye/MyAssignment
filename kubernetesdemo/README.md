# Installation Steps (Running your first app on Kubernetes)

1. Start Colima with Kubernetes support enabled by running the command: `colima start --kubernetes`.

2. Deploy your Kubernetes resources by applying the configurations in the YAML files:
   - Apply the Pod configuration: `kubectl apply -f k8s-deployment.yaml`.
   - Apply the Service configuration: `kubectl apply -f k8s-service.yaml`.
5. Retrieve the IP address and NodePort for accessing your service:
   - Run: `kubectl get endpoints` and copy the IP address of Kubernetes (e.g., 192.168.5.1).
   - Run: `kubectl get service` and copy the NodePort for the `k8s-service`.
   - To check deployments  run `kubectl get deployments`
   -  To check pods  run `kubectl get pods`

6. Open your browser and navigate to the IP address and NodePort combination, e.g., `192.168.5.1:32140`.
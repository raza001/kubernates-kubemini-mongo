# Minikube and Kubernetes Setup Commands

This guide provides a list of commands to install necessary tools, set up a Minikube cluster, deploy applications, and manage Kubernetes resources.

---

## Prerequisites

1. **Install kubectl**  
   ```bash
   brew install kubectl
   ```

2. **Install Minikube**  
   ```bash
   brew install minikube
   ```

---

## Starting Minikube and Deploying Resources

1. **Start Minikube**  
   ```bash
   minikube start
   ```

2. **Check Pods Status**  
   ```bash
   kubectl get pod
   ```

3. **Apply Configurations and Deployments**  
   ```bash
   kubectl apply -f mongo-config.yaml
   kubectl apply -f secret.yaml
   kubectl apply -f mongo-app.yaml
   kubectl apply -f web-app.yaml
   ```

4. **Check Pods and Other Resources**  
   ```bash
   kubectl get pod
   kubectl get configmap
   kubectl get secret
   kubectl get svc
   ```

5. **Retrieve Minikube's IP**  
   ```bash
   minikube ip
   ```

6. **Get Node Details**  
   ```bash
   kubectl get node -o wide
   ```

7. **Access the Web Application Service**  
   ```bash
   minikube service webapp-service
   ```

---

## Cleanup Commands

1. **Delete All Deployments**  
   ```bash
   kubectl delete deployment --all
   ```

2. **Delete All Secrets**  
   ```bash
   kubectl delete secret --all
   ```

---

## Notes

- Ensure Minikube is running before deploying any resources.
- Use `kubectl get <resource>` to monitor the status of your deployments and services.
- You can access services exposed by Minikube using the `minikube service` command.

---

Happy Coding!

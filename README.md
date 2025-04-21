# MyProject
# Java App on Kubernetes 🚀

This project demonstrates how to:

✅ Build a Java application  
✅ Containerize it using Docker  
✅ Deploy it to a Kubernetes cluster  
✅ Expose it using a LoadBalancer  
✅ Access it successfully from a local machine

---

## 🛠️ Tech Stack

- Java (Spring Boot or plain Java)
- Docker
- Kubernetes (Minikube / EKS / GKE / AKS)
- kubectl
- LoadBalancer Service

---

## 📦 Step-by-Step Setup

 1. Clone the Repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

2. Build the Java App

javac App.java   # or use `mvn clean package` if it's a Maven project
java App.java    # run to verify

3. Create Docker Image

docker build -t java-app .
docker images   # to verify the image is created

4. Push to DockerHub (optional)

docker tag java-app your-dockerhub-username/java-app
docker push your-dockerhub-username/java-app

5. Deploy to Kubernetes
kubectl apply -f k8s/deployment.yaml

6. Expose with LoadBalancer

kubectl apply -f k8s/service.yaml
kubectl get svc   # Note the external IP

7. Access the App
http://<external-ip>:<port>

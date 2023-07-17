# Kubernetes_Ingress
The NGINX Ingress Controller for Kubernetes works with the NGINX webserver (as a proxy).

COMMANDS TO FOLLOW: - (WITH USING NGINX Ingress Controller)

STEP 1 - Change your Kubectl config to docker desktop.

a) kubectl config get-contexts

b) kubectl config use-context docker-desktop

STEP 2 - Applying ingress-nginx Controller to proceed.
To deploy the NGINX Ingress Controller, run the command:
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.0.0/deploy/static/provider/cloud/deploy.yaml

STEP 3 - Now, Run basic commands.

a)Apply your deployment YAML file by running 
kubectl apply -f deployment.yaml

b)Check the deployment status by running: 
kubectl get deployment -n ingress-nginx

c)List all pods in all namespaces related to the Ingress-Nginx controller by running:
kubectl get pods --all-namespaces -l app.kubernetes.io/name=ingress-nginx

d)Apply the service YAML file by running:
kubectl apply -f service.yaml

e)Apply the ingress YAML file by running:
kubectl apply -f ingress.yaml

f)Check the created Ingress resources by running:
kubectl get ing -n ingress-nginx

STEP 4 - Lastly, Open Powershell -> Run following commands and edit your host file.

a) cd driver

b) cd etc

c) notepad.exe hosts

d) Add your xyz.com below in the host file like this

![image](https://github.com/JaislinBajwa/Kubernetes_Ingress/assets/89400877/83e709a5-153a-4d23-8b67-eb44dacd1803)




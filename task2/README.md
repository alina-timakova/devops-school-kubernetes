**Task 2**

ConfigMap & Secrets
![image](https://user-images.githubusercontent.com/67266752/152607851-a87a99ad-6e83-446b-9cc1-137e40aaf00f.png)

Check env in pod
![image](https://user-images.githubusercontent.com/67266752/152608120-f0e90515-6cf3-4188-8487-b00cdf1b8fb6.png)

Create deployment with simple application
![image](https://user-images.githubusercontent.com/67266752/152610020-bc2cb349-9d26-43dc-8b51-5d8ee28dfbca.png)

Get pod ip address
![image](https://user-images.githubusercontent.com/67266752/152610482-0c518663-9222-4c62-bfb9-c8e7959298a7.png)

Try connect to pod with curl (curl pod_ip_address)
![image](https://user-images.githubusercontent.com/67266752/152615139-e016213d-6510-4bd2-8e41-7bf33cf4e671.png)

From you PC - not reachable

From minikube:
![image](https://user-images.githubusercontent.com/67266752/152616753-44fac21c-768e-4092-a08f-44db94017121.png)

From another pod:
![image](https://user-images.githubusercontent.com/67266752/152707452-1f96a578-c112-47d4-99c6-8dc180758f4f.png)

**Create service (ClusterIP)**

Create and apply a manifest
![image](https://user-images.githubusercontent.com/67266752/152807341-cf811732-6f68-4e4b-88ec-a203c0aedadf.png)
![image](https://user-images.githubusercontent.com/67266752/152807594-13379705-a576-4840-a35c-799b385e41be.png)

Try connect to service (curl service_ip_address). What happens? connection timed out
![image](https://user-images.githubusercontent.com/67266752/152808405-73a7c459-a290-4444-bdab-2677f6d5e795.png)

From you PC - unreachable

From minikube (minikube ssh) (run the command several times)
![image](https://user-images.githubusercontent.com/67266752/152809679-9c62fb96-c238-479d-9a18-98b193ee3cce.png)

From another pod (kubectl exec -it $(kubectl get pod |awk '{print $1}'|grep web-|head -n1) bash) (run the command several times)
![image](https://user-images.githubusercontent.com/67266752/152809077-9bf9e995-461f-4425-84e8-c4174b628c00.png)

**NodePort:**

![image](https://user-images.githubusercontent.com/67266752/152810949-14f9334c-51d7-4721-8215-68e479fb1a97.png)

Checking the availability of the NodePort service type - available
![image](https://user-images.githubusercontent.com/67266752/152811479-15c868e3-4109-4bca-80db-e62cedd025d3.png)

**Headless service**
![image](https://user-images.githubusercontent.com/67266752/152811730-1374938b-1433-4f8e-a202-8f4f0cd64fd8.png)

**DNS**
Connect to any pod cat /etc/resolv.conf
![image](https://user-images.githubusercontent.com/67266752/152890990-8d912317-64b5-45d2-ac61-5e6e8ac389cb.png)

Pod with dnsutils has been created:
![image](https://user-images.githubusercontent.com/67266752/152890879-a07eaaa7-4575-4af4-bdc6-02ba2cc69613.png)

DNS service of the cluster
![image](https://user-images.githubusercontent.com/67266752/152891108-d9ed4cc9-e4fc-41d7-9acc-ee2526257616.png)

Run nslookup to normal clusterip and headless
![image](https://user-images.githubusercontent.com/67266752/152891394-7389c889-31f9-4c96-8af5-b19ada55a8da.png)

**Ingress**

![image](https://user-images.githubusercontent.com/67266752/152866027-e9f13230-0410-4aeb-97ea-af82a247b8eb.png)

![image](https://user-images.githubusercontent.com/67266752/152866628-a882f399-de8b-4510-8b46-ab0466fd5f9a.png)


**Homework**

- In Minikube in namespace kube-system, there are many different pods running. Your task is to figure out who creates them, and who makes sure they are running (restores them after deletion).

Running pods in kube-system namespace
![image](https://user-images.githubusercontent.com/67266752/152867631-c2501955-86e4-42f9-b62c-06b8df4513ac.png)

Kubelet make sure that control plane components which are etcd,kube-apiserver,kube-controller-manager and kube-scheduler running as pod.

- Implement Canary deployment of an application via Ingress. Traffic to canary deployment should be redirected if you add "canary:always" in the header, otherwise it should go to regular deployment. Set to redirect a percentage of traffic to canary deployment.




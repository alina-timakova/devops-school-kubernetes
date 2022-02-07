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

# devops-school-kubernetes
kubectl and minikube are installed on dv3 VM located in Azure (Nested virtualization is supported in the Dv3 and Ev3 series of Azure virtual machines)

Verify kubectl installation:
![image](https://user-images.githubusercontent.com/67266752/152444764-ead85567-b8df-48dd-a62e-3575bff821d2.png)

Setup autocomplete for kubectl:
![image](https://user-images.githubusercontent.com/67266752/152444571-31b44d68-5a3d-404d-b05e-881c27e049af.png)

Get information about cluster:
![image](https://user-images.githubusercontent.com/67266752/151454115-f6f4d58b-24bd-4ba5-85f7-c7b19c587b58.png)

get information about available nodes:
![image](https://user-images.githubusercontent.com/67266752/151454272-b4e10ed8-78cb-4910-bcd1-d79745ef4c6c.png)

Installed Kubernetes Dashboard, worked only after kubectl delete clusterrolebinding kubernetes-dashboard

Check kubernetes-dashboard ns:
![image](https://user-images.githubusercontent.com/67266752/151457143-39ba40ee-1457-4a98-b375-08114166b490.png)

Installed Metrics Server and updated deployment

Connected to Dashboard (configured tunnel settings in putty)
![image](https://user-images.githubusercontent.com/67266752/152445671-53c5a46c-4f29-4c09-a202-df0e6096277b.png)


Task 1.2

pod created
![image](https://user-images.githubusercontent.com/67266752/152446075-b4690344-46f2-4d99-bb66-e022ad6c14d4.png)

![image](https://user-images.githubusercontent.com/67266752/152446011-4a9e5022-c3a6-40cd-aafa-539cc41eeb43.png)

Apply manifests (download from repository):
![image](https://user-images.githubusercontent.com/67266752/152447008-cddd4a4e-6745-46f6-90f1-63e5722ee519.png)

Deployment "nginx-deployment" has been created
![image](https://user-images.githubusercontent.com/67266752/152451551-58b8e964-3ecd-42cb-8e12-3412d682d02e.png)

When I deleted 1 pod I saw another one immidiately created
![image](https://user-images.githubusercontent.com/67266752/152451651-415c5ef1-13d2-4221-8717-8eb8d35dd287.png)










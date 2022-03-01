Create pv in kubernetes
![image](https://user-images.githubusercontent.com/67266752/155038981-7485cfc0-df6e-4dc5-9c39-458e19c8b71d.png)

Create pvc
![image](https://user-images.githubusercontent.com/67266752/155039170-3f87ccb4-849f-4114-85cb-4c9e730c0276.png)

Apply deployment minio
![image](https://user-images.githubusercontent.com/67266752/155039418-42323b3d-fe3c-48c1-9c2c-afd3c34220fa.png)

Apply svc nodeport
![image](https://user-images.githubusercontent.com/67266752/155629810-6f2a6fb2-c356-4f7b-ac40-aa6a76d50f4c.png)

nodeport available
![image](https://user-images.githubusercontent.com/67266752/155629990-34c85dbc-7a60-4bb5-b4fa-142ffdab8ac3.png)

Check pod and statefulset
![image](https://user-images.githubusercontent.com/67266752/155630185-7b4f5c60-2a9d-4c42-8681-82c403c443b9.png)

**Homework**
- We published minio "outside" using nodePort. Do the same but using ingress.
- Publish minio via ingress so that minio by ip_minikube and nginx returning hostname (previous job) by path ip_minikube/web are available at the same time.

Ingress controller already exists
![image](https://user-images.githubusercontent.com/67266752/155630422-98175e73-413f-4c45-b8c6-61cb27d68583.png)

ip_minikube
![image](https://user-images.githubusercontent.com/67266752/156204551-6acba018-34d2-4b13-aea4-5d190c456c39.png)

ip_minikube/web
![image](https://user-images.githubusercontent.com/67266752/156203880-e5a587f4-7575-4dcc-a032-a2755b97e250.png)

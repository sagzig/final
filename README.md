# John Bryce Final Project
Part one:

Question 1: Deploy a pod named nginx-pod using the nginx:alpine image.
Name: nginx-pod-yourname
Image: nginx:alpine.

Solution: 
![image](https://user-images.githubusercontent.com/31998392/126076028-619f92a3-eef0-47e3-b0de-655503385896.png)

Question 2: Deploy a messaging pod using the redis:alpine image with the labels set to tier=msg.
Pod Name: messaging
Image: redis:alpine
Labels: tier=msg

Solution: ![image](https://user-images.githubusercontent.com/31998392/126076060-9f220edb-8668-4128-aa3a-6812b9b13c46.png)

Question 3: Create a namespace named apx-x998-yourname

Solution: ![image](https://user-images.githubusercontent.com/31998392/126076089-27db84c4-a4db-47e6-a8a5-74da90ee347f.png)

Question 4: Get the list of nodes in JSON format and store it in a file at /tmp/nodes-yourname

Solution: ![image](https://user-images.githubusercontent.com/31998392/126076102-f0bea894-01a0-47fc-87ac-4a560672f5df.png)

Question 5: Create a service messaging-service to expose the messaging application within the
cluster on port 6379.
a. Use imperative commands - kubectl
b. Service: messaging-service
c. Port: 6379
d. Type: ClusterIp
e. Use the right labels

Solution: ![image](https://user-images.githubusercontent.com/31998392/126076167-9a991bd1-512e-44ab-bcea-824a093a6c8d.png)

Question 6: Same question as question 5.

Question 7: Create a deployment named hr-web-app using the image kodekloud/webapp-color with 2 replicas
a. Name: hr-web-app
b. Image: kodekloud/webapp-color
c. Replicas: 2

Solution: ![image](https://user-images.githubusercontent.com/31998392/126076188-8b3ccfc1-5ac1-4872-8627-544df7cf973d.png)

Question 8: Create a static pod named static-busybox on the master node that uses the busybox image and the command sleep 1000
a. Name: static-busybox
b. Image: busybox
c. Replicas: 2

Solution: ![image](https://user-images.githubusercontent.com/31998392/126076221-348833df-e448-48e3-9500-e7165af30061.png)


Qutestion 9: Create a POD in the finance-yourname namespace named temp-bus with the image
redis:alpine
a. Name: temp-bus
b. Image Name: redis:alpine

Solution: 
Creating the namespace:
![image](https://user-images.githubusercontent.com/31998392/126076859-0dc49d3d-4d92-448e-a717-b413d56a66d6.png)

Creating a pod with the namespace:

![image](https://user-images.githubusercontent.com/31998392/126076877-543228c9-b874-421e-98fe-5fbe3263fe0b.png)


Question 10: Create a Persistent Volume with the given specification
a. Volume Name: pv-analytics
b. Storage: 100Mi
c. Access modes: ReadWriteMany
d. Host Path: /pv/data-analytics

Solution:
![image](https://user-images.githubusercontent.com/31998392/126077005-968ad58c-1251-468b-a0d3-968aa03e589f.png)

Check that it's created successfully:

![image](https://user-images.githubusercontent.com/31998392/126077017-3f645b80-4249-47a7-8d55-7878eba2425a.png)



PV YAML File(pv-volume.yaml) here - https://github.com/sagzig/final/blob/main/pv-volume.yaml
PV-Claim YAML File(pv-claim.yaml) here- https://github.com/sagzig/final/blob/main/pv-claim.yaml


Question 11: Create a Pod called redis-storage-yourname with image: redis:alpine with a Volume of type emptyDir that lasts for the life of the Pod. 
specs:
a. Pod named 'redis-storage-yourname'
b. Pod 'redis-storage-yourname' uses Volume type of emptyDir
c. Pod 'redis-storage-yourname' uses volumeMount with mountPath =
/data/redis

Solution:

![image](https://user-images.githubusercontent.com/31998392/126077101-5880b61b-f44b-4946-8d45-7f596578e98c.png)

Create pod YAML File(pv-pod-new.yaml) here - https://github.com/sagzig/final/blob/main/pv-pod-new.yaml


Question 12: Create this pod and attached it a persistent volume called pv-1
a. Make sure the PV mountPath is hostbase : /data

Solution:

Creating a persistent volume:
![image](https://user-images.githubusercontent.com/31998392/126077435-eb093661-aab3-4362-aba1-0d3c15f5928c.png)

Creating a pod and attaching the pv to it:
![image](https://user-images.githubusercontent.com/31998392/126077336-4446ea2c-8baf-4ab4-a80c-584000a0e444.png)

Create pod file (createpod.yaml) here- https://github.com/sagzig/final/blob/main/createpod.yaml
Create volume file (createvol.yaml) here- https://github.com/sagzig/final/blob/main/createvol.yaml


Question 13: Create a new deployment called nginx-deploy, with image nginx:1.16 and 1 replica.
Record the version. Next upgrade the deployment to version 1.17 using rolling update. 
Make sure that the version upgrade is recorded in the resource annotation.
a. Deployment : nginx-deploy. Image: nginx:1.16
b. Image: nginx:1.16
c. Task: Upgrade the version of the deployment to 1:17
d. Task: Record the changes for the image upgrade

Solution:
![image](https://user-images.githubusercontent.com/31998392/126077586-2b9c7eee-c535-4d08-9c10-f9fb4f638999.png)

Question 14: Create an nginx pod called nginx-resolver using image nginx, expose it internally with a service called nginx-resolver-service.
Test that you are able to look up the service and pod names from within the cluster.
Use the image: busybox:1.28 for dns lookup.
Record results in /root/nginx-yourname.svc and /root/nginx-yourname.pod

Solution:
![image](https://user-images.githubusercontent.com/31998392/126077751-1416b727-7c21-4649-9ec1-be58f2000be4.png)

Createing a service File(createservice-q14.yaml) here- https://github.com/sagzig/final/blob/main/createaservice-q14.yaml

Question 15: Create a static pod on node01 called nginx-critical with image nginx. 
Create this pod on node01 and make sure that it is recreated/restarted automatically in case of a failure.

Solution: 


Question 16: Create a pod called multi-pod with two containers. Container 1, name: alpha, image: nginx
Container 2: beta, image: busybox, command sleep 4800.
a. Environment Variables:
i. container 1:
ii. name: alpha
iii. Container 2:
iv. name: beta

Solution: 
![image](https://user-images.githubusercontent.com/31998392/126077873-d6cf7f87-32a4-41fb-953e-6f888cee6379.png)

Pod creation YAML File(multipod.yaml) here - https://github.com/sagzig/final/blob/main/multipod.yaml

_________________________________________________________________________________________________________________________________________________________________


Part 2




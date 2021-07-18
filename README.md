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

Solution: 
![image](https://user-images.githubusercontent.com/31998392/126076060-9f220edb-8668-4128-aa3a-6812b9b13c46.png)

Question 3: Create a namespace named apx-x998-yourname

Solution:
![image](https://user-images.githubusercontent.com/31998392/126076089-27db84c4-a4db-47e6-a8a5-74da90ee347f.png)

Question 4: Get the list of nodes in JSON format and store it in a file at /tmp/nodes-yourname

Solution:
![image](https://user-images.githubusercontent.com/31998392/126076102-f0bea894-01a0-47fc-87ac-4a560672f5df.png)

Question 5: Create a service messaging-service to expose the messaging application within the
cluster on port 6379.
a. Use imperative commands - kubectl
b. Service: messaging-service
c. Port: 6379
d. Type: ClusterIp
e. Use the right labels

Solution: 
![image](https://user-images.githubusercontent.com/31998392/126076167-9a991bd1-512e-44ab-bcea-824a093a6c8d.png)

Question 6: Same question as question 5.

Question 7: Create a deployment named hr-web-app using the image kodekloud/webapp-color with 2 replicas
a. Name: hr-web-app
b. Image: kodekloud/webapp-color
c. Replicas: 2

Solution: 
![image](https://user-images.githubusercontent.com/31998392/126076188-8b3ccfc1-5ac1-4872-8627-544df7cf973d.png)

Question 8: Create a static pod named static-busybox on the master node that uses the busybox image and the command sleep 1000
a. Name: static-busybox
b. Image: busybox
c. Replicas: 2

Solution:
![image](https://user-images.githubusercontent.com/31998392/126076221-348833df-e448-48e3-9500-e7165af30061.png)


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

Question 1: Type the command for: Get pods with label information

Solution: kubectl get pods --show-labels

Question 2: Create 5 nginx pods in which two of them is labeled env=prod and three of them is labeled env=dev

Creation of 2 pods labeled env=prod YAML File(2pods.yaml) here- https://github.com/sagzig/final/blob/main/2pods.yaml
Creation of 3 pods labeled env=dev YAML File(3pods.yaml) here- https://github.com/sagzig/final/blob/main/3pods.yaml

Question 3: Verify all the pods are created with correct labels

Solution: 
![image](https://user-images.githubusercontent.com/31998392/126078040-f213decf-19ee-4da8-9327-d02357debc64.png)

Question 4: Get the pods with label env=dev

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078049-9d754c93-1897-4d86-8af9-ed3c42709eac.png)

Question 5: Get the pods with label env=dev and also output the labels

Solution: ![image](https://user-images.githubusercontent.com/31998392/126078054-07079457-594e-4e06-b940-a169877b9f4a.png)

Question 6: Get the pods with label env=prod

Solution: 
![image](https://user-images.githubusercontent.com/31998392/126078065-a105ebcc-47f2-4db6-a165-18cd92c202e1.png)

Question 7: Get the pods with label env=prod and also output the labels

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078091-e61c0438-f9b5-4ab9-ba0d-d42430b44f9d.png)


Question 8: Get the pods with label env

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078096-944faf99-4feb-4192-913c-1e3b788bc99f.png)


Question 9: Get the pods with labels env=dev and env=prod

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078101-cb0ec539-eea5-4570-bb16-1d71f412f699.png)


Question 10: Get the pods with labels env=dev and env=prod and output the labels as well

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078111-91fb2952-534d-4776-8d44-329763c1523d.png)


Question 11: Change the label for one of the pod to env=uat and list all the pods to verify

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078115-53c567a0-ddca-4d21-af99-d39abca5028f.png)


Question 12: Remove the labels for the pods that we created now and verify all the labels are removed

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078125-622c325d-a2c9-4bda-a6ac-172468d54c9f.png)


Question 13: Let’s add the label app=nginx for all the pods and verify (using kubectl)

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078132-c2549204-75cf-4f3b-870e-306bb99ba939.png)


Question 14: Get all the nodes with labels (if using minikube you would get only master node)

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078135-42909d48-27a9-433e-909d-fc32495f9c2b.png)


Question 15: Label the worker node nodeName=nginxnode

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078139-b3bf0dcd-29fe-4d73-b985-731ef8a29957.png)

Question 16: Create a Pod that will be deployed on the worker node with the label nodeName=nginxnode

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078152-e0048167-c431-4b6c-986e-d3f768bc9b58.png)

Create a pod YAML File(question16.yaml) here- https://github.com/sagzig/final/blob/main/question16.yaml

Question 17:  Verify the pod that it is scheduled with the node selector on the right node... fix it if it’s not behind scheduled.

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078192-4727254e-12ec-4905-a68d-65fb4c107efe.png)


Question 18: Verify the pod nginx that we just created has this label

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078194-2eaf4a9d-4b0b-4dad-8bf6-7443201656d8.png)



_________________________________________________________________________________________________________________________________________________________________


Part 3


Question 1: Create a deployment called webapp with image nginx with 5 replicas
a. Use the below command to create a yaml file.
i. kubectl create deploy webapp --image=nginx --dry-run -o yaml > webapp.yaml
ii. Edit it and add 5 replica’s

Solution:

1.a:
Editing the file

![image](https://user-images.githubusercontent.com/31998392/126078229-df695914-89eb-45dd-9fab-5ca324a2e5fc.png)

1.b:

Checking replicas added 

![image](https://user-images.githubusercontent.com/31998392/126078243-8156a5cb-247b-4346-988e-cfac0556300b.png)

Question 2: Get the deployment rollout status

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078274-db2c6478-6e25-4e50-99ee-1c0ece903dbb.png)

Question 3: Get the replicaset that created with this deployment

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078283-33206b70-94b6-4b14-88b5-d268d8867de6.png)


Question 4: EXPORT the yaml of the replicaset and pods of this deployment

Solution:
YAML File of the replicaset here - https://github.com/sagzig/final/blob/main/replicaset.yaml
YAML File of the Pods here - https://github.com/sagzig/final/blob/main/exportpods.yaml

Question 5: Delete the deployment you just created and watch all the pods are also being deleted

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078611-ce6f7d8f-8659-4e6d-b1e0-3aa745d2399d.png)


Question 6: Create a deployment of webapp with image nginx:1.17.1 with container port 80 and verify the image version
a. kubectl create deploy webapp --image=nginx:1.17.1 --dry-run -o yaml > webapp.yaml
b. add the port section (80) and create the deployment

Solution:

6.a:
Building the configuration and editing the file:
![image](https://user-images.githubusercontent.com/31998392/126078635-3096bd63-e52a-4e61-ae33-d48b61be1b92.png)

6.b: 
Running the file after editing and verifying the port 80 attached:
![image](https://user-images.githubusercontent.com/31998392/126078661-581e2609-b1c8-4766-9c9c-a4a3cc635a1e.png)


Question 7: Update the deployment with the image version 1.17.4 and verify

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078679-e78ce63e-847e-4c15-89ee-0a46c1bba6c7.png)


Question 8: Check the rollout history and make sure everything is ok after the update

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078682-f3e5775b-4f5f-4881-b7c9-7a3864e1cf2a.png)

Question 9: Undo the deployment to the previous version 1.17.1 and verify Image has the previous version

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078684-54777f0f-cb63-4773-b4a9-c71111a78060.png)


Question 10: Update the deployment with the wrong image version 1.100 and verify something is wrong with the deployment
a. Expect: kubectl get pods (ImagePullErr)
b. Undo the deployment with the previous version and verify everything is Ok
c. kubectl rollout history deploy webapp --revision=7
d. Check the history of the specific revision of that deployment
e. update the deployment with the image version latest and check the history
and verify nothing is going on

Solution:

10.a:
![image](https://user-images.githubusercontent.com/31998392/126078754-12319e28-0620-481e-84a5-fba05402e448.png)


10.b:
![image](https://user-images.githubusercontent.com/31998392/126078769-c729e8c5-28c0-44b3-97a3-7aeea6920c82.png)

10.c:
![image](https://user-images.githubusercontent.com/31998392/126078787-8deb94ad-c38d-4d8f-a31e-72c0be0295f6.png)

10.d:
![image](https://user-images.githubusercontent.com/31998392/126078791-b1f2cb84-ca4f-49a2-ae6f-f28eab7f68f4.png)

10.e:
![image](https://user-images.githubusercontent.com/31998392/126078799-3f822544-f73a-48d9-a9a5-729eb3a29ef6.png)


Question 11: Apply the autoscaling to this deployment with minimum 10 and maximum 20 replicas and target CPU of 85% and verify hpa is created and replicas are increased to 10 from 1


Solution:
![image](https://user-images.githubusercontent.com/31998392/126078808-6edbb323-cfe6-4287-a31d-19e666660dbd.png)


Question 12: This question does not exists


Question 13: Clean the cluster by deleting deployment and hpa you just created

Solution:
![image](https://user-images.githubusercontent.com/31998392/126078816-84f7c8a6-e3bb-43c6-af67-96dcafa99532.png)


Question 14: Create a job and make it run 10 times one after one (run > exit > run >exit ..) using the following configuration:
kubectl create job hello-job --image=busybox --dry-run -o yaml -- echo "Hello I am from job" > hello-job.yaml”
a. Add to the above job completions: 10 inside the yaml


Solution:
Editing the file and edditng the "completion:10" into it:

![image](https://user-images.githubusercontent.com/31998392/126078826-4bae7e86-767d-4419-a81e-89a3d8a69f9c.png)

_________________________________________________________________________________________________________________________________________________________________


Part 4

Question 1: Create a file called config.txt with two values key1=value1 and key2=value2 and verify the file

Solution:
I ran the given commands and received the file:
![image](https://user-images.githubusercontent.com/31998392/126078864-cde67e2e-b80c-4a95-85a5-238d9c2723bc.png)


Question 2: Create a configmap named keyvalcfgmap and read data from the file config.txt and verify that configmap is created correctly

Solution:
Creating the ConfigMap:
![image](https://user-images.githubusercontent.com/31998392/126078895-cd6bceda-3acd-44a2-a0c3-58973a098c26.png)


Question 3: Create an nginx pod and load environment values from the above configmap keyvalcfgmap and exec into the pod and verify the environment variables and delete the pod
// first run this command to save the pod yml
kubectl run nginx --image=nginx --restart=Never --dry-run -o yaml > nginx-pod.yml

Solution:
Editing the given file:
![image](https://user-images.githubusercontent.com/31998392/126079025-7bffa4ef-7db0-4f14-9c1e-7e9943315452.png)

Running the file and checking that it's built with the ConfigMap:
![image](https://user-images.githubusercontent.com/31998392/126078933-65265239-cd73-4d59-b856-182bdab75904.png)

The File(nginx-pod) used to created to pod after editing, here- https://github.com/sagzig/final/blob/main/nginx-pod.yml

# OpenShiftCourse


# Resources we are going to see

# openshift has 2 planes in its architecure. 
# 1) control plane
# 2) data plane

# below image shows what are the tasks both the planes are performing individually


![image](https://user-images.githubusercontent.com/80065996/155132033-41454976-9d10-4e4e-8b83-1aa6c0437675.png)


![image](https://user-images.githubusercontent.com/80065996/155132119-71404e5f-3be6-4875-a344-740c79af3433.png)


![image](https://user-images.githubusercontent.com/80065996/155154656-50bfa4b7-2908-4b88-aefd-83d2bc8a8d81.png)


![image](https://user-images.githubusercontent.com/80065996/155154783-f8f61e64-a63f-41bf-8efc-9e2ce85ddf59.png)


![image](https://user-images.githubusercontent.com/80065996/155155029-890e2fad-19ae-44ef-acd3-7fe317431483.png)


# kubernetes administrators are responsible for maintaining both 'control plane' and 'data plane'
# As a developer, your responsibility is to interact with 'REST API' in the control plane to deploy your applications


![image](https://user-images.githubusercontent.com/80065996/155155830-cf58c679-39b8-4286-a39a-b5315ba4fb38.png)


![image](https://user-images.githubusercontent.com/80065996/155156242-51cb7a03-f5b2-45e0-b357-a75035b6b91d.png)


# CONCEPT := OPENSHIFT COMMAND LINE INTERFACE - 'OC' tool. it is wrapper created on top of 'kubectl' command line tool from kubernetes


# Example of running a simple example using 'OC' command to run jenkins in the openshift cluster


![image](https://user-images.githubusercontent.com/80065996/155157755-07dac533-d01f-4db6-b056-5cdf4f30f57b.png)


![image](https://user-images.githubusercontent.com/80065996/155157839-3d67b1c2-d84a-441b-ae66-cce8b8f03e22.png)


# open the URL given to us in the command line after started the jenkins, use this URL in browser to see the jenkins up and running


![image](https://user-images.githubusercontent.com/80065996/155158121-40ec775a-af3f-407a-b0d1-e16ecc5c2eea.png)


# course Overview


![image](https://user-images.githubusercontent.com/80065996/155158426-93cb345b-9a17-45b8-963e-4aacc3115115.png)


![image](https://user-images.githubusercontent.com/80065996/155158540-6224488a-05e9-4cdb-85ec-069820782e9c.png)


# we are going to use simple hello-world application using 'oc' command line



# using command line is the best way of learning openshift. Only Ops team will make use of webconsole to monitor the openshift cluster. developers mostly use 
# command line tool 'OC'


![image](https://user-images.githubusercontent.com/80065996/155264324-df84df04-91fb-4d29-b199-153ab02b6b6c.png)


# main use of terminal 'OC' - WE CAN AUTOMATE THE TASKS USING SHELL SCRIPT.BUT IN WEB CONSOLE WE CANNOT DO THE AUTOMATION


![image](https://user-images.githubusercontent.com/80065996/155264462-d320995c-aae1-486b-b08d-a48505418cee.png)


# BASIC LINUX KNOWLEDGE NEEDED


![image](https://user-images.githubusercontent.com/80065996/155264550-6615ac67-baea-4068-a704-4203686506e8.png)


![image](https://user-images.githubusercontent.com/80065996/155264697-627ec1f2-661c-4184-82ba-824fb59521c7.png)


# Installation:


![image](https://user-images.githubusercontent.com/80065996/155265260-dfd3005b-2850-44db-ade9-79adf1279850.png)


# We are planning to use Redhat hosted sandbox for our learning purpose
# we can create account in redhat site and use the sandbox. Sandbix will come with all the setup for openshoft cluster.
# we have to reinstall the cluster once in every 35 days. That is the only problem.
# Once sandbox is set up, we have to download the command line ('oc') from the cluster itself


![image](https://user-images.githubusercontent.com/80065996/155269990-2a316fc3-c510-48e4-a6ea-601443c6241f.png)


# Once downloaded unzip the folder and set the 'environment variable'(user variable) for this path.

# open the 'windows powershell' as the adminstrator type 'oc'


![image](https://user-images.githubusercontent.com/80065996/155270110-3fdbae49-45aa-40b3-8f1e-6ba246395765.png)


# click the 'copy login command' as highlighted below


![image](https://user-images.githubusercontent.com/80065996/155270203-256676e9-4c98-4468-bf03-c77367c35242.png)


# you will get API token,


![image](https://user-images.githubusercontent.com/80065996/155270305-49b267df-766d-4ede-8348-277f0d817011.png)


# use this API Token to login into the openshift cluster running inside the sandbox,


![image](https://user-images.githubusercontent.com/80065996/155270358-ac271173-c4e2-4fc2-97f9-4c1c9af50679.png)


# clone the below git repository from the gitlab. this repo is going to get used throughout the complete tutorial of openshift


![image](https://user-images.githubusercontent.com/80065996/155270463-1d38e14c-893d-4b64-b1e8-c6e0330cfca4.png)


# open accounts in 
# 1)quay.io - for image stream repository
# 2)gitlab - hosted repository for github repos


# Note: Docker image can be pushed to 'Docker hub','artifactory','quay.io'. it purely depends on the project


![image](https://user-images.githubusercontent.com/80065996/155274410-8601975f-d282-4096-9548-1a08a10f7b0d.png)


# Note: When your docker image repository is in 'Dockerhub', then we can mention only the image name frmo Dockerhub.
# When you docker image is in 'quay.io', then we have to mention complete path of the image name like shown below,


![image](https://user-images.githubusercontent.com/80065996/155276851-8484e092-5387-46f9-b377-cd41d3999fd1.png)


# ports


![image](https://user-images.githubusercontent.com/80065996/155277650-e37aff5a-6da4-4bca-922a-8439afd22536.png)


![image](https://user-images.githubusercontent.com/80065996/155277676-bf7a8a79-e875-4066-8f76-85d19d61d14f.png)


# see the full command below to set the port
# host port can be anything (host is the EC2 machine in which container is running). continaer port is the one in which application port used in the code listening to
# in our case, golang API server running inside the container exposed in port '8080'


![image](https://user-images.githubusercontent.com/80065996/155277859-2b2e7035-7b47-44b4-9fe4-d8154665f86c.png)


# Base image


![image](https://user-images.githubusercontent.com/80065996/155281058-64d28a89-cf73-495e-8fcf-b6d7bb858bd1.png)


# Dockerfile for simple golang API server app


![image](https://user-images.githubusercontent.com/80065996/155281531-78b17f65-11c7-4b84-9074-e571f205fa56.png)



# Environment variable set up
# in below screenshot, we are setting the value to the environment variable names 'Message' with a big string message 


![image](https://user-images.githubusercontent.com/80065996/155282038-98ec55ee-1d58-42cb-865d-4d36c0c6b7d3.png)


# 'oc' commands


![image](https://user-images.githubusercontent.com/80065996/155554277-0c5999c9-fc6b-4980-af9c-f4bf0cf77286.png)


![image](https://user-images.githubusercontent.com/80065996/155554349-f4b4d3c0-fdc3-49d2-87ef-ee34ce3e3b86.png)


![image](https://user-images.githubusercontent.com/80065996/155554454-8db5faf5-ef83-45a3-8c34-654d54f4c992.png)


![image](https://user-images.githubusercontent.com/80065996/155554662-636c13d4-7dae-4391-b08d-109178bd1cfe.png)


# switching between projects


![image](https://user-images.githubusercontent.com/80065996/155555434-65fb53f4-64d7-4fea-840e-41e6035dba51.png)



# pod


![image](https://user-images.githubusercontent.com/80065996/155555920-a8611c04-3868-4625-a836-ccfd7d8a9e4d.png)



# pod can have single container inside of it or multiple containers inside of it. 


![image](https://user-images.githubusercontent.com/80065996/155556254-940d41a6-c08d-4232-87ab-b1301b4728bf.png)


# single pod contain single container inside of it. that is a good approach. if we have multiple containers inside we will call it as side car containers


# oc explain - explains documentation of resource


![image](https://user-images.githubusercontent.com/80065996/155557012-382b6b67-5cac-4e61-b44f-3d425e9f3a1a.png)


![image](https://user-images.githubusercontent.com/80065996/155572203-168fb17a-532f-4605-b9a5-9dd654e5130c.png)


# we can get more granular information about every fileds in pod using below command


![image](https://user-images.githubusercontent.com/80065996/155573488-d43bf2c6-d79f-4408-9841-cf1661f4bc19.png)


![image](https://user-images.githubusercontent.com/80065996/155573944-50222a9f-dc30-45c7-9f42-cbadcb5b208e.png)


![image](https://user-images.githubusercontent.com/80065996/155575528-ba9cf4a0-1536-4c88-983e-a443f66b5f39.png)


![image](https://user-images.githubusercontent.com/80065996/155575994-5530fe56-14d2-4c38-9913-4f71fb4be2b0.png)


# how to check what are the resources in openshift cluster


![image](https://user-images.githubusercontent.com/80065996/155576794-bb3386a2-2b18-4112-a3ff-33b8ae5ab11e.png)


# run the first pod


![image](https://user-images.githubusercontent.com/80065996/155577105-d6f18b93-af7a-45de-bac5-f5e1dc5aa4fd.png)


![image](https://user-images.githubusercontent.com/80065996/155577506-d3e0e626-6cb6-4387-bd21-d511a19c9c43.png)


# check the resources in the cluster using 'oc get'


![image](https://user-images.githubusercontent.com/80065996/155656201-66cc1bbf-fc45-46f4-9651-8e2c9bfe7cc5.png)


![image](https://user-images.githubusercontent.com/80065996/155656258-6283d57a-8db3-4dfa-8bae-41273f99969c.png)


# getting inside of the pods and running a shell. Note: Once you get inside the pod, you are always inside of the container too in a single pod with single app running inside


![image](https://user-images.githubusercontent.com/80065996/155656551-f73cffa0-63cd-459a-94a2-d6ebf83b98d3.png)


![image](https://user-images.githubusercontent.com/80065996/155657450-52841cba-ad1e-45e4-9b27-c8135bf14432.png)



![image](https://user-images.githubusercontent.com/80065996/155657612-2cc54e0c-587f-483c-8686-0529ab2a92d8.png)


# how to delete the resources in openshift cluster. we have to use 'oc delete' command. while using 'oc delete' command we have to mention the resource type as well.
# because with oc command we can delete almost anything in the openshift cluster. 


# error will be throwed if we didnt mention the resource type as shown below


![image](https://user-images.githubusercontent.com/80065996/155658772-374b35e0-3dcc-4788-a765-fb610893285c.png)


![image](https://user-images.githubusercontent.com/80065996/155658885-c2ac6978-8055-4349-8d4c-eebf68749567.png)


# how to watch lifecycle of pod. -- open multiple teminals for this demo


![image](https://user-images.githubusercontent.com/80065996/155659537-fa16a22f-c4fc-4c7b-b452-253b5bc07514.png)


# kept one terminal for watching and open the other terminal and run the 'oc create' command for pod. you can see the lifecycle clearly 


![image](https://user-images.githubusercontent.com/80065996/155660063-b94bf15e-466d-484c-a82c-d43419172785.png)


# check the status of deletion of the pod.


![image](https://user-images.githubusercontent.com/80065996/155660490-f05d6481-41e8-4bf1-8a82-ae8304880e05.png)


# 'oc explain' - understanding the YAML definition of pod


![image](https://user-images.githubusercontent.com/80065996/155663020-41c96de5-bb11-4b03-8ad4-5299a7d8530c.png)


# note: first (pod) - is resource name. next followed by objects names(header names) in the YAML file. you have to traverse the fields in YAML by mentioning parent
# followed by child


![image](https://user-images.githubusercontent.com/80065996/155663262-c7ccfb5f-16ce-4620-ac04-7793f1a3e696.png)


# CONCEPT: NEXT OPENHIFT RESOURCE TYPE - DEPLOYMENTCONFIG - SAME AS 'DEPLOYMENTS' IN KUBERNETES


![image](https://user-images.githubusercontent.com/80065996/155663776-df906353-6043-4059-8260-f9d412b72d53.png)


# documentation for 'deploymentconfig'


![image](https://user-images.githubusercontent.com/80065996/155664438-38e8da73-2930-4425-8102-dea08b125a42.png)


![image](https://user-images.githubusercontent.com/80065996/155665089-3285313f-8a66-4cd0-94f4-ba917e2f6b1b.png)


# 'deploymentconfig' using image name


![image](https://user-images.githubusercontent.com/80065996/155674607-7f07be57-2c44-446a-b352-6f00bfc75dfe.png)


![image](https://user-images.githubusercontent.com/80065996/155675146-fb0e643a-bb63-488e-a377-da37d700af81.png)


# we have created 'deployment-config' using already existing image from 'quay.io' repository. Note: we didnt create a YAML file for this. 


![image](https://user-images.githubusercontent.com/80065996/155675601-13b5567a-bef1-4266-9b34-6169b5757d51.png)


![image](https://user-images.githubusercontent.com/80065996/155675798-324af090-25ca-434a-8ab6-2e71c4a374f9.png)


![image](https://user-images.githubusercontent.com/80065996/155675944-7495281d-c1eb-4f93-b2a9-3d9b25b23d63.png)


![image](https://user-images.githubusercontent.com/80065996/155676026-690be070-ba00-48f8-9ba5-0405a3f24618.png)


![image](https://user-images.githubusercontent.com/80065996/155676658-b104ec96-67b9-472f-8e50-e82eb77d2e5b.png)


# Cleaning up 'deployment-config'

# demo: if i try to delete a pod, you could see immediately another pod is starting up.


![image](https://user-images.githubusercontent.com/80065996/155677748-b5458aae-05ad-42ca-8f39-660ef8f0a4a0.png)


# how to see image stream details


![image](https://user-images.githubusercontent.com/80065996/155678161-19566064-596f-40d3-b301-20ff3a20af0a.png)


![image](https://user-images.githubusercontent.com/80065996/155678251-c0f26a16-131d-414c-9bcf-44552766ac6d.png)


# cleaning up the 'deployment-config' 


![image](https://user-images.githubusercontent.com/80065996/155678800-2dd6d35a-075a-43eb-9e65-0a231a8ada34.png)


# how to clean up a 'deployment-config' using 'label-selector'
# NOTE:
# 1) IN KUBERNETES, WE DONT HAVE OPTION TO GET IMAGE FROM DOCKER HUB AND CREATE A DEPLOYMENT WITH 'KUBECTL' COMMAND
# 2) BUT IN OPENSHIFT, WE HAVE A COMMAND FOR THIS WITH 'OC' TOOL. 


![image](https://user-images.githubusercontent.com/80065996/155687762-c167382f-58e1-4c0d-8b81-90f5c15adcd7.png)


![image](https://user-images.githubusercontent.com/80065996/155688141-696cb273-bc91-41fc-8d49-d914ace52ac9.png)


# we are going to clean up the 'deployment-config' using labels. so we are using 'oc describe' command to get the labels


![image](https://user-images.githubusercontent.com/80065996/155689135-f49924b3-01f2-4d5f-b7c4-dcc3e46defe3.png)



![image](https://user-images.githubusercontent.com/80065996/155688721-4cb5c0d9-4528-45e3-9cc3-ea913bdcf6ff.png)


![image](https://user-images.githubusercontent.com/80065996/155689331-799290df-80d6-473b-bba0-17c19e3fb932.png)


# note : we cannot delete the deployment in kubernetes by using labels. but in openshift we can delete the deployment using labels
# while selecting the appropriate label, see the label under the 'deployment' section from the result displayed by 'oc describe' command as highlighted above
# also leave the label which is having dot operator inbetween (.).


# confirming all the resources are deleted completely


![image](https://user-images.githubusercontent.com/80065996/155692881-e1bdb305-8ab9-4e1d-90a6-6ede3d867c6f.png)


# CONCEPT: 'NAMING THE DEPLOYMENTS'
# without giving name to the deployment, it will by default take the name of the 'image'


![image](https://user-images.githubusercontent.com/80065996/155693801-49dc1d71-f3de-4803-998c-1a3ce27a7329.png)


# Now all the resources (services,deployment-config,image streams) are named as 'demo-app' as given in the command


![image](https://user-images.githubusercontent.com/80065996/155695192-faba99ea-6a0d-4eed-bef9-4d6c36820395.png)


![image](https://user-images.githubusercontent.com/80065996/155695636-350670d7-bb3e-4818-83c2-d5bd1c26fed2.png)


# you can do any number of deployments by changing the name of deployment. In this example, we have created a new deployment as shown below. Total 2 deployments are visible


![image](https://user-images.githubusercontent.com/80065996/155696106-c58b5541-3ab1-4c12-9604-fc863e1adf73.png)


# find the label using 'oc describe' command for 'deployment-config'


![image](https://user-images.githubusercontent.com/80065996/155696915-9458f964-2f1b-4e34-a5c1-65b7d0f26aaa.png)


# deleting the first 'deployment-config' as shown below. Notice that even labels are created with name we have given in the command for 'deployment-config(demo-app)'


![image](https://user-images.githubusercontent.com/80065996/155697154-db532d65-30c3-456b-a3b2-ec4cf12f0874.png)


# we had 2 'deployment-config' (demo-app and demo-app2). we deleted the first 'deployment-config'. Only second 'deployment-config' exists


![image](https://user-images.githubusercontent.com/80065996/155697768-fd9b3648-7c73-4ce2-9c84-7d99a03ce924.png)


# now delete second 'deployment-config' too. identify the label using 'oc describe' command


![image](https://user-images.githubusercontent.com/80065996/155698021-a28deb74-3342-4ff4-b5f9-c5de7f0b3cbc.png)


![image](https://user-images.githubusercontent.com/80065996/155698223-05da85dd-db6b-47fd-a41f-4b4f646d5c0d.png)


# CONCEPT : DEPLOYING APPLICATION FROM GIT. BECAUSE ALL THE TIME, WE CANNOT FIND OUR IMAGE IN REPOSITORY (EITHER QUAY OR REPOSITORY ETCC...)


![image](https://user-images.githubusercontent.com/80065996/155751580-f225c0ae-fa16-4f78-bcde-9f4f5d972211.png)


![image](https://user-images.githubusercontent.com/80065996/155752583-513298d2-af47-40c4-941d-64a45213c239.png)


![image](https://user-images.githubusercontent.com/80065996/155752925-87589180-7ac5-427a-b984-ebd151a08859.png)



# how automated creation of 'docker image' happened in the backend. This is called as 'Build config'
# We can see 'build config' and 'image stream' in detail little later.
# this demo we have given only 'github' repo. so openshift 'build config' will clone the git repo and then build it using dockerfile present ithe git repo and push the image to 
# image repository and tag it. Also a trigger will be added to the image repository. If any changes to code it will get rebuild again.


![image](https://user-images.githubusercontent.com/80065996/155836965-6578f942-039d-4df7-ad59-696461658a93.png)


# 'oc logs -f bc/hello-world'  -- below image gives the detailed steps and logs on how this build happened.


![image](https://user-images.githubusercontent.com/80065996/155837263-bda6f3d7-a474-4dc2-a2ca-5e7131a1ab7a.png)


# there will be certain pod which will be in completed status when we deploy application. They are called 'build pods', those pods will  be in completed status.
# they are just like doing the job get completed. openshift will delete them in sometime and reclaim its resources.


![image](https://user-images.githubusercontent.com/80065996/155837401-20a81341-79ab-4774-8d22-304b9579f779.png)


![image](https://user-images.githubusercontent.com/80065996/155837539-5b9fd7b5-ba48-4bf1-b5e9-56ce0414045a.png)


# clean up and resdy for next set of demo. Since we build this time, you can see 'build config' is create seprately and it got cleaned up.


![image](https://user-images.githubusercontent.com/80065996/155837585-aac80a6c-f24d-4030-aa9d-fdc6c6747b6f.png)


# CONCEPT := REPLICATION CONTROLLER


![image](https://user-images.githubusercontent.com/80065996/155837615-125a84ee-ea63-4bd6-8bfb-33771d13b972.png)


![image](https://user-images.githubusercontent.com/80065996/155837705-f58a8cef-bfb5-49ff-9bec-667ed43a6b99.png)


# demo: deploy application from quay.io


![image](https://user-images.githubusercontent.com/80065996/155837718-78f5b7bb-0eec-47e6-8f8a-b81791bfbd48.png)


![image](https://user-images.githubusercontent.com/80065996/155837741-242f973d-3612-4fb0-bd39-f11d0f046302.png)


# we are going to see the YAML file for 'deployment config' in openshift to understand better. below command will display the YAML in screen


![image](https://user-images.githubusercontent.com/80065996/155837773-8bda6e2f-5c28-4aee-aecf-a3efc9fa26bd.png)


# instead we can take the output to file like shown below,


![image](https://user-images.githubusercontent.com/80065996/155837820-8aef8116-3b61-4b96-b397-2cb29021841e.png)


![image](https://user-images.githubusercontent.com/80065996/155837990-fa8e2e0e-7853-432e-b8fe-816f17f4e941.png)


![image](https://user-images.githubusercontent.com/80065996/155838006-060b281e-2d98-4427-ae9a-426f81cb5915.png)


![image](https://user-images.githubusercontent.com/80065996/155838018-cc8af99a-b0dd-4e5e-814b-32fa0735a462.png)


# How to check the replication controllers?


![image](https://user-images.githubusercontent.com/80065996/155845318-c784ff2f-f053-4420-ada7-ca9fd5dbb6df.png)


# CONCEPT:= ROLLOUT AND ROLLBACK OF APPLICATION
# 1) oc rollout
# 2) oc rollback


# open two terminals for this demo


![image](https://user-images.githubusercontent.com/80065996/155845488-b14a756c-252c-4356-a1df-f3e58e9b9e00.png)


# run the application using image present in 'quay' repository in one of the terminal window
# NOTE: WE ARE INSTALLING THE APP NOT AS 'DEPLOYMENT CONFIG'. only as'deployment'


![image](https://user-images.githubusercontent.com/80065996/155845748-74a4ddc4-f1ac-4fbc-ac03-7c07fd66e3ef.png)


![image](https://user-images.githubusercontent.com/80065996/155845814-b888a26d-93f0-458a-8740-39d7611f6b1a.png)


# run pod watch in one of the terminal


![image](https://user-images.githubusercontent.com/80065996/155845846-ea055a07-9c06-4b42-a061-da555dfdb87b.png)


# rollout command


![image](https://user-images.githubusercontent.com/80065996/155845865-cf46c1f0-1f94-4fab-960a-8a620bdf4d7a.png)


# if we use only 'deployment' we cannot do rollback


![image](https://user-images.githubusercontent.com/80065996/155845912-b837e91e-c7f9-44e9-8ed3-fe207d9e971e.png)



# deleted the deployment and created 'deployment-config' of the application


![image](https://user-images.githubusercontent.com/80065996/155846013-5003feab-f43a-4a1e-8fb8-38a52d19d70d.png)


![image](https://user-images.githubusercontent.com/80065996/155846034-f5bc6102-a8d5-41fb-b7e9-4edf8122333d.png)


# run the pod watch in one 'terminal' and in other terminal we are going to rollout the deployment


![image](https://user-images.githubusercontent.com/80065996/155846113-26518196-2051-497c-b0c6-01246d6ddf6c.png)


# you could see pods under first replicaset (hello-world-1) is deleted and new replica set(hello-world-2) is created and pods are scheduled newly in second replica set
# counter for pods in old replicaset is reset to zero


![image](https://user-images.githubusercontent.com/80065996/155846211-581100d0-fca8-4d1c-8883-4a66eca6bb70.png)



# explantion:


![image](https://user-images.githubusercontent.com/80065996/155846296-70eddd33-70fa-4553-95b5-8648c0af4b22.png)


# we have 'deploy' pod which starts and then created new pods in new replication controller and then gets completed.
# also we could see old pods are also getting terminated.
# pods are getting showed in lifecycle - pending,creating,running,completed/terminated.


# rollback to previous version if a new version you rollout has an error


![image](https://user-images.githubusercontent.com/80065996/155846400-03895335-447c-43c6-a505-4f26026383ce.png)


![image](https://user-images.githubusercontent.com/80065996/155846661-67d10bc1-5ae5-4ff3-bf03-b84a4553a95a.png)


# CONCEPT: INTRODUCTION TO SERVICES


![image](https://user-images.githubusercontent.com/80065996/155846776-be7c3ead-77a5-4589-a256-5e7def4d67d5.png)


![image](https://user-images.githubusercontent.com/80065996/155846802-94a4138e-e6fe-4d63-a3e3-4a0503b35576.png)



![image](https://user-images.githubusercontent.com/80065996/155846861-972c3883-2c94-47bf-bee6-b5dac8a0adf3.png)


# NAVIGATE TO BELOW DIRECTORY WE DOWNLOADED


![image](https://user-images.githubusercontent.com/80065996/155846915-efc6289f-3b94-4676-a621-78b608a5083c.png)


![image](https://user-images.githubusercontent.com/80065996/155846951-99b13caf-f5e9-4ff6-9d49-7c5eb386abe4.png)


# create a pod from YAML we have


![image](https://user-images.githubusercontent.com/80065996/155847021-73fce2f1-6f3d-4740-a492-5fb47e82b25a.png)


# expose the pod


![image](https://user-images.githubusercontent.com/80065996/155847087-111b06a6-e349-4f2e-8eea-2d66d26b3c30.png)


# when we run this command to expose the pod to outside world, we should get this error


![image](https://user-images.githubusercontent.com/80065996/155847125-76306009-79cc-40a6-89c6-c0474f50e8dc.png)


# oc expose command needs a little more information. 
# 'oc expose' command is creating the service for the pod which is exposed in the port 8080 by the application running inside the pod
# but default service created by openshift 'oc expose' command is using only 'cluster ip' service


![image](https://user-images.githubusercontent.com/80065996/155847154-f2e20106-b2f9-46cc-ad0e-cc60f6d88ae2.png)


![image](https://user-images.githubusercontent.com/80065996/155847174-6208c4a4-a80f-414c-80e1-f70e5d611509.png)


![image](https://user-images.githubusercontent.com/80065996/155847246-fd05e1a8-7560-49f8-adf0-df13c3017c5f.png)


# create the second pod as part of demo using YAML file we have in our local folder


![image](https://user-images.githubusercontent.com/80065996/155847304-b0d5c217-cce9-4467-8eae-090a6d0a87ab.png)


![image](https://user-images.githubusercontent.com/80065996/155847374-dc500e84-e480-43c0-9cad-5d3362742271.png)


# to communicate application running inside another pod, we need to use ip address of service created to load balance the pod
# now we have pod-1 which is having service which is loadbalancing it
# second pod (pod-2) we created is not having any service. we entered the second pod and called the application running inside the pod-1


![image](https://user-images.githubusercontent.com/80065996/155849917-833eede8-2bda-4cdf-b850-d6e69988768d.png)


![image](https://user-images.githubusercontent.com/80065996/155850029-c5b62e15-56a6-418d-9131-0497c68863ce.png)


![image](https://user-images.githubusercontent.com/80065996/155849964-4a4211d0-17d6-4aa1-825d-53e3add30eaa.png)


# accessing another pod using service with the help of environment variable - more robust way.
# first way - we used 'oc status' command and got the ipaddress of service and then called the application over the network which is running inside another pod


![image](https://user-images.githubusercontent.com/80065996/155850086-2c19610a-f373-4b9e-986c-0b41547b4c7a.png)


# check the environment variables inside the pod by giving below command after entering into the pod


![image](https://user-images.githubusercontent.com/80065996/155850320-a9b5e4a6-fc20-4d3e-9e9b-3042abdba8de.png)


![image](https://user-images.githubusercontent.com/80065996/155850538-d364e5f8-9996-4f9a-8bff-c41fd2f698c2.png)


![image](https://user-images.githubusercontent.com/80065996/155850946-2d5c17fb-a0d1-4535-9163-79496359c797.png)


# you can use the environmant variable for ipaddress and port number. just use dollar symbol($) before and then give the environment variable as shown below


![image](https://user-images.githubusercontent.com/80065996/155851004-d36f5d86-b430-4ce6-a317-bece3dfea970.png)


# so in openshift, for every pod created from 'deployment-config', if we enter into the pod, it will have environment variables which has ipaddress of services created to 
# load balance the deployment-config created. so we can use that to connect to pods over the network



# CONCEPT: EXPOSING THE ROUTE. (This is similar to 'Nodeport' in the kubernetes)


![image](https://user-images.githubusercontent.com/80065996/155851465-934dc0d1-e661-4a21-a0ae-0c4159341cbd.png)


![image](https://user-images.githubusercontent.com/80065996/155851796-3646309f-9a08-493c-ac53-2863fb59b62f.png)


# NOTE: WE CAN CREATE A 'ROUTE' BY USING 'OC EXPOSE' COMMAND. WE CAN EXPOSE A POD SEPARATELY AND 'SERVICE' SEPARATELY. 
# MOSTLY WE USE TO EXPOSE THE 'SERVICE' CREATED FOR 'DEPLOYMENT-CONFIG' BY USING 'OC-EXPOSE' COMMAND
# 'OC EXPOSE' COMMAND WILL GIVE US THE 'URL' TO ACCESS THE APPLICATION FROM THE BROESE.
# AS SHOWN ABOVE WE GOT THE URL. BY USING THE URL, WE ACCESSED THE APPLICaTION RUNNING INSIDE THE OPENSHIFT CLUSTER


![image](https://user-images.githubusercontent.com/80065996/155852081-c8797ebd-fbfe-45c5-bb40-80317140429a.png)


# EXPOSING A POD - CREATES THE 'SERVICE' 
# EXPOSING THE SERVICE - CREATES THE URL TO EXPOSE THE APPLICATION TO GET ACCESSED FROM BROWSER


# delete all the existing resources and deployed a new application. once 'deployment-config' is created it will by default ask us to expose the application.


![image](https://user-images.githubusercontent.com/80065996/155852297-3a113b66-519b-483e-94a3-3c89eb3564b9.png)


![image](https://user-images.githubusercontent.com/80065996/155852523-d54445c5-a98c-495e-95e5-9d74750ba531.png)


# run 'oc status' to check the URL,


![image](https://user-images.githubusercontent.com/80065996/155852617-367983de-7c3f-4fcf-b953-a549fd76dbfe.png)


# result in the browser


![image](https://user-images.githubusercontent.com/80065996/155852645-1773c5ce-9a24-4929-9b63-98c5552100c2.png)


# intro to routes


![image](https://user-images.githubusercontent.com/80065996/155872136-66e34631-fa5b-487f-acdc-7469a33886cb.png)


# ROUTE is new to openshift. it is not available in kubernetes.
# 'ROUTE' is used to expose the 'service' to outside world by providing 'DNS URL'. (similar to 'nodeport' in kubernetes)
# when we run 'oc expose' command 'route' will be created.


![image](https://user-images.githubusercontent.com/80065996/155872434-ff5fc11d-8c67-45b9-9883-0879a0e59b7a.png)


![image](https://user-images.githubusercontent.com/80065996/155872484-a8f8955d-d1e7-4821-8c7f-bbbdb76a0e68.png)


![image](https://user-images.githubusercontent.com/80065996/155872509-4511f0ae-388a-4463-b8f7-06c18c76197c.png)


# just check the 'spec' section it shows it created the 'route' for 'service' (mentioned in 'to' section) of YAML))


![image](https://user-images.githubusercontent.com/80065996/155872535-b3ba2297-bdfe-4e12-825c-db1ad51cd1e9.png)



# CONCEPT : CONFIGMAPS


![image](https://user-images.githubusercontent.com/80065996/155872643-85610e5d-bb7b-4b34-bf01-7ab6da51f6d1.png)


![image](https://user-images.githubusercontent.com/80065996/155872655-a69e8cb2-bbf4-4b13-93d0-e342954f7016.png)


![image](https://user-images.githubusercontent.com/80065996/155872664-0ba04d37-b782-4b4b-8bd5-197549197790.png)


![image](https://user-images.githubusercontent.com/80065996/155872689-e96337b7-be71-45bd-89be-19821d49e6c0.png)


![image](https://user-images.githubusercontent.com/80065996/155872718-bced876a-2992-4497-ac34-6db40749e6e7.png)


# WE SHOULD NOT STORE ANY SENSITIVE INFORMATION IN 'CONFIGMAP'. WE HAVE SEPARATE RESOURCE TYPE IN OPENSHIFT FOR STORING SENSITIVE INFORMATION


![image](https://user-images.githubusercontent.com/80065996/155872752-62de8f25-08c1-4662-9d51-269f9c3fb73a.png)


# Limitation of configmaps is we can create configmap which is having limit of 1 MB only. More than 1 MB, we cannot use 'configmap' we have to use alternative


![image](https://user-images.githubusercontent.com/80065996/155873827-8fffba27-b286-4132-8625-da73ea46458a.png)


# configmap is used when we have situation to use environment variables in our deployment file in multiple places which are repetitive. instead of mentioning multiple
# times, we can create a 'configmap' resource and refer the value from it. 


# sample YAML file for creating configmap


![image](https://user-images.githubusercontent.com/80065996/155874056-a387bb3e-a6e9-452f-b982-df5c3366441f.png)


# CREATING CONFIGMAP FROM COMMAND LINE


![image](https://user-images.githubusercontent.com/80065996/155874079-605ef6b5-a0ba-410d-bdfd-c3b33ba648e2.png)


![image](https://user-images.githubusercontent.com/80065996/155874308-76464981-e266-480e-9bce-10ca96ffa8f5.png)


![image](https://user-images.githubusercontent.com/80065996/155874344-8d1c18c4-b995-4015-b3d9-40790b56bf1a.png)


![image](https://user-images.githubusercontent.com/80065996/155874422-1c50a522-27d0-4a44-9173-603a82f8132f.png)


![image](https://user-images.githubusercontent.com/80065996/155874445-c7b62c70-e2bb-4607-afec-6bd836a06fb5.png)


# we need to always look for the 'DATA' section in the configmap YAML. 'DATA' section will contain the environmant variables we are going to share across the
# multiple pods.


# below is the code we have to use to retireve the environment variable we are setting using configmaps.
# os.getenv(environment_variable_name)


![image](https://user-images.githubusercontent.com/80065996/155874497-1f4d9dbf-8fe8-42d6-ba1b-d6ab25753b18.png)


![image](https://user-images.githubusercontent.com/80065996/155874572-c6b912fb-8115-4335-a72f-58073e739fea.png)


# CONCEPT: CREATING 'CONFIG-MAP' USING 'DEPLOYMENT-CONFIG'


![image](https://user-images.githubusercontent.com/80065996/155874733-c0d656f0-52e5-47d0-95ee-74089f1f3bed.png)


![image](https://user-images.githubusercontent.com/80065996/155874769-e8c5556c-1255-4ad6-949e-401070c0bf1f.png)


![image](https://user-images.githubusercontent.com/80065996/155874785-783a19d0-e5fd-42d5-9506-9b2453ac7dce.png)


![image](https://user-images.githubusercontent.com/80065996/155874848-6d371501-0fe0-4670-a0a8-646a44a72f4b.png)


![image](https://user-images.githubusercontent.com/80065996/155874858-82837268-8000-4e8d-91d3-3d1b14759b5c.png)


# we are getting the default message in the environment variable. This is because, we created configmap and deployment-config separately but we are yet to make a
# connection or link between configmap and deployment-config


![image](https://user-images.githubusercontent.com/80065996/155875009-4ef71910-4a6d-4169-b0f1-0f39cdb14b63.png)


# connecting command 


![image](https://user-images.githubusercontent.com/80065996/155875015-9a38e829-3282-47a5-8d63-03e10cc1f9ba.png)


![image](https://user-images.githubusercontent.com/80065996/155875100-56ecee99-507f-4555-9cbf-f83585cad05f.png)


# successfully overrided the environment variable using configmap as shown below


![image](https://user-images.githubusercontent.com/80065996/155875164-923e6f8d-81c5-47c2-8c0a-f7c3638f2adf.png)



![image](https://user-images.githubusercontent.com/80065996/155875310-7309093c-63f1-4f6d-898e-6b79d0ad84f3.png)


# Notes: 
# 1) when we create configmap via 'oc create' command, YAML file will be created behing the scenes for the key value pair we have given in the command(MESSSAGE)
# 2) so configmap resource will be created.
# 3) you can use 'oc get -o yaml cm 'cm_name' > cm.yaml' to see the YAML file
# 4) next we will create deployment config using ' oc new-app' command for the 'hello-world' application
# 5) you can go 'oc get -o yaml dc hello-world' > dc.yaml to see the deployment-config yaml. This YAML will not map configmap with our deployment-config yaml
# 6) you have to connect the configmap with deployment config using a connector command 'oc set'
# 7) once connected, you can run 'oc get -o yaml dc hello-world' > up.yaml to see configmap section


![image](https://user-images.githubusercontent.com/80065996/155875567-afbe27aa-122c-4fda-a846-ae792806731c.png)


![image](https://user-images.githubusercontent.com/80065996/155875587-589e9bd7-c772-4e89-9d21-1fe6d9c3a819.png)



# creating 'configmap' from the file 


![image](https://user-images.githubusercontent.com/80065996/156124346-bf462743-009c-4f5a-9bc2-e214fbb532dd.png)


![image](https://user-images.githubusercontent.com/80065996/156124461-bdd1ee53-61c5-4230-88a8-de999c40228d.png)


![image](https://user-images.githubusercontent.com/80065996/156124591-b6815a73-ff3b-40cc-a5f2-ab308771a725.png)


![image](https://user-images.githubusercontent.com/80065996/156124861-b1deab52-faa2-4c02-86ea-86928aba06f5.png)



![image](https://user-images.githubusercontent.com/80065996/156125059-a3fe1a2a-17f3-4ea1-983e-7b5d46f72a45.png)


# instead of filename as 'key' in the configmap, we can provide the name to the file in the same command so that key will be the name we passed in the command


![image](https://user-images.githubusercontent.com/80065996/156125723-8d0b0798-7604-4a8a-8a64-54713317602d.png)



![image](https://user-images.githubusercontent.com/80065996/156125829-859c6d2a-685f-45b2-8c30-9fbce2243040.png)



# Key value pair for this type of 'configmap' is created with the format.
# key is the 'filename'
# value will be content inside the file

# 'configmap' is created. now we have to create 'deployment-config'. after creating 'deployment-config', we have to link the 'configmap' with 'deployment-config'


![image](https://user-images.githubusercontent.com/80065996/156125461-2681df38-df3c-4d4f-ad0a-c5f9999b54ec.png)


# connecting 'configmap(file-map)' with 'deployment-config(hello-world)'


![image](https://user-images.githubusercontent.com/80065996/156128523-8d6b8199-ea8a-4c51-9ca4-1a89c18642a3.png)


![image](https://user-images.githubusercontent.com/80065996/156129547-404be984-05e9-4f09-8511-4e320873d6c3.png)


# since we mapped both configmaps (file-map-1 and file-map-2), we could see both environment variable are set


![image](https://user-images.githubusercontent.com/80065996/156129591-d5b7aa4d-c777-40eb-a6c7-c70f41a7d32d.png)


# we are using 'Message' environment variable inside our golang code using 'os.Getenv(MESSAGE)'.
# expose the service and check this. route will be created


![image](https://user-images.githubusercontent.com/80065996/156130159-6ef7cff8-019f-4321-aedd-e4b9d94d8835.png)


![image](https://user-images.githubusercontent.com/80065996/156130097-370edc48-2bff-42f5-9329-185598da5828.png)


# NOTE: CREATE A CONFIGMAP, CREATE THE DEPLOYMENT-CONFIG and then run the 'oc command set env' to connect both. (sometimes configmaps will not be picked up)


# CONCEPT :=  CREATING 'CONFIGMAP' FROM DIRECTORY


![image](https://user-images.githubusercontent.com/80065996/156132417-50446ca1-bfba-4e75-b935-420f4a72cc30.png)


![image](https://user-images.githubusercontent.com/80065996/156132814-9aad2f50-4628-4342-b4d6-090890e6088c.png)


# directory 'pods'


![image](https://user-images.githubusercontent.com/80065996/156132878-aef76bda-6460-4290-8645-6014328f0470.png)


![image](https://user-images.githubusercontent.com/80065996/156132951-c39f6377-0b07-4db7-8228-8b0796a1d9fb.png)


![image](https://user-images.githubusercontent.com/80065996/156133036-d86182e9-b67b-44e2-a6f6-89773ee108e3.png)


# 'file name' inside the directory is created as a 'key' and contents of the files are created as 'value'. so forms the key-value pair


# now we have to connect the configmap with deployment-config using 'oc set env' command


![image](https://user-images.githubusercontent.com/80065996/156134576-2012b99d-0e6b-48f2-afda-eeb9ae7a9e7c.png)


![image](https://user-images.githubusercontent.com/80065996/156134610-0df00386-6984-4966-91e9-404a7ca79b87.png)


![image](https://user-images.githubusercontent.com/80065996/156134859-4a3ecc39-472a-4389-90e0-04fac75a2b7e.png)


![image](https://user-images.githubusercontent.com/80065996/156134913-fdc979e8-4543-40c1-87c1-d57cac6ee12c.png)


![image](https://user-images.githubusercontent.com/80065996/156134982-ea0d28da-232a-4bae-ad15-fc7cfa42c50e.png)


![image](https://user-images.githubusercontent.com/80065996/156135106-cbac159c-3a3e-4ec3-8a9b-4a06cbd860c2.png)



![image](https://user-images.githubusercontent.com/80065996/156135262-8ebf49e8-1a50-4cc3-81c1-1a4bf9084464.png)



![image](https://user-images.githubusercontent.com/80065996/156135746-1d1e4e0b-9023-4f0b-a78a-d1a0f575ced5.png)



![image](https://user-images.githubusercontent.com/80065996/156135852-dd6c7b18-9832-4bfc-bf7f-1b00432fd0b3.png)


# CONCEPT- 'SECRETS' INTRODUCTION
# this is similar 'key-value' pair as of 'config-maps' but as per name suggests we need to use this to store sensitive information


![image](https://user-images.githubusercontent.com/80065996/156135932-b63601b0-2cb5-403a-a33d-c217ec89d1c0.png)


# Types of secrets.
# Opaque tokens. This is generic token which dont have any proper structure. we can use as per our flexibility


![image](https://user-images.githubusercontent.com/80065996/156137166-22045a6c-bb84-4d42-bb59-545bde44efd1.png)


# 'service account' token. This token is used by the pods to communicate with other API's avaialble inside the openshift cluster. We are not going to cover this token
# much in this course


![image](https://user-images.githubusercontent.com/80065996/156137421-5c75c7fa-ebd6-4de7-b960-77378cdbd4c5.png)


# Registry authentication token. This is used when we use 'images available in private registries' from the dockerhub,quay or any other public hosted registries.


![image](https://user-images.githubusercontent.com/80065996/156138119-63e1b0da-aa56-4327-af11-f73c956671c9.png)



# Authentication types when using secrets: This is used to access repos such as 'git' when openshift trying to conenct to them.


![image](https://user-images.githubusercontent.com/80065996/156138535-7685afa5-697b-4e0b-8d15-b9f4f5d60017.png)


# CONCEPT: CREATING 'OPAQUE SECRET' FOR CUSTOM AUTHENTICATION


![image](https://user-images.githubusercontent.com/80065996/156138798-b3a256dd-cdf4-41a5-82f8-79ff6d6971bf.png)


![image](https://user-images.githubusercontent.com/80065996/156139030-c6023d44-6516-4d97-a25a-9c0a5d816b5d.png)



![image](https://user-images.githubusercontent.com/80065996/156139228-c0b6a40c-354e-43ff-a180-7cc84447ab2e.png)


![image](https://user-images.githubusercontent.com/80065996/156139664-7b890338-3b15-48e7-8d20-06cf5d101e58.png)


# YAML is showing key value (MESSAGE) but the corresponding value (encoded in base64) while showing as highlighted below


![image](https://user-images.githubusercontent.com/80065996/156139924-4ed81417-4625-469d-874d-5e5c0b1ae351.png)


# CONSUMING SECRETS AS ENVIRONMENT VARIABLES INSIDE THE APPLICATION RUNNING INSIDE THE POD USING 'DEPLOYMENT-CONFIG'


![image](https://user-images.githubusercontent.com/80065996/156140286-2aee2fa8-3c0e-4c9e-9d62-81cfdc597adf.png)


![image](https://user-images.githubusercontent.com/80065996/156140939-5fd62ebb-e64e-4c25-8eb3-17dd13f41a50.png)


# result. Below it displays the value of the environement variable 'MESSAGE'. But we are going to change it using 'secret'


![image](https://user-images.githubusercontent.com/80065996/156141208-0857e1ed-26be-47d4-8da9-b428dcfadd19.png)


# PODS currently running


![image](https://user-images.githubusercontent.com/80065996/156141452-08412d5c-c577-4185-88e3-5e9e8fc3aa8c.png)


![image](https://user-images.githubusercontent.com/80065996/156141563-bce1a7ce-b7dd-412d-91b5-0bd7fb424599.png)


# connecting 'secret' with 'deployment-config'. for every 'oc set env' connect statement old pod will be destoyed and new pods will be created using 'config-map'
# or 'secret'.


![image](https://user-images.githubusercontent.com/80065996/156141777-523072fa-48c3-452d-8941-b409d0830cf5.png)


# you could see the value of 'MESSAGE' environment variable displayed using 'os.getenv($MESSAGE)' inside golang program as highlighted below


![image](https://user-images.githubusercontent.com/80065996/156142174-5efb43ef-5ef3-4746-bea9-211dd5dd0a64.png)


![image](https://user-images.githubusercontent.com/80065996/156142595-67423011-c8f3-423d-b393-241b0ab194df.png)


![image](https://user-images.githubusercontent.com/80065996/156142940-c0ac111f-b683-4595-a6ff-d6114bbce5e2.png)


![image](https://user-images.githubusercontent.com/80065996/156142799-233a9c6a-be61-4d10-8be9-9c7251a96221.png)



# CONCEPT: INTRO TO 'IMAGES' - 'IMAGE' AND 'IMAGE STREAMS' AND 'IMAGE STREAM TAG'


![image](https://user-images.githubusercontent.com/80065996/156144293-2c638b58-c8f9-44f4-b481-90a723fa0a35.png)


# 'IMAGE STREAM' IS NOTHING BUT SET OF IMAGES. FOR EXAMPLE, IF YOU TAKE GOLANG, WE HAVE MORE NUMBER OF IMAGES WITH DIFFERENT TAGS IN THE DOCKER HUB
# UNDER 'TAG SECTION'. COLLECTION OF THE IMAGES ARE CALLED 'IMAGE STREAM' AND TAG ASSOCIATED WITH EACH IMAHE IS CALLED 'IMAGE STREAM TAG'

# ONE MAJOR DIFFERENCE FOR THIS TERM IS, WE CAN SET UP A TRIGGER FOR THE IMAGE TAG WITH 'DEPLOYMENT-CONFIG', IF IN CASE ANY NEW CHANGE PUSHED FOR THAT IMAGE, 'DEPLOYMENT-CONFIG' WILL BE TRIGGERED AUTOMATICALLY.


![image](https://user-images.githubusercontent.com/80065996/156144779-1c6b714f-f550-46b1-a996-5e31960d1e71.png)


# create a new 'deployment-config' called 'hello-world'. you could see 'image stream' also created as part of this command while creating 'deployment-config'


![image](https://user-images.githubusercontent.com/80065996/156146652-d5fbad41-6210-467a-894d-3f2efa206ac7.png)


# 'image stream' is the openshift resource, we can see it by using 'oc get' command


![image](https://user-images.githubusercontent.com/80065996/156147295-3b47a1f1-603d-4abc-a2e5-cfac5cbd1957.png)


![image](https://user-images.githubusercontent.com/80065996/156147326-2339523d-063a-4a6a-bfda-daaf558e0206.png)


![image](https://user-images.githubusercontent.com/80065996/156147604-c4f53b56-e0d6-4030-bd72-ff662237b26a.png)


# image will be pulled from the 'quay.io' and stored in the 'image stream repositoy' in the openshift. (similar of 'image cache' in docker architecure)


![image](https://user-images.githubusercontent.com/80065996/156149060-f1bec9ba-97e3-42fc-953b-2ec9b6b27144.png)



# CONCEPT: HOW TO CREATE 'IMAGE STREAM'. IN OPENSHIFT WE CAN CREATE 'IMAGE STREAM' WITHOUT EVEN CREATING 'CONFIG-MAP'


![image](https://user-images.githubusercontent.com/80065996/156149148-18b1075b-56a2-452a-9149-10dd0bf8ede1.png)



# before this demo, make sure we dont have any 'image tag' or 'image stream' present already


![image](https://user-images.githubusercontent.com/80065996/156151559-11f8a7e2-0930-4d77-b0a2-40f360007d13.png)


# command to create new 'image stream'


![image](https://user-images.githubusercontent.com/80065996/156151906-e7cd5e40-790b-44b9-adc9-5a7a44a92703.png)


![image](https://user-images.githubusercontent.com/80065996/156152627-8ca0f5a5-b313-428f-8b74-c7dc961a6cde.png)


# describe 'image stream tag'


![image](https://user-images.githubusercontent.com/80065996/156153211-1c96b7ab-d5bc-45e1-9465-34d54fe76cfa.png)


# describe 'image steam'


![image](https://user-images.githubusercontent.com/80065996/156153424-fdc34635-ab67-4df1-9049-a79e0eaae0ec.png)


# command to create 'deployment-config' using our own newly created 'image-stream' rather than default openshift created 'image-stream'


![image](https://user-images.githubusercontent.com/80065996/156154355-f68b9bc7-4e5e-4502-8c9b-2021b7d8fed3.png)


# you could see 'image stream' is not created newly. it is picked up from the 'image stream' we created.


![image](https://user-images.githubusercontent.com/80065996/156154973-9c58871b-9505-4541-a428-5567dabb9562.png)


# Adding more 'image stream tags'


![image](https://user-images.githubusercontent.com/80065996/156157527-d8a5f0a8-a426-4c0b-a6c7-a5b541ebf4ab.png)



![image](https://user-images.githubusercontent.com/80065996/157685425-5196dee0-eea7-463a-9d5a-c1c3a062ab20.png)


![image](https://user-images.githubusercontent.com/80065996/157686964-0a843ba4-a05b-4dd7-9e3a-b637b8633c79.png)


# adding images of different tag to the 'image stream' 


![image](https://user-images.githubusercontent.com/80065996/157687094-28f55942-65b9-469b-9ca8-df6d01ec4d44.png)


![image](https://user-images.githubusercontent.com/80065996/157687346-50aaf56b-d986-41ce-abd4-73d7ea8e00ac.png)


![image](https://user-images.githubusercontent.com/80065996/157687528-2825b574-bbe7-4df0-8bfe-cba2a6c6493d.png)


# how to create private image stream


![image](https://user-images.githubusercontent.com/80065996/157688073-3a8a75ca-99bb-4926-877e-c5e18a2cdc66.png)


# till now we have downloaded image from a public registry which does not have any authentication. Now we are going to set up a private registry

# for our project, jenkins build the image using dockerfile, and push the image to artifactory. openshift in turn take image from artifactory and deploy in openshift


# INTRO TO 'BUILD' AND 'BUILD-CONFIG' IN OPENSHIFT


![image](https://user-images.githubusercontent.com/80065996/157692730-bd8ef2c7-b6c2-4a34-a2ea-e383cb7932b6.png)


![image](https://user-images.githubusercontent.com/80065996/157692966-64899bde-ceb6-44ba-b8fb-9947f7ebade2.png)


# we have given link of 'gitlab' repository where code and 'dockerfile' exits


![image](https://user-images.githubusercontent.com/80065996/157693916-160180e3-85bc-42d3-b165-e7d9bc06aa3c.png)


# from the dockerfile, base image 'golang:1.17.7' is taken, and 'image stream' is created also trigger will be attached to it to capture any changes to that image.


![image](https://user-images.githubusercontent.com/80065996/157694468-6e82c3db-bdd3-4456-973e-b785f6687387.png)



![image](https://user-images.githubusercontent.com/80065996/157694815-d91b7be3-834b-440c-ba01-35321b28a1da.png)


![image](https://user-images.githubusercontent.com/80065996/157702157-7e0e2938-f049-4cda-a3b8-18b55f05c8d3.png)


![image](https://user-images.githubusercontent.com/80065996/157702402-5e55110c-59d7-4359-8c87-ca96eaae82b7.png)


![image](https://user-images.githubusercontent.com/80065996/157703137-357d9a7e-06be-488e-a1b3-0d5179e557d8.png)


![image](https://user-images.githubusercontent.com/80065996/157703773-2b9663fc-7c0f-4cb7-a939-d2d3918d7bff.png)


![image](https://user-images.githubusercontent.com/80065996/157704061-9d9bd615-2aa1-4585-ba5a-bb5fffdb2652.png)


# how to check 'logs' for the 'builds'


![image](https://user-images.githubusercontent.com/80065996/157704318-ab18470b-5c7e-4e6c-8cf9-68871096f8ad.png)



![image](https://user-images.githubusercontent.com/80065996/157705802-57348717-5144-4498-b203-5910d0c61adc.png)


![image](https://user-images.githubusercontent.com/80065996/157705903-023c744a-faed-4a16-8502-7d771970fec5.png)


![image](https://user-images.githubusercontent.com/80065996/157705973-54fca8f9-a166-4297-821e-4756f5b0d2ed.png)


# you can see 'build' takes code from github and take 'dockerfile' from github and build the 'dockerfile' and push the image built into 'openshift registry'


![image](https://user-images.githubusercontent.com/80065996/157708326-f9b6e3e0-c1f4-48d5-8461-72a6d5fa4a15.png)


# HOW TO START A BUILD. (PREVIOUS WE SAW 'OC NEW-BUILD' NOW WE ARE GOING TO USE 'OC START BUILD')


# create 2 new powershell window. 1st window for watching pod


![image](https://user-images.githubusercontent.com/80065996/157836430-2563e4c7-35f2-435c-87ba-395ad6f56670.png)


# second window for 'starting the build'


![image](https://user-images.githubusercontent.com/80065996/157836482-03bb0e02-189b-438e-b459-aab0847196d8.png)


![image](https://user-images.githubusercontent.com/80065996/157836741-b2afc815-af88-47c5-b62d-95cebf913977.png)



![image](https://user-images.githubusercontent.com/80065996/157836934-fece2610-f506-4117-87a7-d3a90605404e.png)


![image](https://user-images.githubusercontent.com/80065996/157837034-bbdcb4d6-bc2d-4b6c-b277-544062b1a2d4.png)


![image](https://user-images.githubusercontent.com/80065996/157837613-d9089e95-abe5-45fe-a59e-98e7ed6e6b53.png)



![image](https://user-images.githubusercontent.com/80065996/157838428-2fbb52ba-81b9-44d7-8f69-af990096d15f.png)


# Cancelling builds in the middle


![image](https://user-images.githubusercontent.com/80065996/157838662-47a3c6fc-e35b-4a4f-9465-985f0d02cd0b.png)


# for this demo, opening a 2 powershell terminals, one for watching pods and other for triggering and cancelling the 'build'


![image](https://user-images.githubusercontent.com/80065996/157840372-e78ebcdb-285e-4c54-9875-a35dad1a7f39.png)


# you could see build is cancelled in between using command and pods created are terminated in the middle once we cancel the build manually

# 'BUILD CONFIG' IS LIKE THE JENKINS PIPELINE CREATION JOB. 'BUILD' IS LIKE EACH AND EVERY BUILD JOB WHICH JENKINS IS CREATING. WE CAN CREATE ANY NUMBER OF BUILDS
# WHILE SEEING 'OC LOGS' YOU CAN ALWAYS USE LATEST BUILD FOR LOGS 'OC LOGS 'LATEST BUILD''. DONT USE THE 'BUILD CONFIG' FOR CHECKING 'OC LOGS'

# 'IMAGE STREAM' IS THE REPOSITORY OF STORING 'IMAGE STRAM TAG(IMAGES WITH TAGS))'. WHILE CREATING 'DEPLOYMENT CONFIG' OR 'BUILD CONFIG' MOSTLY 'IMAGE STREAM'
# WILL BE CREATED AND IT PUTS THE RESULTANT IMAGE IT CREATED FROM DOCKERFILE IN THE GITHUB IN THE 'IMAGE STREAM' WITH TAG ATTACHED TO IT (IMAGE STREAM TAG)'




# building 'webhooks'


![image](https://user-images.githubusercontent.com/80065996/157841062-5079e0e1-0651-4519-86ed-13c398475ba0.png)


![image](https://user-images.githubusercontent.com/80065996/157842564-680ec517-8738-48e9-8add-dbe9457f7fce.png)


![image](https://user-images.githubusercontent.com/80065996/157843170-cb042a3e-55b0-4649-b6c9-2e42d0256d09.png)


![image](https://user-images.githubusercontent.com/80065996/157843337-ef32c93b-be35-477c-98cf-e437258e7878.png)


![image](https://user-images.githubusercontent.com/80065996/157843517-54a4a89e-757d-416a-80cc-2bef7d104564.png)


# IF YOU GET THE YAML, WE CAN GET THE 'SECRET' UNDER 'TRIGGERS' SECTION 


![image](https://user-images.githubusercontent.com/80065996/157844032-5df98f14-99fd-4f2e-a219-8f13284d23d9.png)


# take the 'generic secret' from the yaml we have created.


![image](https://user-images.githubusercontent.com/80065996/157844151-9d94fbc2-d9aa-4bea-9522-d80b35745899.png)


![image](https://user-images.githubusercontent.com/80065996/157844263-2817c535-e91e-43dc-b029-cdaf061e5fb8.png)



![image](https://user-images.githubusercontent.com/80065996/157846387-1000c341-27b6-450a-adac-dcad44acfe12.png)


![image](https://user-images.githubusercontent.com/80065996/157846997-1705759f-691e-4411-bcc5-c71bdc5527dc.png)


# we cannot manually create a 'webhook' for this demo. because for that we need git to be hosted in some public server. that is not possible now.
# instead we can mimic the 'code commit' sceanrio by taking 'secret' value by creating YAML file out of 'build config' command. (from the YAML file, take the secret value
# from the 'generic' section). 

# next using the 'describe' command for 'build config', we can take the 'URL' of the github webhook. After that simply run a POST request using CURL,
# by using a 'secret' we got from the YAML file


![image](https://user-images.githubusercontent.com/80065996/157851284-afee63b9-a3ba-4d29-80fc-a00705d0168e.png)


![image](https://user-images.githubusercontent.com/80065996/157851378-71ba89f8-c45b-45c0-9724-cfa1ccdeae49.png)


![image](https://user-images.githubusercontent.com/80065996/157851439-b8bb0510-9d4b-44e4-978b-b585938df54f.png)


# we mimic the simple POST command.  you can see in 'webconsole' sandbox, new 'build' is started. 


![image](https://user-images.githubusercontent.com/80065996/157851575-c80dd131-8c64-475e-805f-1aa5a2066288.png)



# in the same mechanism 'webhook' will be set up, for any of the code commit, new 'build' will be started.


![image](https://user-images.githubusercontent.com/80065996/157851999-03ab90b1-0006-44d7-8205-24e6b8d26ef1.png)


![image](https://user-images.githubusercontent.com/80065996/157852136-68c1c5f1-e406-4421-8bdb-fd565baa83e7.png)


# cleaned the openshift cluster and created 'new-build' for 'update-message' branch in the git.(previously we did for master branch)


![image](https://user-images.githubusercontent.com/80065996/157853039-682743c9-e0bb-4969-b20e-e50c84f4bd00.png)



![image](https://user-images.githubusercontent.com/80065996/157854546-84c5c5dc-8023-406b-b3c1-b464da6ead6d.png)


# now 'build','build config', 'image stream' and 'image stream tag' are created using 'update-message' branch from 'gitlab'.
# build take code, build it and created the image and tage it and put inside the 'image stream'



# How to build a sub directory from the 'github' repository


![image](https://user-images.githubusercontent.com/80065996/158127900-fff24976-0d59-4ae8-9e76-93ae5840274d.png)


# Goal of this demo is to build the code present under the particular sub directory (example: take this 'hello-world-go' directory from this repo)
# this is same as ' bit bucket will have many 'repositories' under the 'project' option'. so we are going to create a build only for a partiuclar folder under it(parituclar repo)


![image](https://user-images.githubusercontent.com/80065996/158128776-40128110-44d2-4bcf-9181-672ec3eff184.png)


![image](https://user-images.githubusercontent.com/80065996/158129235-a71dc854-551a-4777-8598-cbbc07ba0a0f.png)


![image](https://user-images.githubusercontent.com/80065996/158130128-e9b17817-f3b1-4542-b88f-fd2269a791af.png)


![image](https://user-images.githubusercontent.com/80065996/158130235-85f5ca98-d092-4937-8a23-5220b49204bc.png)


![image](https://user-images.githubusercontent.com/80065996/158130548-367358f4-8764-4fef-a243-ab23ac643d3f.png)


# NOTE: Usage of the URL in the above demo will be the root URL of the gitlab or bit bucket. From that we mentioned a directory (repo inside the project incase of bitbucket)


# Configuring 'Build hooks'


![image](https://user-images.githubusercontent.com/80065996/158131104-b5fb3b88-3ae7-488d-ace6-6c10745cc9b2.png)


![image](https://user-images.githubusercontent.com/80065996/158131241-288e7e1c-8768-40fa-b73c-93106427078a.png)


# Using 'build hooks'


![image](https://user-images.githubusercontent.com/80065996/158131712-b5557413-0d84-4566-bf89-d45ae560edae.png)


![image](https://user-images.githubusercontent.com/80065996/158132937-ef5174e4-cbb9-48d8-b61f-e5c841efdb27.png)


![image](https://user-images.githubusercontent.com/80065996/158133338-52fa84bb-5206-4d6c-8d1e-bfaa1bb4934d.png)


# Updating 'build hooks' - post commit hook
# Default 'post commit hook' is to push the image to push the image built in 'image stream'


![image](https://user-images.githubusercontent.com/80065996/158135164-bed7bef2-cede-465e-9ff8-ace2ca6f81c0.png)


![image](https://user-images.githubusercontent.com/80065996/158136128-f267b5b6-2f37-4b54-8f88-606cc592e371.png)


# now we updated the 'default post commit hook'. You can check below - 'post commit hook' is updated


![image](https://user-images.githubusercontent.com/80065996/158136420-9f257587-3cc6-41df-aa21-15362e23b331.png)


# starting the build to see the updated 'post commit hook'


![image](https://user-images.githubusercontent.com/80065996/158136571-89aa23cc-d0fd-4e45-8c60-3491c41fd109.png)


![image](https://user-images.githubusercontent.com/80065996/158136992-f1a5b2c7-51d7-4b62-9a50-11d2775ddf5e.png)



![image](https://user-images.githubusercontent.com/80065996/158137069-7fb85dfb-f409-4fac-bd19-0464fb9f5431.png)


# setting another 'post commit hook' - making build fail manually by setting 'post-commit' hook


![image](https://user-images.githubusercontent.com/80065996/158137643-174e2db0-0dc8-4f49-9272-09e88e9d2781.png)


![image](https://user-images.githubusercontent.com/80065996/158140364-64614e60-8c6e-4fd1-9c82-595e3cb6b500.png)


![image](https://user-images.githubusercontent.com/80065996/158140758-76666c48-691f-4e20-81c6-94eaad39c712.png)


![image](https://user-images.githubusercontent.com/80065996/158140868-f2c47d26-2a4a-46b9-8f4d-510d52e5239f.png)


![image](https://user-images.githubusercontent.com/80065996/158140963-aa3b45e7-f823-45b6-843f-d2798033e16e.png)


![image](https://user-images.githubusercontent.com/80065996/158141921-ff4917dd-7451-4b59-9495-696c800244ac.png)


![image](https://user-images.githubusercontent.com/80065996/158142016-fe85b2c4-a31f-4ec6-93f1-2c4d08857933.png)


# removing the 'post commit build hook'


![image](https://user-images.githubusercontent.com/80065996/158142264-b46343ee-8541-4acb-b688-45d63d244561.png)


![image](https://user-images.githubusercontent.com/80065996/158142389-3191063b-8f27-45ae-b5c4-db6432e26294.png)


![image](https://user-images.githubusercontent.com/80065996/158142888-fbd7d3d5-fa89-404a-8900-ef3e0c0c8366.png)


![image](https://user-images.githubusercontent.com/80065996/158143164-0f2abc6e-9df2-4021-bedb-a105eb762ecb.png)


![image](https://user-images.githubusercontent.com/80065996/158143391-a6ba11a9-c0ed-4df7-bfa9-c37b1b9c5726.png)


![image](https://user-images.githubusercontent.com/80065996/158143553-02cc8a0f-79b6-48d4-8f06-1ec8adcdb296.png)


# This time after removing 'post commit hook', now you could see default hook executed which created 'image stream' and pushed the 'images' into 'image stream'


![image](https://user-images.githubusercontent.com/80065996/158143631-acdea054-0a72-4687-a954-7b06567ff454.png)


# S2I -source to image

# S2I is similar to 'Dockerfile'. 'Docker file' is the source to create 'docker images'. as the name suggests, 'source to image' is we should have some kind of data as a 
# source to create the images.
# Why we need S2I even if we have Dockerfile. s2I is redhat resource and we dont even need to use 'Dockerfile' to create the images. 
# S2I is by default integrated with 'oc new-app' command in openshift.


![image](https://user-images.githubusercontent.com/80065996/158150307-d96483f0-be43-4340-a7a8-82b638bc3033.png)


![image](https://user-images.githubusercontent.com/80065996/158150413-4000a0c2-45c4-451a-9752-1c20b0a4084e.png)


![image](https://user-images.githubusercontent.com/80065996/158150681-ae5d8729-4f27-4a52-a0d8-1d370cd1cb96.png)


![image](https://user-images.githubusercontent.com/80065996/158150818-5996bba4-d6eb-4a0f-86ab-2d82bae9eb2b.png)


# file going to be used for this demo,

# if you see this repository, there is no Dockerfile available. But we can use S2I resource of openshift to create the image even without Dockerfile


![image](https://user-images.githubusercontent.com/80065996/158153423-f104c5ee-e02d-49f3-9181-1a16d2ac2f2a.png)


![image](https://user-images.githubusercontent.com/80065996/158161660-8cbe3a4e-d599-4900-b6c8-cb89d06c1506.png)


![image](https://user-images.githubusercontent.com/80065996/158161708-05f58570-e04e-428d-ba75-7125e3e1f86c.png)


# from the above screenshots, we could see there are no 'Dockerfile' available for this 'Ruby on Rails' code. Lets use 'oc new-app' command
# to check how it works


![image](https://user-images.githubusercontent.com/80065996/158162612-2919549c-e09b-46a9-bcfe-8a2272f4c20e.png)


![image](https://user-images.githubusercontent.com/80065996/158162991-63a0eaa9-64bb-4fb7-895c-0b881ae38fd6.png)


![image](https://user-images.githubusercontent.com/80065996/158163942-9cc73d67-cfcb-428c-8672-bc9adaff6544.png)


# NOTE: as name suggests, S2I will get 'source code' of whatever the language and openshift will take the corresponding base image and build it and create the 
# 'deployment config' and create the 'service', 'image stream' and 'image stream tag' with the name of parent folder (lab) (project - incase of bitbucket)
# once you expose the 'SVC' created, Route will be created and you can access the website from outside of openshift cluster


![image](https://user-images.githubusercontent.com/80065996/158165653-1060dbf7-c1fb-40c2-98b4-6ada5293c4a3.png)


![image](https://user-images.githubusercontent.com/80065996/158165779-dbbdb37f-bc85-4e9d-af26-1887d1f837f2.png)


![image](https://user-images.githubusercontent.com/80065996/158165824-b70d9382-c348-4ecb-94ed-13ed69535c28.png)


![image](https://user-images.githubusercontent.com/80065996/158167007-d9e5f427-174a-4780-b7df-a081376919d2.png)


![image](https://user-images.githubusercontent.com/80065996/158167192-7e1b8bbe-2a8b-433c-a4ca-3d13ebad11f2.png)


![image](https://user-images.githubusercontent.com/80065996/158167298-5d3af5cc-669b-46d0-9ad6-0330c121ede4.png)


# How S2I auto detection works?


![image](https://user-images.githubusercontent.com/80065996/158168925-a4e0ea3a-1f5f-42c4-872d-13ef0a844f3e.png)


![image](https://user-images.githubusercontent.com/80065996/158169152-c920691c-dc17-4e31-8b53-ea9c1e084ed3.png)


![image](https://user-images.githubusercontent.com/80065996/158169257-e0e7e5c9-e7e7-4833-ad4b-16997530a1af.png)


![image](https://user-images.githubusercontent.com/80065996/158169476-3cf0af3d-6c43-47cc-97b6-0c477da7ea7c.png)


# Explicit ovverride on S2I - Mentioning Explicit builder image 


![image](https://user-images.githubusercontent.com/80065996/158170124-f1bb2a35-4f05-438e-adbc-58ba5aca53aa.png)


![image](https://user-images.githubusercontent.com/80065996/158171354-98302c00-02e8-4b7a-81d3-4b96511d8011.png)


![image](https://user-images.githubusercontent.com/80065996/158173522-1e5381f9-0071-4ed0-bfdb-4354cc1e6c40.png)


![image](https://user-images.githubusercontent.com/80065996/158174065-575c4c73-f981-4fe5-a820-5081d61a6cc2.png)


![image](https://user-images.githubusercontent.com/80065996/158174438-31ae84c3-ecad-4765-b086-d538309b0575.png)


![image](https://user-images.githubusercontent.com/80065996/158174574-b7f73f48-f44b-412a-8f38-de313138dbe8.png)










































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






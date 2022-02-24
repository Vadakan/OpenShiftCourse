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





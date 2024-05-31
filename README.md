# kerberos_setup_k8s
# Kubernetes Deployment with Kerberos, NFS, and MongoDB

This document provides a step-by-step guide to setting up a Kubernetes deployment for Kerberos with NFS and MongoDB . This setup includes creating and applying the necessary ConfigMaps, PersistentVolumeClaims, and deploying your Kerberos application. The application is configured to use a MongoDB instance for storage and an NFS server for shared file storage.

## Prerequisites

- [Minikube](https://minikube.sigs.k8s.io/docs/start/) installed and running
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) installed and configured 

## Step 1: Setup MongoDB

### 1.1 Create a MongoDB Deployment
- [mongoDBpv_pvc.yaml](mongoDBpv_pvc.yaml)
- [mongodeploy.yaml](mongodeploy.yaml)
### 1.2 Create a MongoDB Service
- [mongo_svc.yaml](mongo_svc.yaml)
## Step 2: Create ConfigMap for MongoDB
- [mongoconfig.yaml](mongoconfig.yaml)
## Step 3 : Setup NFS 
- [nfs-pv.yaml](nfs-pv.yaml)
- [nfs-pvc.yaml](nfs-pvc.yaml)

## Step 3: Setup the Kerberos Application Deployment
### 3.1 Create the clusterrole
- [clusterrole.yaml](clusterrole.yaml)
### 3.2 Create the Deployment and NodePort Service for the Application
- [factory.yaml](factory.yaml)
## Step 4: Verify the Setup
```
http://192.168.49.2:30090
```
<img src=login.png>
<img src=test.png>

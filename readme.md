# Flask-OBC App

Flask-OBC app helps non-OpenShift admin users to create Object Bucket Claims with OpenShift ODF for OpenShift AI data connection.

![App Screenshot](app.png)

## Overview

The app creates an Object Bucket Claim (OBC) in an existing project and adds `us-east-1` as the bucket region. The app outputs the following data:

- **AWS Access Key**
- **AWS Secret Key**
- **Bucket Name**
- **Bucket Region**
- **Bucket Endpoint URL**

The app is protected with Oauth Proxy. So you need to add permissions to the Openshift AI Admin to grant access

![Output Screenshot](output.png)

## Deployment Steps

1. Create a project named `flask-obc`.
2. Edit the deployment and route YAML files with the cluster API URL and `*.apps` URL.
3. Apply all YAML files.

## YAML Files

- [deployment-oauth-proxy.yaml](deployment-oauth-proxy.yaml)
- [flask-obc-oauth-config.yaml](flask-obc-oauth-config.yaml)
- [flask-obc-service.yaml](flask-obc-service.yaml)
- [oauth-sa-secret.yaml](oauth-sa-secret.yaml)
- [oauth-sa.yaml](oauth-sa.yaml)
- [oauth-service.yaml](oauth-service.yaml)
- [rb.yaml](rb.yaml)
- [role-flask-obc.yaml](role-flask-obc.yaml)
- [route.yaml](route.yaml)
- [sa-secret.yaml](sa-secret.yaml)
- [sa.yaml](sa.yaml)
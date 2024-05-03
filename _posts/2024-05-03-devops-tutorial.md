---
layout: post
title: "Deploying apps to kubernetes using GHA - part 1"
---
Deploying apps to kubernetes using GHA

Steps:

1. Dockerize app(s)
2. Deploy kubernetes
3. GHA CI/CD
4. Add Kubernetes resources to enable CI/CD from GHA
5. Set secrets values to repository
6. Deploy app to kubernetes using GHA
7. Publish app - deploy `ingress-nginx` to kubernetes
8. Enable secure access to app - deploy `cert-manager` to kubernetes and set DNS


# Tasks

1. Dockerize app(s):
- find a couple of simple apps or write your own
- create a git repository
- write Dockerfiles and push them to the repository
- build and push them to a registry server

2. Deploy kubernetes:
- create an instance in Aws EC2 from the web UI
- install all required packages and deploy `kind`
- set security groups(ec2) to expose required ports if required
- test kubernetes API access from your machine

3. GHA CI/CD
- create workflow files in GitHub repository
- add step to build the apps
- create docker server token (dockerhub) to be used in the workflow

4. Add Kubernetes resources to enable CI/CD from GHA
- create the following resources:
  * `namespace`
  * `serviceaccount`
  * `token`
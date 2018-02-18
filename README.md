
<img src="https://ace-docs-production-red.ng.bluemix.net/docs/api/content/homepage/images/containerServiceIcon.svg" width="200"> <img src="https://kubernetes.io/images/favicon.png" width="200">
# Developer Works Lab: IBM Bluemix Containers Service and Kubernetes


# Disclaimer
This lab is meant to be used with the IBM Containers Service Course. I wrote this with other IBMers while still employed with IBM, and I believe they have made a much better course from this work, which can be found [here](https://github.com/IBM/container-service-getting-started-wt) All code is provided as-is, and I will not be updating it further. Please use the wonderful link above and go learn yourself some IBM Containers with the IBM Cloud!




# Overview and Initial Setup

Preconditions:  This lab expects a paid IBM Cloud account.  Running from the cli expects that you will have the clis installed as well, as per https://console.ng.bluemix.net/docs/containers/cs_cli_install.html . If you do not yet have a IBM Cloud account or the kubernetes cli, please do [lab 0](https://github.com/colemanjackson/container-service-getting-started-wt/tree/dwworks-additions/Lab%200#lab-0-getting-the-ibm-bluemix-containers-service) before starting the course.

This lab is an introduction to  using Docker containers on Kubernetes in the IBM Containers Service. By the end of the course
you will understand the core concepts of Kubernetes, and be able to deploy your own applications on Kubernetes or the IBM Cloud Containers Service. 

If you haven't already, provision a cluster (this can take a few minutes, so let it start first). To get the list of data centers, use `bx cs datacenters` - then create your cluster with `bx cs cluster-create --name=<name-of-cluster> --datacenter=<datacenter>`

After creation, before using the cluster, make sure it has completed provisioning and is ready for use. Run `bx cs clusters` and make sure that your cluster is in state "deployed".  Then use `bx cs workers yourclustername` and make sure that all workers are in state "deployed" with Status "Deploy Automation Successful".  Make a note of the public ip of the worker!

#  Lab Breakdown

There are nine stages to the Lab, including an optional advanced lab and a getting started lab.

[Lab 0](https://github.com/colemanjackson/container-service-getting-started-wt/tree/dwworks-additions/Lab%200#lab-0-getting-the-ibm-bluemix-containers-service) (Optional): Provides a walkthrough for installing IBM Cloud command-line tools and the Kubernetes CLI. You may skip this lab if you have the containers-registry plugin, the IBM Cloud CLI and Kubectl already installed on your machine.

[Lab 1](https://github.com/colemanjackson/container-service-getting-started-wt/tree/dwworks-additions/Lab%201#lab-1---set-up-and-deploy-your-first-application): This lab walks through creating and deploying a simple "hello world" app in Node.JS, then accessing that app. 

[Lab 2](https://github.com/colemanjackson/container-service-getting-started-wt/tree/dwworks-additions/Lab%202#lab-services-replica-sets-and-health-checks): Builds on Lab 1 to expand to a more resilient setup which can survive having containers fail and recover. Lab 2 will also walk through basic services you need to get started with kubernetes and the IBM Cloud Containers Service

[Lab 3](https://github.com/colemanjackson/container-service-getting-started-wt/tree/dwworks-additions/Lab%203#lab-3-deploy-an-application-with-bluemix-services): This lab covers adding external services to a cluster. It walks through adding integration to a watson service, and discusses storing credentials of external services to the cluster.

[Lab 4](https://github.com/colemanjackson/container-service-getting-started-wt/tree/dwworks-additions/Lab%204#highly-available-deployments-with-the-ibm-bluemix-containers-service) (Under Construction, Paid Only, Optional): This lab will outline how to create a highly available application, and build on the knowledge you have learned in Labs 1 - 3 to deploy clusters simultaneously to multiple availibility zones. As this requires a paid IBM Cloud account, you may skip this lab if you are sticking to the free tier.

[Lab 5](https://github.com/colemanjackson/container-service-getting-started-wt/tree/dwworks-additions/Lab%205#security-with-the-ibm-bluemix-containers-service): This Lab walks through securing your cluster and applications using network policies, and will later add leveraging tools Vulnerability Advisor to secure images and manage security in your image registry.

[Lab 6](): This lab walks through using Instana for CI/DC montioring and network patrolling of your cluster

[Lab 7](): This lab walks through the Kubernetes ecosystem to introduce you to node visualizers like WeaveScope, and package content handling with Helm.

[Lab 8]() (Under Construction): This lab walks through Microservice architecture at large, and provides a jumping off point to learn Istio!

---
layout: post
title: Questions about Deploying to AEM
---
In my 8 years of working with AEM, deployments have been a significant part of that work. I have worked with a lot of organizations either handling the deployments directly, or helping them with Cloud Manager. There has been a tremendous effort to minimize the work created by deployments by introducing a CI/CD process to AEM. If you are trying to figure out how best to handle deployments into AEM, there are some things you need to consider.

## Automated deployments are a redesign of an equivalent outcome.
If you read the documentation about Cloud Manager on Adobe Managed Services, and Cloud Manager on AEM as a Cloud Service, you should notice that the two processes are very different. One CI/CD process deploys to a running instance that almost never goes down, and another builds an immutable image to run in containers that are rebuilt on every full-stack deployment. Why does this matter? It matters because the difference has an impact on business timelines, deployment windows, "rollbacks", and every other factor related to pushing code into production.

The key distinction between AEM deployments vs AEM as a Cloud Service, in my opinion, is that Cloud Manager deployments on AEM as a Cloud Service is the only method that provides an opportunity to validate that the business requirements of a deployment are met. How does it do that? With custom functional and UI testing. If a devops engineer runs a deployment, the only concern they have after a deployment has completed is if the instances are up, the bundles are started, and the site is available. However, the whole point of deploying new code is to see new code. If you are using custom functional and UI testing you can verify that everything is functional on the stage environment, and if it's not the deployment doesn't move forward **because the business requirements weren't verified**. 



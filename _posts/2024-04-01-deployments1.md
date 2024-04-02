---
layout: post
title: What is a successful deployment?
---
If you are an organization using AEM as a Cloud Service there are a number of items regarding deployments that need to be carefully considered. Instead of running as a monolithic VM, AEM as a Cloud Service builds immutable images that can be deployed instantly to auto-scale and self-heal. This means a code deployment is building images, not just deploying packages one after another. With those as key principles, it changes how you should consider whether a deployment was successful or not. 

The first question to consider is what does your organization consider a successful deployment? Is it just that the service is up and running when the deployment is finished? Most likely not. A good deployment means there's no errors during the execution, all the services start, **and** the features and improvments work as expected. 

AEM as a Cloud Service is very good at having deployments complete successfully, but what if the features or improvements aren't quite right, or broken? Someone running the deployment is good, but if the business owners say things aren't fixed how do you address that scenario? I think the reactive options are:

1. Fail forward with a hotfix
2. Rollback the deployment

These are both reasonable options, but they are both approaches that keep an organization in a reactive mindset, and always concerned about the worst-case scenarios. Between the lines, it also means the QA/testing isn't really trusted.

The 3rd option to make sure features and improvements are valid on a deployment is to **improve and automate the testing**. With any AEM deployment using Cloud Manager, you can wait for approval on a production deployment while you smoke test the deployment, or have an external system do the testing. In AEM as a Cloud Service, you can include custom functional or UI tests in the project that will run after the code is deployed with a new image. If a custom functional or UI tests fails, it's a much better situation to be in than finding out after a deployment has gone all the way to production that something is wrong. A deployment that fails because of failed custom test, is a successful deployment. 

As you look to migrate to AEM as a Cloud Service, make custom testing a significant part of your deployments. They will make deployments more robust, more successful, help your organization be more pro-active, and build confidence that your QA process will spot issues long before they reach production. 



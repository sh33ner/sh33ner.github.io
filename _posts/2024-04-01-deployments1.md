---
layout: post
title: What is a successful deployment?
---
If you are an organization on AEM as a Cloud Service there are some key distinctions about deployments that need to be carefully considered. Instead of running as monolithic VMs, AEM as a Cloud Service builds immutable images that can be deployed instantly to auto-scale and self-heal. This means a code deployment is building images, not deploying packages one after another. That means that if you deploy non-working code to production, you can't just uninstall a package or go to a previous version of a package on every instance. You need the last successfully deployed code to be running.

If you think about this, it should get you to raise a number of questions that I'm going to explore in this and future posts. 

The first question to consider is what does your organization consider a successful deployment? Is it just that the service is up and running when the deployment is finished? Most likely not. A good deployment means there's no errors during the execution, all the services start, **and** the features and improvments work as expected. 

AEM as a Cloud Service is very good at having deployments complete successfully, but what if the features or improvements aren't quite right, or broken? The reactive options are to 1) fail forward with a hotfix, or 2) rollback the deployment. These are both reasonable options, but the pipelines in Cloud Manager are meant to prevent these from even happening. If your organization only ever focuses on worst-case scenarios, it's likely because the QA process isn't automated enough to build confidence that the validation of a deployment is thorough. There is an option that is more pro-active and less re-active.

A 3rd option to make sure features and improvements are valid on a deployment is to **improve and automate the testing**. With any AEM deployment using Cloud Manager, you can wait for approval on a production deployment while you smoke test the deployment, or have an external system do the testing. In AEM as a Cloud Service, you can include custom functional or UI tests in the project that will run after the code is deployed with a new image. If a custom functional or UI tests fails, it's a much better situation to be in than finding out after a deployment has gone all the way to production that something is wrong. A deployment that fails because of failed custom test is a successful deployment. 

As you look to migrate to AEM as a Cloud Service, make custom testing a significant part of your deployments. They will make deployments more robust, more successful, help your organization be more pro-active, and build confidence that your QA process will spot issues long before they reach production. 



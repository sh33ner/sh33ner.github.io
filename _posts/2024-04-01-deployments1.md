---
layout: post
title: 
---
If you are an organization on AEM as a Cloud Service there are some key distinctions about deployments that need to be carefully considered. 

Instead of running as monolithic VMs, AEM as a Cloud Service builds immutable images that can be deployed instantly to auto-scale and self-heal. This means a code deployment is building images, not deploying packages one after another. If you deploy non-working code to production you can't just uninstall a package or go to a previous version of a package on every instance, because if the orchestration layer has to start up a new instance it's going to use the code that was just built. 

The production pipelines for AEM as a Cloud Service only deploy to Stage and Production together. In my former experience, a major point of struggle was when the experience on stage was different than production. Tying them together with a pipeline is meant to mitigate that problem. However, being tied together does not inherently solve that problem. 

There are still cases where a production deployment could be built, go through code quality, go through the unit tests, go through smoke-testing on stage, and still result not be considered a successful deployment. So, knowing that AEM as a Cloud Service uses immutable instances, and knowing that the production pipeline is meant to have a complete mirror of the code in stage before production what would be a reasonable way to prevent having to do a rollback? Increasing the testing.

You can use your own tooling to get Cloud Manager events and trigger testing to happen as soon as the stage deployment is complete, or you can include custom functional or UI tests directly in the project code. (This has some significant advantages outside of just validating your deployment.) Increasing the automated functional or UI test ideally would reduce how much "smoke-testing" has to be done while also continually adding coverage that your componenets and features work as expected. 

When you consider the immutability changes to AEM as a Cloud Service, and the tight coupling of stage and production together, you can see how an organization needs to carefully consider these changes to drive success for their organization.

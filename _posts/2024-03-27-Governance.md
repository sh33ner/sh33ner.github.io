---
layout: post
title: Screws and Rivets
---
In my work with AEM as a Cloud Service, one of the frequent topics of discussion with organizations is on the best practices for deployments. This process has drastically changed in the last 9 years, and I think I have seen every concievable device used for managing deployments. Everyone has their own schedule, regulations, and ideas on how these are supposed to work. Adobe has cosnistently driven towards giving customers the ability to deploy as regularly and reliably as they can according to their own time frame. Sounds pretty great to me.

Then why is this so frequently discussed? I think one reason is because many organizations just look at the release process, transpose their current deployment method into Cloud Manager and call it good. The problem is that using a CI/CD pipeline for deployments is not simply automating the deployment. It's not just deploying a package using the curl commands for crx package manager. There's quote that demonstrates this problem. In "The Art of Doing Science and Engineering: Learning to Learn", Richard Hamming wrote:

>When we first passed from hand accounting to machine accounting we found it necessary, for economical reasons if no other, to somewhat alter the accounting system. Similarly, when we passed from strict hand fabrication to machine fabrication we passed from mainly screws and bolts to rivets and welding.
>
>It has rarely proved practical to produce exactly the same product by machines as we produced by hand.
>
>Indeed, one of the major items in the conversion from hand to machine production is the imaginative redesign of an equivalent product. Thus in thinking of mechanizing a large organization, it won’t work if you try to keep things in detail exactly the same, rather there must be a larger give-and-take if there is to be a significant success.

The automation of the deployment for AEM as a Cloud Service requires there to be a "larger give-and-take if there is to be significant success." 

So what does that mean? And what can I share that can help you in this?

---
layout: post
title: Governance and CI/CD Pipelines
---

## The Knife Versus The Meat Slicer

Imagine for a second that you own a deli, and that your method of slicing meat at this deli is with a tried and true knife that is perfectly sharp and which you have sliced thousands of meats with. Business starts to pick up, and I can see you're not getting as much done as you could. I come to you with a meat slicer that allows you to slice 4 or 5 times the amount of meat with perfect consistency just like your knife. You now have the capacity to increase business, the speed of delivery, without sacrificing the quality you used to use with your trusted knife. And then you say, "I can't use that slicer." 

"Why", I ask?

"Because the blade on it isn't straight. It's a circle." 

It would seem ridiculous to not try the meat slicer, but we tend to look at any machine or system that automates a task the same way. Richard Hamming addressed this same idea in his book "The Art of Doing Science and Engineering: Learning to Learn". He wrote:

>When we first passed from hand accounting to machine accounting we found it necessary, for economical reasons if no other, to somewhat alter the accounting system. Similarly, when we passed from strict hand fabrication to machine fabrication we passed from mainly screws and bolts to rivets and welding.
>
>**It has rarely proved practical to produce exactly the same product by machines as we produced by hand.**
>
>Indeed, one of the major items in the conversion from hand to machine production is the imaginative redesign of **an equivalent product**. Thus in thinking of mechanizing a large organization, it won’t work if you try to keep things in detail exactly the same, rather there must be a larger give-and-take if there is to be a significant success.

In my world with Adobe Experience Manager, the number one place I see this kind of thinking block progress is with deployments and moving to a CI/CD process. What are the details that an organization gets focused on maintaining, and what is the "give-and-take" that has to take place for an organization to move forward with a good CI/CD process? 

## 1. Release Cadence
Although it's obvious, many organizations never have a discussion internally when using a CI/CD process about changing their actual release cadence. They may move to using CI/CD pipelines, but may still be required to only deploy to production once every two weeks. 

So what gives? Why would this happen? 

Because the people running deployments in a CI/CD pipeline have not proven yet that they can be trusted doing more frequent changes. If you're in an organization that deploys to production on Fridays, and every Friday night people are working late because of errors in a deployment, no one in the right mind would let you run one every day. Your CI/CD process is going to have to be build up a lot of credibility. Well, how is someone supposed to do that?


## 2. Testing
The key is to focus on pro-active work, rather than re-active. Pro-active work means writing such smart automated testing, that it will block any problems with a deployment. That's the only way to help an organization build confidence enough to let a CI/CD process run either daily or on every commit to production.



## 2. Testing

## 3. Controlling the Wild West

## Conclusion

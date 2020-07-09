Effective Feature Management

Instead of coding if statements, using some variable in a configuration, and needing to restart an app - modern feature management works differently.

Benefits include: 
* decoupling the act of deploying from the act of releasing.
* eliminating / minimizing teams being stuck in long-running feature branches.
* business can take advantage of progressive delivery (strategically controlling when individual users or user segments gain access to new features).

2 parts:
* passing in a context (can contain anything)
* the feature management platform is called out - passing the context and using a set of business rules to determine which code path is executed.

this makes the behavior of the function dynamic, changing whenever the rolllout rules are changed.  No need to redeploy.

FF can be temporary or permanent.

With temporary - we can do A/B testing, test new behaviors against old ones, and after a flag is being used by 100% of users, flag is intended to be removed.

Permanent flags allow us to control behavior at any time.  You could:
* create a kill switch
* reveal functionality only to specific users

You can create a release strategy.  Some questions that the team can ask include:
- [ ] How will the feature be released? 
- [ ] Should anyone see it now? 
- [ ] Who will be getting this feature first? 
- [ ] Who will beta test it? 
- [ ] Will it be rolled out progressively? 
- [ ] Do I need to compare it against the old behavior? 
- [ ] Do I need to hit a particular date for an external event? 
- [ ] What do I do if something doesn’t go right?

Concept of testing in production

in a microservices world, it becomes increasingly difficult to replicate a production environment for testing when you take into account variables that affect performance and processes in general, such as:
* volume of messages
* volume of transactions
* volume of traffic
* volume of data

Even if you could replicate this production scenario, now you are talking about an expensive test environment.  

So - the staging server is being discouraged in favor of the production server for these reasons.

Patterns used for safely testing in production:
* Canary releases
* ring deployments
* percentage rollouts

(blue/green deployment is where you cut over completely.  You actually have 2 prod environments, one with the new and one with the old - allowing you to rollback if necessary. )

Monitoring is key here, of course.  You must understand the impact of a rollout change.  

Netflix engineers are encouraged to test new code in production instead of an artificial staging environment. They use percentage rollouts, have strong guidelines on how tests are set up, and are always monitoring so that it can stop experiments before anything has a significant impact on customers.  

Percentage Deployments
* small numbers of users are selected randomly to experience a new feature.  
* gradually, the number is increased
* useful when there is little variation in targeted user base, or you are more concerned with the operational impact of your change.
* e.g. was a social media company that tested a new caching strategy on a small number of users to tweak performance before rolling out to wider audience and eventually everyone.  

Ring Deployments
* strategy of first deploying to internal users.
* after success there, expose the next set of users, the canary group.
* Teams use canaries to measure reaction from real users in production and look for early indicators of danger or success
* the 3rd ring - beta testers or early adopters.
* then - general release.
* Or - you may segment to different types of users, or different geographies.


Flag early - and Often 
* anything can be a feature, not just a customer-facing feature.  
* many teams have too narrow a definition of what they can feature flag.  
* 

Safety Valves / Circuit Breakers
* enabling non-essential features of an app to quickly disabled if they increasing in latency.  e.g. product recommendations or reviews on an ecommerce site.
* these are permanent flags
* must be properly documented so they are not accidentally removed.
* baking in these safety valves to incident mgmt. processes as appropriate so relevant communications are triggered.
* initially - they can be manually managed, but eventually you want to automate them.  Error monitoring or other metrics should trigger them. 
* BEWARE - the false positive.  ensure you are monitoring properly.
* Kill Switch example - ecommerce company lost millions on Black Friday bec/ they could not disable non-essential features which created a complete outage.

Infrastructure Migrations
* You could manage ( in a set of multiple steps ) the risk of doing things such as: 
    * database schema changes
    * vertically scalling a database
    * changing cloud service providers
* e.g. upgrading to new version of ElasticSearch
* 








References:
* Effective Feature Management - LaunchDarkly. 


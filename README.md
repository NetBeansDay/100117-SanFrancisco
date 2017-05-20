# NetBeans Day San Francisco 2017

7 slots with 30 minute breaks, in principle, though we may get more and we may get split tracks.

   * 08:00 - 08:45
   * 09:15 - 10:00
   * 10:30 - 11:15
   * 11:45 - 12:30
   * 13:00 - 13:45
   * 14:15 - 15:00
   * 15:30 - 16:15
   * 17:00 OpenWorld Keynote
   
We'll probably be able to start later and split into two tracks, like last year:

https://netbeans.org/community/articles/javaone/2016/netbeans-day-2016.html
   
Proposed content for NetBeans Day.   

   * "Apache NetBeans"
      - ID: UGF6160
      - Speakers: Mark Stephens, Florian Vogler, Constantin Drabo
   * "Java in Space: James Webb Space Telescope Flight Dynamics Ground System"
      - ID: UGF6161
      - Speakers: Sean Phillips and team
   * "Breaking up the Monolith with Jigsaw" 
      - ID: UGF4400
      - Speakers: Johannes Weigend, Sven Reimers, Jens Deters, Martin Klaehn
   * "Java Performance Tuning with Free Tools"
      - ID: UGF6163
      - Speakers: Kirk Pepperdine
   * "Confessions of a Java Educator: What I Wish I Had Known Earlier"
      - ID: CON5169 (to be converted to UGF)
      - Speakers: Ken Fogel, Zoran Sevarac, Gail Anderson, Paul Anderson
   * "Docker for Java Developers"
      - ID: UGF5805
      - Speakers: Arun Gupta, Fabiane Nardon
   * "Rapid Development Tools for Java EE 8"
      - ID: UGF3883
      - Speakers: Gaurav Gupta, David Heffelfinger, Ivar Grimstad
   * "Rapid Development for Web and Mobile with Oracle JET"
      - ID: UGF4508
      - Speakers: Andrejus Baranovskis
   * "Rapid Node.js Development with NetBeans"
      - ID: To Be Done
      - Speakers: Ryan Cuprak
   * "Single-Page Web Apps in Plain Java with Vaadin"
      - ID: UGF2367
      - Speakers: Matti Tahvonen
   * "Enterprise Cross-Platform Mobile Applications with Gluon"
      - ID: UGF4122
      - Speakers: Johan Vos, Jose Pereda
      
If there are too many in the list above, depending on the allocation assigned to NetBeans during Community Sunday, we'll submit some of the above to the main conference.      

Sessions in the main JavaOne/OpenWorld conference connected to NetBeans.

   * TUT1931: Goin' Mobile: Developing JavaFX Apps for IOS and Android with Java 9
   * CON5168: Java Desktop in the Wild for Science and Analysis: Sean Phillips, Geertjan Wielenga, Rob Terpilowski, Chris Heidt, Thierry Danard
   * CON2887: Transforming a Java-based Desktop Application with Jython: Thierry Danard
   * CON4389: Oracle JET in the wild - how and why organizations are using JET for their UIs: Lucas Jellema
   * CON2367: Single-Page Web apps in Plain Java with Vaadin: Matti Tahvonen
   * CON5172: JavaScript: Does It Make Sense In Large Web & Mobile Apps?: Geertjan Wielenga
   * ...
   * ...
   * ...
   
Reviewers for Java Development Tools Tracks

   1. Anton Arhipov
   1. David Heffelfinger
   1. Fernando Babadopulos
   1. Gerrick Bivins
   1. Ixchel Ruiz
   1. Josh Juneau
   1. Leanne Scheepers
   1. Markus Eisele
   1. Max Andersen
   1. Melissa McKay
   1. Patrycja Wegrzynowicz
   1. Rabea Gansberger
   1. Zoran Sevarac


https://www.youtube.com/watch?v=cYdgMnH45qQ

I deal mostly with tools for developers. Both development tools and infrastructure tools for developers. 

In this session, I am going to share some of the lessons we learned when we build our own tools. Those are lessons, actually, from our own development teams that are building products. 

Specifically those are lessons around how to do agile team development and a little bit of DevOps as well, using a Cloud environment. 

1:00 Cloud --------------------------------------

So, at Oracle, just like you, we have a bunch of software developers that are building products. Several years ago we made a transition of our products to become Cloud products. This brought along a bunch of changes in the way that we needed to develop software. 

- One key aspect is release frequency. When we did on-premise products, most of our products would have a big release once a year, maybe some patch release every half a year or something like that. And then people would actually pick it up on their own time. You would release something and then you would still find people using the release that you produced four years ago on premise. In Cloud, everything moves much faster. We are able to release software, basically, once a month. We have a timeframe where we can update the Cloud and then all our customers get this new version of the product.

- One other thing that changed for us is the level of quality that we needed from our product. We needed to have high quality of the software before as well, but in a Cloud environment, we're hosting everything and we are multi-tenant, so we have one product serving multiple customers. If you have a bug, it's going to impact a lot of people. The software needs to be very stable, very secure, because multiple people are using the same instance. In a lot of aspects, the quality of the software has been increased in terms of the demand from us.
- The speed of needing to be able to find a bug and fix it, again, we needed to increase this.
- We also changed a lot of our development technologies. When we used to do on on-prem products, we used to do a lot of things like in C and C++ and Java and stuff like that. We still do a lot of Java in the Cloud, but we're also seeing a lot of products that are now doing stuff with Node.js at the backend, where a lot of our products in terms of the frontend are now based on JavaScript, HTML5 type of UIs. And, again, various types of backends, whether its Node.js or Java or sometimes it's directly against the database. So, the development technologies, the variety of them, inside Oracle has increased. 
- The development process is also something that's changed for us. 
3:00 Agile --------------------------------------
We moved to adopt an agile development methodology. The reason we moved to agile is because it allows us to address a lot of the requirements in the previous slide.
Agile, there's a lot of books that you can read about it, there's a lot of websites that give you a deeper understanding of agile. I usually try to summarize it in 4 main points of what we're trying to achieve with agile. 

- We want to have short delivery cycles and build the product in an incremental mode. So, rather than building the whole product, which is what we used to do, we would go out, build a product like all the features that we could think about and then we would ship it. In the Cloud, and in agile, we actually start with what we call the MVP, the minimal viable product, and we put it out there, and then based on the feedback that we get from customers, who are actually using it, we then add more features. And we add more features in a very quick way. Every couple of months you're going to see new features appearing in the product, rather than once a year or something like that.
- The other thing that agile gives us is the ability to change our focus on which features and which fixes and stuff like that we are targeting, very dynamically. So, based again, we put a product out there and people are using it. We get feedback and sometimes it completely changes what we thought would be our focus for the next release. We see a lot of people demanding a specific feature, we are going to focus on that one. So, there is constant shift and adaptation on our side in terms of the product that we are delivering and what it does in the next release.
The releases are more frequent, features are changing all the time, this is agile. To some degree it introduces a lot of uncertainty and a sort of a mess into your development process. Some people like the old approach where you would go out and at the beginning of the project you would plan everything for the next two years and then you would go for two years and you write everything then and you deliver the project and the product. But, in today's world, if you start a project and then deliver a year after that, everything is changed during this year, in terms of what people need and what they expect and even the technologies. So this is what agile gave us.
6:00 DevOps --------------------------------------
Now, something that is not agile but relates to agile, is the concept of DevOps. So I did the lazy thing and I copied the definition of what DevOps is from Wikipedia. And it's a long sentence and you can read it, but I highlighted a few things. The first thing is that a lot of people, when they talk about DevOps, and also when they talk about agile, they talk about a cultural shift in how you do stuff. And yeah, there is this aspect of cultural aspects, and changing roles in the organization, and the way that you conduct meetings, and stuff like that.
Me, as a technical guy, I'm less interested in those aspects. I'm more interested in the actual software that is needed to achieve this. And if you actually look at the definition of DevOps again, they also talk about it as a culture and environment. The environment is actually the important part for me, which is I need a platform that allows you to do building and testing and releasing of software, very rapidly, very frequently and in a more reliable way.
Now if you look at the adjectives at the end there, things like "rapidly", "frequently", and "reliably", those are the same adjectives that agile is trying to achieve. This is kind of the connection between the two. We see DevOps as the way to achieve agile or as a mandatory thing that you need to have in order to actually be able to do agile development. 

By the way, DevOps talks about this circle of starting from planning your product, coding it, building it, testing it, releasing it, deploying it, operating it, and monitoring it. And based on the operation and monitoring and the feedback that you get, you'll continue to develop and add and stuff like that.
So those are kind of the goals we have. What I wanted to share in this session is to talk about how we actually do this. How we do agile and DevOps. 
8:00 DCS --------------------------------------
And I'm going to talk about one of our teams. So Oracle is, basically, you can think about it as a lot of smaller companies, each product is a company. And I'm going to talk about one product or one company that is called the Oracle Developer cloud Service. So, this is a team that right now has about 170 members in this team.
So the members in the team some of them of course are the actual developers. But members in the team are also the QA engineers, the doc writers, the product managers, the development managers, the vice presidents, well, things like that. 
In other words, there's 170 people that are involved in building this product. This is quite a large product in terms of scope. Thousands of lines of code. I'll talk about what the product does in the next slide. We're working in a two-week sprint approach, where we basically build the product in two week sprints. Every two weeks, we define what we are going to do in the next two weeks, focus on those tasks and do them.
So what is this Developer Cloud Service? It ties in nicely into the rest of the session because Developer Cloud Service is actually the product that Oracle uses to do agile and DevOps. Developer Cloud Service focuses on code management and continuous integration. So what it does, it basically gives you a code repository based on Git. It gives you build automation utilities with a bunch of frameworks, like Maven and Ant and Gradle, which are used by projects that do Java development at Oracle. It gives you things like NPM and Gulp and Bower for projects that are based on Node.js and JavaScript. It gives you utilities for testing, like JUnit and Selenium. JUnit is backend testing, Selenium is UI testing. It gives you FindBugs for code review. All of those utilities, together, gives us a platform for managing our code. All of them are integrated into a single product. This is used by multiple teams inside Oracle to build their software. By the way, the same platform that we use internally this is what we offer for customers. You can get Developer Cloud Service and use it to build your own and manage your own code. 
The other stuff that we are doing in Developer Cloud Service is managing the team in the development process. So in there there's a task tracking system or an issue tracking system. There's a bunch of utilities to manage the agile development process. So basically prioritizing stuff and managing sprints and getting reports and things like that. There is a platform for doing online peer code review, so multiple people can collaborate and comment on code pieces. And there's a Wiki for sharing things like design documents or documenting use cases, stuff like that. There's also something called Activity Stream, which is kind of like your Twitter or Facebook feed of what's going on today in the project. 
And, again, all of this is integrated into a single offering. Beyond that we provide integration with various development tools and I'm going to show you some of those today.
Sso this is what the product that we are building does. 
11:00 Source and Version Management --------------------------------------
And again this is all done as a single project. All of those features are in one product. 
- But what we did then is we a branched into 40 separate Git repositories. Each Git repository deals with one aspect of the product. You would have a Git repository for issue tracking and a Git repository for doing the build framework or a Git repository for the continuous integration engine. Then we manage all of those again because it's a single project with a one central place where we track tasking issues.
- So let's start by talking about how we do version management of our code. What we do there is we use a process called Git Flow which is a very popular approach to working with a Git repository. The idea there is that when a developer works on a new bug that he's fixing or when a new feature that he's working on, he's going to branch the code and create a local copy of the code that he's working on. In this case, the situation is where you will have a lot of those branches managed. But it also allows you to have a situation where if suddenly the priority changes and you need the developer to go and work on something else, he can just leave this branch on the side with the work that he did and branch to another focus area and work on that. So the developer works on the code and once he's comfortable with the code, he thinks he's finished the work on the specific feature that is working on, he can actually create a merge request, basically asking to merge the code from the branch into the mainline. 
- But before we actually do the merge, there's the process of code review. So the manager for this feature will review the code, see the changes, and we can also bring other people into the review not just the manager, and they do a kind of iterative interaction between the developers and his peers to get the code into the best best state basically. Once the code is approved, we run a bunch of automated builds, that actually take the code and make sure that it passes tests and things like that. And then we merge it back into the master. So this is kind of what we do when in terms of managing the codes for features and, again, if you look at our team we have about 200 commits of the code done per week. So this is quite a lot for this.
14:00 Release Management --------------------------------------
One special situation is when we are getting close to a release. When we're getting close to a release, we're actually branching from the master line of code and creating a separate release branch. This release branch is protected so you can't just merge things into there. Only specific people are allowed to say ok now we can merge something in there. This is in order to create the most stable release version. So, what we basically do in terms of changes in this release branch are only critical bug fixes. This is usually done like a week or something like that before a major release or something like that and then again all the automated builds work there. Once we are done and we have a stable release, we release it, and then merge all the changes, all the bug fixes, back into main.
That is kind of our process for doing this.
By the way, just so you know what to expect, I'm going to talk with slides about what we are doing for a while and then I'm going to actually show you how we're actually doing it. So I'm going to actually do the development process demo. 


15:00 Tips -- source management --------------------------------------
So some tips from outside on code management. 
- One aspect is that it's okay to have more than one repository for your code. As I said, we have 40 repos and the reason is that if your project is big and you're trying to manage everything in one place it's going to create a lot of overhead in terms of looking at all the code and browsing through it and stuff like that. It's easier to modularize stuff and then let your build system do the integration of the various models into the product that you deliver. So don't be afraid to have multiple Git repositories for one project. 
- We highly recommend this Git Flow process. For us it provides a lot of agility in the way that we build the product. This agility to say okay oops there's a critical bug that we need to fix, we're freezing for a second one branch, we'll branch into another thing we're working on, this very quickly finishish this merging it and then go back to what we were working on before. This is again you can google Git Flow to see a lot of tutorials on how to do it, a lot of documents, and we recommended to use it, it works for us pretty good.
- One key thing for us is this code review process. Code review, the aim there is to create a situation where we have better code not just in terms of readability or stuff like that but also in terms of the code quality, prevent errors, stuff like that. Peer programming and we automate code review. It's a required step for you when you're going to do before you actually merge something. One nice thing that we are also automating is we have a default code reviewer for each area. The manager for a specific part of the product has to do a code review before the gets approved. Beyond him the developer can ask to another peer of him to also review the code so we do all of this online. It is very easy to communicate and I'll show you how we do it later on.
- This best part is of branching main into a release before release helps you achieve in this world of agility and everything moving a little bit more stabilization before you actually release something. So do this if you want to actually create a little bit stability before you release a product.
17:00 Build process --------------------------------------
So this was how we manage our code and coding process. 
Then there's the build process. The build process, as I said before, there are automated commits, so automated builds that are fired based on commits. So when a developer commits his code, we require him to have a build process for his code that includes things like tests. Beyond those builds that are fired based on commits and merged into the main line, we also have twice a day an overarching build that takes all the components of the product, all the 40 Git repositories, and builds the product to all of them, bunch them together into a single product, and then deploys this product into virtual machines, which are basically running a version of our produc. Wwhen the version is running there, we are able to run additional builds that run automated tests on our product, UI tests and things like that.
In addition, when we have it over there QA can do manual tests. So the QA guys can actually go there and do that. So those are twice a day scheduled builds that we're doing. Usually one of them is at night, one of them is sometime in the morning. 

One thing to highlight here is the fact that our development team, those 170 people, they are spread all over the world. We have some of them sitting in the Oracle HQ in San Francisco, some of them are sitting in the Czech Republic, some of them are in the UK, some of them are in India. Some of them just work from home in various places. All of them are collaborating, checking in code and stuff like that and then the build basically gets this unified product out of it.
Also, every two weeks we take the master branch and we do a build on it. That basically creates the product, deploys it, runs automated tests, and also allows our QA guys to do manual testing on this. This is kind of our big two week end of sprint build, which basically is supposed to create our candidates for product release. Not every two weeks we are releasing, sometimes it's more like once a month or something like that. But this is actually how we produce the product, and at the end of the day you will get access to our Cloud.
20:00 Tips -- build process --------------------------------------
So, some tips from our experience about builds. 
- You want a notification going out from your build. It's kind of like you know like the question of if the tree falls in the forest and nobody hears, did it actually happen. If the build fails and nobody knows about it, it doesn't mean anything. So when a build fails, we send notifications to all the team to know that this happened. It also prevents the idea of I didn't know it was broken, things like that situation. 
- You need to require a test like we require a test as part of the build so every feature that is being big okay we're big believer in test driven development and when the developer produces the new features, he builds the test into it, and we automate it and include it as part of the build for this feature. 
- The fact that we do regular builds help us to more quickly realize there are problems. This twice daily build across the product helps us identify problems much sooner. When you identify a problem sooner in the development cycle, it's usually easier to detect what went wrong because it's something that happened in the last like half days okay and it is easier usually to fix it.
- There is no such thing as build overloads. What you need to remember here is the build is automated there's no person that actually works and does some thing. So you shouldn't be worried about having the computer do a lot of work for you. So doing those two builds a day or doing those little builds on every commit, don't worry about the fact that you're overloading the system. This is going to help you at the end of the day. I know that some people say okay we'll do one build per day. That's not the solution like when you need it run a build. In our case for example and we actually have a situation where there's almost no part of the day where our build servers are not doing something. We are not afraid to overuse.
- Another thing by the way that we are doing with build automation it's not just part of the release of the product. We're actually using the build automation to monitor the live application. We have watchdog builds that basically do things like check the performance and ping the URL and make sure that everything works okay and those are again part of our automation.
So this was a little bit about how we do agile and how we do continuous integration and delivery. 

22:00 --------------------------------------
I want to take you to the typical day of the various roles in our organization. So, again, I'll do it with slides and then I'll actually show you how it looks.
So I'm going to talk about one person who is the developer. 
What the developer usually does, the way that their day starts is that they get an e-mail about a new task Or feature that day are required to build or a bug that they need to fix. And this is how they know what to do. It's not every day that you get an email but it's usually when if something is assigned to them.
By the way if there is a situation where nothing is assigned to you today, it doesn't mean that you can go home. What it means is that we have a list of open issues with no assignment you go over there and you pick one that you know that you were able to work with and this is the one that you're going to work.
So you know the test that you're supposed to do today. Then you branch the code and you'll start working on your code.
By the way working on the code at Oracle means you can use any IDE you want. Oracle has an IDE called JDeveloper samo fellow developers use this some people use the clip some people use netbeans some people using telly j some people actually call directly in the cloud so if you being at the keynote in the morning they showed you this case we actually have a code base of coding as environments in the cloud so formula browser you can call 
Each one whatever suits him okay. At the end of the day all of those coding environments are connected to our gate repository so once you're done coding in your favorite environment you can actually commit and put the changes into the digital 
These files are built on your specific branch okay and if everything goes perfectly fine and you're ready with your code it past your yo test you go and you do a male's request mel's request initiate also a code review cycles and you do kind of iterative reviewing of the code. You get comments every comment gets you you get an email about it and then you modify your code again run the bills automatically. When everything is done and your code is the pool you merge it into the master and then you close the task Val kisses resolved okay and then you start all from the beginning pick up the next up and do this. 
So this is what a developer does. 
25:00 --------------------------------------
The DevOps guys. 
We actually don't have a lot of them because DevOps, all they do is like most of our DevOps is automated. so melty girl a build a unit tests are executed automatically our build produce a binaries that go into a maven repository will remain and roll our binaries it's a builds fails you get a notification. The scheduled builds that one every like a couple of times a day em when a bill is successful we notify a QA automatically a QA then goes in and can verify the things that will master's touch that were closed and actually closed the updates anybody that they are now closed after death 

We ran selenium UI testing automatically and I will develop guys what mostly what they do is okay they define the initial build files okay all the build processes but then what most of the time is spent on is actually monitoring, designing the environment. So their ops is instead of focusing on kind of the wasteful part of trying to take the code and move it along the chain it's actually they are focused on monitoring that our runtime platform is performing well in stable stuff like that. Which is what we want your ox guys to do you want to make sure that your runtime platform, your finished product is actually successful.

26:00 --------------------------------------
Let's talk about the development manager and what his day looks like. So one thing the development manager usually does in the morning is look at the Activity Stream, basically, look at what has happened during the night because, again, as I said, there are teams all over the world working on it in different time zones. So he looks at what has been happening and what new issues were reported, stuff like that, and then he goes over and he does issue management. So, he looks at the issues, he prioritizes them, he assigns them to people. He can click the status of issues, stuff like that. The next thing that he might be doing is look at merge request which are also code review cycles. 
Some of our managers are also acting as the sprint managers so they actually track the progress of the sprint, look at various reports and how are we matching our goals, stuff like that, and at the end of the day they are also the ones who are working on this release branch, that is, the protected branch that will go over and become our product. They are the only ones who are approved to approve actually merges into that one so they also do that. 
44:30 Conclusion --------------------------------------
Let's finish with a couple of slides, just to recap some of the things we've shown you today.
- This concept of having the agile part, the managing of the process of development, with DevOps together, is what gives us the power. Having those two things separately or just one of them doesn't is not going to work for you. Just having them together is something that is very powerful. 
- The fact that everything is in the cloud is so much simpler for us. It used to take us months to get an environment for building because we needed to buy the servers and the software and install everything and connect everything. Now the team at Oracle can get this full environment in a matter of two minutes. They put in a request, everything is provisioned for them in the Cloud, and they can start working. By the way you can do the same thing. 
- And then team collaboration is key for us. 
Here are some statistics about what we do, again, 40 Git repositories, 170 project members, 50 of them are actual coders 200 commits a week, 50 builds a day, over 20k of issues that are documented in our system and 250 Wiki pages that we use to share information among our team.
- What it gives us is full traceability. We can collect something from the issue being reported, to looking at how long it takes us to fix it, all the way to seeing the source code changes, the build that will fire, the deployment, everything is traceable.
- It gives us a faster feedback on our code commit because we get in immediate build and build success and test results.
- It improves our collaboration, you could see how easy it is to request a code review from someone, sharing the knowledge of the experts with the beginners, stuff like that.
- And we have a one stop shop for agile and DevOps.
- Accessibility, its cloud-based, you can go anywhere. Like I'm working in the hotel doing the same stuff that people in the office do. If you're on a vacation and you have a you checked in something that broke the build, there's no excuse, you can still access the code and fix it to our Cloud. Even if you don't have your laptop with you.
- And, as well, easy provisioning and scaling.
So if you want to try this on your own, you have a location for getting a trial environment or actually getting the cloud environment for the Oracle Cloud. We actually provision this product what you saw today, this whole thing, is available for you for free with almost every other PAAS service that you get. If you're getting the Java cloud Service or our Application Container Cloud or our Database Cloud Service or our container Docker Container Cloud Service, all of them come with an instance of Developer Cloud Service for free.
You can use it and try it out and see how it can help you manage your own project doing the same thing I just did here. Everything I showed you by the way is on our current production version, nothing future version, everything has been out a while, so you can just try it on your own.
We also have a bunch of tutorials and videos and blogs and forums for questions, if you go to this website and all the information is there.
And that's all the time I had for today. If you have any questions, because I need to let everyone go. Hey i'll be here just come back and ask your questions and I'll be happy to answer them. Thank you very much.


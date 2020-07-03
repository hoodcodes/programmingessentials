##### Pair and Mob Programming

Pair Programming

https://app.pluralsight.com/player?course=pair-programming&author=brendan-enrick&name=pair-programming-m1&clip=0&mode=live

Module 1:  Introduction to Pair Programming

BASICS OF PAIRING 

Pair Programming: 2 developers working as a pair on the same code using only one computer

2 roles:  driver and navigator
driver - dev at the keyboard
navigator - coming up with the plan, the direction and keeping the big picture in mind

PP is a discussion.  A collaboration.  It is not one person taking over, but rather both being involved in the conversation, providing rapid feedback

 Subject of Personal Space is a common one brought up on this topic.  Use common decency and sense and you should be fine.  Be considerate, patient and kind to one another is a good guideline.

BENEFITS

Knowledge Transfer- not just on the code itself, but devs share and enrich each other by way of sharing their experiences in code which might be from other projects.  

raising the number of the “Bus Factor” - number of people that would have to no longer be on the team before the business would feel its effects.  The higher the better.

From the Business’ perspective:  the scariest thing they consider is the lost productivity

Studies actually show that while productivity may slow a little bit, the number of bugs produced from the resultant code is ALWAYS LESS, and the code is MORE MAINTAINABLE.  The study was done by blind analysis, using judges who looked at code produced from both solo developers and paired programmers.  the paired programmers consistently scored better in both areas.  Success in projects is a marathon, not a sprint.  This translates into $$ savings.  Business cares about that.  And more stable products and services. 

 Improved Morale - 

teams who pair program don’t usually need team building exercises because they are already:
relying on one another
trusting one another
reaching out to one another
collaborating  
All of these activities improves morale of the team
Constant Review - 

Your code is constantly being reviewed when you PP, and at a much more appropriate time - BEFORE you might have normally invested a large amount of time and effort going down a path that might have been less than optimal.  

It is entirely possible too - that if that occured where it was found that something else would have been better to do, that it might be concluded that it is not worth going back and fixing (undoing) because the additional cost makes it prohibitive cost or time wise, from a business perspective.  Now - you have technical debt !!

Increased Readability - 

2 minds get to make the decision whether something is too complicated, or if namings are best.  


WHEN TO PAIR

Complex Code - when you are unsure how to approach something  100% of the time.  If you think it is complicated, someone else may as well.

making the complicated stuff ‘maintainable’ is of critical importance

Volatile Sections - 

Critical Systems - 

Core Libraries - here you need more than one opinion because these get used in a variety of places.  so you need to do it right, do it well.


WHEN NOT TO PAIR  

Trivial Tasks - something simple, been done before, might not be coding even.  

Spiking Code -  Be careful here, as if there is a hint of the code you write going into production, just get a pair.  

What is a Spike?  A ‘Spike’ is when we just go try something, such as try a little sample code - prototype a solution.   Spiked code is not intended to go into production.  You should throw it away, then pair up and write the thing for real if your prototype is good.  

When Sick - stay home.   (BUT - now with VS Live Share, this is still possible if you want to work or find yourself having to, but remember, your mind is going to be less than 100% if you are sick, usually.  This could be frustrating for your pair if your cognition is impaired)

TIMES YOU ALREADY PAIR 

Debugging together - there are times when several of you gather around a screen to debug an issue.  More heads are better than less in trying to solve an issue that is especially challenging.

Naming Discussions - It’s one of the more challenging things in code as they say.  Good names are valuable for readability and maintainability.  

Whiteboard Design Sessions - It is a design session, a discussion - about figuring out how to do / solve something

Reviewing Code - You are looking at code here, and have the ability to ask questions, make suggestions as you feel appropriate.  


OTHERS WHO PAIR 

Pilots - good thing!  A lot of data and tasks, so redundancy and several perspectives to manage the complex task of flying an airplane is especially valuable.  

Police - not as common.  good for safety.  having someone else thinking while one is working on discovery.  another head to think about the task and have another perspective.

Snipers - sometimes have a ‘spotter’  - someone who can provide another perspective on the subject.

Surgeons - Here is a mission critical task where you don’t want someone going off by themselves in a room and doing everything.  It is a team effort to keep you alive on that operating table.

the other person, a navigator is generally thinking about the ‘bigger picture’ while the responder is focused on execution of the detail.  


AND WHEN YOU PAIR UP 

Pay attention!  Stay attentive.  It would be rude to the other person if you are not fully engaged.  


Module 2:  Beginning Pairing Techniques

Ping Pong Pairing  

Involves writing tests.  Sequence is as follows:
Driver A writes a failing test.  
Switch Places
Driver B  makes the test pass
Driver B writes another failing test
Switch Places
Driver A makes the test pass
Repeat Steps 1-6  

Benefits of Ping Pong Pairing:
Enforces a TDD approach and discipline in that space
Collective Code Ownership 
Consistent switching 
Shared Decision Making  

Demo:  Notes  

When writing tests and code to get them working, you want to return the simplest thing that makes it works, and not over-engineer your method until a test really calls for it.  e.g. returning “1” in the very first FizzBuzz test.  

Discussions about naming, what to work on next are going to be rather common.  Then there are design discussions about the approach to use, and the benefit that only one person need know a particular detail implementation if they agree they want to pursue that line of logic - which makes pairing valuable and the code better in the long run.  

Pomodoro Switching  

Pomodoro Technique:  time mgmt technique designed around the idea of working in 25 minute intervals called ‘pomodoros’.

2 variations:
each person switches off every 25 minutes
start a pomodoro, but then use the ping pong pairing technique for the 25 minute period.  Then at the start of the next pomodoro, switch off with another partner 

Module 3:  Pairing Beyond The Basics 

When to Switch Roles



Research on Pair Programming



Experienced Pairing  



Rotating Team Members



Mob Programming   



Next Steps and Summary  



Module 4:  Organizational Considerations


Team Considerations   

Many developers object to the concept and some common developer objections are:
I’m not a social person
it will just slow me down 
i can’t think with someone else there
I just want to listen to music and do my thing  

While there are plenty of jobs out there for ‘loner’ developers, it can be argued that those who are willing to collaborate and interact more with team members are generally more effective than those who refuse to do so.

Collective Code Ownership - one of the key extreme programming benefits, and provides many benefits to the team.  

You can change your organization, or you can change organizations. - Martin Fowler  

Warning Signs that pair programming is not working effectively - 
one member becomes disengaged or distracted with some other activity
the pairing session turns into a ‘watch the master’ sesssion
silence - a signal of a breakdown in communication.  But - if partner asks for a minute or two to think, let them have it….

Pairing is best side by side, not some other way  

Furniture Considerations  

u shaped desk cubicle  - very hard to pair due to restrictions to be side by side comfortablly

L shaped desk layout - still hard to get 2 chairs together

Open desks and tables best   - 6ft tables are great.   

Standing desks are good.  

Avoid cubicles, and L shaped desks.  

Open areas and whiteboards, along with private spaces are great for pairing



Room Considerations   

Communication Barriers:
Different Time Zones
Different Rooms
Different Cubicles

cube farms not conducive

good layouts for collaboration:
open team room
caves and commons  

lots of whiteboards help
Workstation Considerations  

two sets of keyboards and mice are great

2 screens  - Extended Screen vs. Duplicate screen  

Extended screen allows:
space for coding and viewing
more familiar for the developers
easy to point at the screen

Duplicate screen allows:
Maintain better personal space
Each developer has a good view
May be able to use smaller fonts  

decide what works best for you both based on individual preferences  

Source Control and Work Tracking

simplest way is to take turns when performing checkouts or commits

you could note the users you were pairing with (github @mention)  

you could have user identities for each pair - but that could get large quickly for team greater than 5-6 developers

you could have a per-station login name if you have shared pairing workstations.  This has been seen as one of the more effective strategies.  You will have to mention in your checkin comment who was working at the machine at the time of the commit so it is clear who was doing the work

Remote Pairing   

VS Live Share !!! 

Next Steps   















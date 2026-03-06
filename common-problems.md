## Common Problems in Large Legacy Monoliths

Large legacy monolithic systems are extremely common in enterprise and public sector environments. Many of these systems started as small applications but gradually grew into complex platforms over many years.

As functionality increased, architectural evolution often did not keep pace with the growth of the system. This leads to a series of recurring technical problems.

This document summarizes some of the most common issues observed in large legacy monolithic systems.

### Low organizational scalability

With too many engineers working on the same code base, code merge conflicts become serious problems. Essentially, everyone is stepping on each other's toes and completing even the most trivial feature becomes slower and harder to deal with those issues.

<img width="650" height="350" alt="image" src="https://github.com/user-attachments/assets/098764c8-f553-4cac-8e12-34e035049051" />



We need a lot more planning and coordination which typically means more meetings and the more people we have in those meetings, the longer and less productive they become. 


<img width="700" height="400" alt="image" src="https://github.com/user-attachments/assets/9724e45e-b207-4ec0-92f9-09ecec94c763" />


But the number of engineers is not the only issue. As we add more features to our application, our code base becomes larger and more complex (hard, takes longer to load in the IDE, slower to build/test, risky to deploy) as a result, our release schedule becomes less frequent, which actually makes things even worse, because now every new release contains even more features, increasing the chances for bugs and outages. 

Finally onboarding new developers now takes more time as it is much harder for them to get familiar with this large code base. With every additional engineer in the team, we start seeing diminishing returns until we reach a point where adding more people to the team actually reduces everyone's productivity.

<img width="680" height="380" alt="image" src="https://github.com/user-attachments/assets/2bd3505e-7bb0-42b5-9204-4e34da11e23a" />


### Low system scalability

A large monolithic system can also have technical problems making the system less scalable. Each application instance, which contains our entire business logic, requires a lot of CPU and memory. So insted of using cheap commodity hardware, we need to run each instance on a more high end and expensive computer.


<img width="680" height="380" alt="image" src="https://github.com/user-attachments/assets/2225ed83-592f-463b-892d-e777a0c15cb1" />


We are also very constrained to the technology choices we potentially made many years ago, and we can't take advantage of new and better technologies. Refactoring our code base, even from one library to another, can be a huge effort, let alone considering a new programming language or a framework.

<img width="500" height="280" alt="image" src="https://github.com/user-attachments/assets/efce539d-478d-4aab-a3a7-73ddcb4ad686" />



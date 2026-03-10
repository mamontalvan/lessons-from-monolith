## Common Problems in Large Monoliths

Like many enterprise, the system did not start as a large and complex application. It began as a smaller system designed to solve specific operational needs. However, over the years, new requirements and new features were continuously added.

As the platform grew, the architecture did not evolve at the same pace as the system’s functionality. Instead of introducing clear architectural boundaries or restructuring parts of the system, new logic was often incorporated directly into the existing codebase.

Over time, this resulted in a monolithic system with increasing complexity and several recurring technical challenges.

Working on this platform exposed me to many of the common issues that appear in large monolithic systems. 

### 1) Low organizational scalability

With too many engineers working on the same code base, code merge conflicts become serious problems. Essentially, everyone is stepping on each other's toes and completing even the most trivial feature becomes slower and harder to deal with those issues.




<img width="650" height="350" alt="image" src="https://github.com/user-attachments/assets/098764c8-f553-4cac-8e12-34e035049051" />



<br>

We need a lot more planning and coordination which typically means more meetings and the more people we have in those meetings, the longer and less productive they become. 


<img width="650" height="350" alt="image" src="https://github.com/user-attachments/assets/1229af00-c5cc-4695-abd9-8a86ad09a2dd" />


But the number of engineers is not the only issue. As we add more features to our application, our code base becomes larger and more complex:
  - hard, 
  - takes longer to load in the IDE,
  - slower to build/test,
  - risky to deploy 

As a result, our release schedule becomes less frequent, which actually makes things even worse, because now every new release contains even more features, increasing the chances for bugs and outages. 

Finally onboarding new developers now takes more time as it is much harder for them to get familiar with this large code base. With every additional engineer in the team, we start seeing diminishing returns until we reach a point where adding more people to the team actually reduces everyone's productivity.


<img width="650" height="350" alt="image" src="https://github.com/user-attachments/assets/e8f29482-82a9-454d-a343-3baf0be40766" />



### 2) Low system scalability

A large monolithic system can also have technical problems making the system less scalable. Each application instance, which contains our entire business logic, requires a lot of CPU and memory. So insted of using cheap commodity hardware, we need to run each instance on a more high end and expensive computer.


<img width="650" height="350" alt="image" src="https://github.com/user-attachments/assets/61cb5c83-2866-4005-8b91-0d2e7da99a68" />


We are also very constrained to the technology choices we potentially made many years ago, and we can't take advantage of new and better technologies. Refactoring our code base, even from one library to another, can be a huge effort, let alone considering a new programming language or a framework.

When the company and the codebase grow, the monolithic architecture has both organizational and system scalability issues.






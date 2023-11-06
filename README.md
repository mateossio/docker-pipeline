## CI/CD Pipeline using Jenkins and Docker

### Workflow

The workflow of this React App starts when the devs commit code to the repo, then a Jenkins server pulls it, builds & tests it and after that creates and pushes a Docker image ready to be deployed. Finally another server hosted in Linode runs it and makes it accesible to the user (you)
<br/>
<br/>
I used a public repo (https://github.com/masudranashawon/todo-app) of a ToDo app made with react.

### Access the website:
http://139.144.56.207/

### How does it work?
![CI/CD Workflow](/public/pipeline-details.png)

### Some insights about CI/CD gained while working at this project:
Streamlined Development⚙️
<br>
CI/CD with Jenkins automates the build, test, and deployment processes, reducing manual intervention and accelerating the pace of development cycles.
Containerized Deployments🐳
<br> 
Docker allows to encapsulate applications within containers, ensuring consistency across different environments and enabling smoother, more reliable deployments.
Enhanced Collaboration👨‍💻👩‍💻
<br> 
This implementation isn't just about technology; it's a catalyst for improved collaboration and communication among our teams, fostering a more integrated DevOps culture.
Faster Time-to-Market⚡
<br>
CI/CD automates the build, test, and deployment processes, reducing manual errors and accelerating the delivery of software updates. This means new features and bug fixes can be rolled out more quickly.
Improved Quality and Reliability 🔐 : Automation in CI/CD pipelines ensures regular and consistent testing. This leads to higher-quality software with fewer bugs as issues are caught early in the development cycle, resulting in more reliable releases.

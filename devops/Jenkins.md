# Jenkins : documentation

## Documentation

### Lexicon

CI/CD : Continuous Integration/Deployment

### What is it ?

Jenkins is an open source automation server written in Java.

### Continuous integration with Jenkins

(Quoted from opensource.com)

First things first; let's define a few terms. CI/CD is a practice that allows teams to quickly and automatically test, package, and deploy their applications. It is often achieved by leveraging a server called Jenkins, which serves as the CI/CD orchestrator. Jenkins listens to specific inputs (often a Git hook following a code check-in) and, when triggered, kicks off a pipeline.

A pipeline consists of code written by development and/or operations teams that instructs Jenkins which actions to take during the CI/CD process. This pipeline is often something like "build my code, then test my code, and if those tests pass, deploy my application to the next highest environment (usually a development, test, or production environment)." Organizations often have more complex pipelines, incorporating tools such as artifact repositories and code analyzers, but this provides a high-level example.

## Links and sources

- Wikipedia page : https://en.wikipedia.org/wiki/Jenkins_(software)
- Tutorial on using Jenkins : https://www.tutorialspoint.com/jenkins/jenkins_overview.htm

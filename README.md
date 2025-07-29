# 1. Version control

## a. Git

- Commit: git commit -m "first commit"

- Push: local -> remote

- Pull: remote -> local

- Branch

## b. GitFlow

- 5 branchs:

   - Master: Contains stable code that has been released, only receives merges from release/* or hotfix/* branches.

   - Develop: Used for new feature development. All feature/* and hotfix/* branches are merged here once complete, when preparing for a release, a release/* branch is created from this.

   - Feature/*: Each feature/xxx branch is for developing a single new feature. Created from develop, and merged back into develop when done.

   - Release/*: Created from develop when preparing for a new release version. Used for final testing, minor bug fixes, updating version numbers and changelogs. After release, merged into both main and develop.

   - Hotfixes/*: Created directly from main to fix urgent issues in production. After fixing, merged back into both main and develop.

- Gitflow workflow
  
![](https://nvie.com/img/git-model@2x.png)

## c. Conventional commits 

A successful Git branching model: <type>(<scope>): <message>

- Popular types: feat, fix, docs, style, refactor, test, chore

- Scope: the part that describes the scope of the commit

- Git commit message lint: the process of checking and ensuring your commit message follows a Conventional commits. <Extension `Conventional Commits`>

# 2. System architecture

## a. Architecture patterns

2 main types:

- Monolithic architecture:

   - Layered architecture

   The layered architecture typically consists of four standard layers: presentation, business, persistence, and database.

   ![](https://statics.cdn.200lab.io/2024/01/layer.jpg?width=1200)

   - Pipline architecture

- Distributed architecture:

   - Event driven architecture

      - Broker topology: In the Broker topology, message streams are distributed evenly to event processors through the message broker without the need for a central event coordinator.

      ![](https://statics.cdn.200lab.io/2024/01/fosa_1402.png?width=1200)
    
      - Mediator topology: In the Meditator topology there is an intermediary component, often called a "mediator", which is used to coordinate and manage the flow of events between different services or components in the system.

      ![](https://statics.cdn.200lab.io/2024/01/fosa_1405.png?width=1200)

   - Microservices: Each service models a domain or workflow. This means that each service contains everything needed to function in the application, including classes, their subcomponents, and the database. The components of a basic microservice include:
 
      - Service: contains the business logic of the microservice, only the service can access the database
     
      - Database: a set of tables containing data serving the business logic of the microservice.
     
      -API gateway: provides a unified access point for microservices, helps manage, coordinate and secure communication between services in the microservices architecture, and provides a platform to deploy API management policies and optimize communication.

## b. Design partterns


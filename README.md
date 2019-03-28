# Spring Cloud Contracts

You always need confidence when pushing new features into a new application or service in a distributed system. To that end, this project provides support for Consumer-driven Contracts and service schemas in Spring applications, covering a range of options for writing tests, publishing them as assets, and asserting that a contract is kept by producers and consumers — for both HTTP and message-based interactions.

- [The problem to solve](the-problem-to-solve.md)

## The solution: Dependencies and a Methodology

The usage of this project combine a set of Dependencies in your project and a set of organizational operations between the Consumer and the Producers. In terms of technology, the solution provides a library for the Consumer in order to use the Contracts from any Producer. For the producer, the project provides a library to verify that the contracts match with the reality of your implementation. 

The execution of this project could be organized in 4 phases:

- Specification
- The contract definition
- Testing
- Contract Gobernance

### Specificacion

In the phase, the Consumer, use contracts from the different producers to improve the Integration tests

![](1.jpg)

#### Consumer

- Create an inventary about Dependencies and protocols used for Communications (Http, Messaging, etc...)
- Review with the different Producers if they maintain Contracts in their repositories
- Determine what is the best way to consume the Contracts from a project/consumer point of view (Git repository, Producer Artifactories)
- Collect Contracts (Expectations) from different Producers
- Stablish the initial API Review among Consumer and Producers

#### Producers

- Collect default Contracts (Expectations) from the system
- Create a location to maintanin the Contracts
- Create a version control of the Contracts
- Create an agreement on demand with Consumer about the Contracts
- Create a initial Pipeline to verify Contracts with the system

![](2.jpg)

![](3.jpg)

![](4.jpg)

## References

- https://www.martinfowler.com/articles/consumerDrivenContracts.html
- https://github.com/spring-cloud/spring-cloud-contract
- https://github.com/spring-cloud-samples/spring-cloud-contract-samples
- https://cloud.spring.io/spring-cloud-static/Greenwich.RELEASE/single/spring-cloud.html#_spring_cloud_contract
- https://spring.io/projects/spring-cloud#learn


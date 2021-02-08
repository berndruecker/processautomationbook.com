---
title: Customer Onboarding Example
weight: 10
---

# Customer Onboarding Example

![Customer Onboarding](/images/examples/onboarding.png)

Alongside Chapter 2, there is this example that shows the customer onboarding process of a fictional telecommunications company as executable process solution.

## Link To GitHub

[Customer Onboarding Process on GitHub](https://github.com/berndruecker/customer-onboarding-camundacloud-springboot)


## Stack

It used the following stack:

* Camunda Cloud
* Java
* Spring Boot

The process model contains three tasks:

* A service task that executes Java Code to score customers
* A user task so that humans can approve customer orders (or not)
* A service task that executes glue code to call the REST API of a CRM system


The process solution is a Maven project and contains:

* The onboarding process model as BPMN
* Source code to provide the REST API for clients (using Spring Boot)
* Java code to do the customer scoring
* Glue code to implement the REST call to the CRM system
* Fake for CRM system providing a REST API that can be called (to allow running this example self-contained)

## Current Limitations

At the time of writing the book, Camunda Cloud was missing some features, that should be used in this example:

* *Automated JUnit Tests*. The ability to write unit tests is limited. The sample code contains a [POC for how tests could look like](https://github.com/berndruecker/customer-onboarding-camundacloud-springboot/blob/master/src/test/java/io/berndruecker/onboarding/customer/CustomerOnboardingTests.java), but the real feature has still to land in Camunda Cloud later in 2021.

* *BPMN User Task, a tasklist application and task forms*. As a workaround, the current source code simulates the user to approve customer orders by a service task. The configures task worker simply completes the user task. A feature set resolving this is expected in April 2021.

* *Out-of-the-box DMN Integration*. As a workaround, this project contains own glue code, that executed decision using the Camunda DMN engine. A feature set resolving this is expected end of 2021.

I will update the example as soon as features are released and available.


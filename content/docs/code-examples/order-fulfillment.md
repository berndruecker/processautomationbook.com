---
title: Order Fulfillment Example
weight: 20
---


# Order Fulfillment Microservices Example

![Order Fulfillment ](/images/examples/order-fullfilment-microservices.png)

In **Chapter 7 and 8**, there is this example that shows various microservices interacting to fulfill a customer's order. You can understand that there does not need to be any central orchestration and every microservice might include some process logic. Furthermore, you can also compare the solution approach to a pure event-based choreography.

## Link To GitHub

[Order Fulfillment on GitHub](https://github.com/berndruecker/flowing-retail/tree/master/kafka)


## Stack

It used the following stack:

* Camunda Platform / Camunda Cloud (both is available in sub folders)
* Java & Spring Boot
* Apache Kafka


## Alternative Approach to Microservices Orchestration

As described in **Chapter 6 ("Using The Workflow Engine As Communication Channel")** you can also use the workflow engine itself as communication channel between microservices, even if that might not always be a good idea (as discussed in the book in more detail). In this variant, there is no Apache Kafka.

![A workflow engine as communication channel](/images/examples/workflow_logic_pub_sub_microservices.png)

This [Order Fulfillment Example on GitHub](https://github.com/berndruecker/flowing-retail/tree/master/zeebe) shows an executable example using Camunda Cloud.
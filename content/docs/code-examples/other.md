---
title: Other Examples
weight: 30
---

# Other Examples Mentioned in the Book

Beside the two bigger use cases of [Customer Onboarding](onboarding/) and [Order Fulfillment](order-fulfillment/) there are a couple of smaller examples promised in the book. You can find respective links to runnable source example on this page.




## Combining Process Models and Programming Code

As mentioned in **Chapter 3 ("Combining Process Models and Programming Code")**, there are three conceptual ways to link BPMN process models with glue code.

### Publish/Subscribe

![Connector](/images/examples/workflow_logic_pub_sub.png)

See:

* [Camunda Cloud Job Worker Get Started Guide](https://docs.camunda.io/docs/guides/setting-up-development-project#create-a-job-worker)

### Reference Code 

![Connector](/images/examples/service_task.png)

See:

* [Camunda Platform Java Delegate Docs](https://docs.camunda.org/manual/7.14/user-guide/process-engine/delegation-code/#java-delegate)
* [Simple Service Task Example](https://github.com/camunda/camunda-bpm-examples/blob/master/spring-boot-starter/example-simple/src/main/java/org/camunda/bpm/spring/boot/example/simple/SayHelloDelegate.java)

### Connector Example

![Connector](/images/examples/workflow_logic_connector.png)

See:

* [REST Call via Camunda Platform Connector Example](https://github.com/camunda/camunda-bpm-examples/blob/master/servicetask/rest-service/src/main/resources/invokeRestService.bpmn)
* [Camunda RPA Bridge Docs](https://docs.camunda.org/manual/7.14/user-guide/camunda-bpm-rpa-bridge/)
* [Camunda Cloud - AWS Lambda Worker Code](https://github.com/zeebe-io/zeebe-lambda-worker)





## BPMN For Status Inquiries

Mentioned in **Chapter 11 ("Status Inquiries")** you can also build a simple HTML page showing certain metrics on top of a BPMN model visualized by [BPMN.io](https://bpmn.io/).

![BPMN.io used to visualize status in an HTML page](/images/examples/bpmn-io.jpg)

An example can be found in [this part of the order fulfillment example](https://github.com/berndruecker/flowing-retail/blob/master/kafka/java/monitor/src/main/resources/static/bpmn.html). But it might be easier to look at this example to understand parts of it: [Simple Process Instance Status View using bpmn.io](https://github.com/camunda-consulting/code/tree/master/snippets/bpmn-io-sample).




## Synchronous Facade

* Having a synchronous facade in front of long running logic is mentioned in **Chapter 9 ("Synchronous Request/Response")** 
* You can implement such a facade yourself, in the code invoking the workflow engine, as this example using Java, Semaphores and Camunda Platform 7.x shows: [https://github.com/berndruecker/flowing-retail/blob/master/rest/java/payment-camunda/src/main/java/io/flowing/retail/payment/resthacks/PaymentRestHacksControllerV4.java#L86](https://github.com/berndruecker/flowing-retail/blob/master/rest/java/payment-camunda/src/main/java/io/flowing/retail/payment/resthacks/PaymentRestHacksControllerV4.java#L86)
* You can use built-in features of the workflow engine, such as "awaitable outcomes" in Camunda Cloud, as shown here: [https://docs.camunda.io/docs/product-manuals/clients/java-client-examples/workflow-instance-create-with-result](https://docs.camunda.io/docs/product-manuals/clients/java-client-examples/workflow-instance-create-with-result)


## Stateful Retry

* Mentioned in **Chapter 9 ("Synchronous Request/Response")** 
* Implementation with Java and Camunda Platform 7.x: [https://github.com/berndruecker/flowing-retail/tree/master/rest/java/payment-camunda](https://github.com/berndruecker/flowing-retail/tree/master/rest/java/payment-camunda)



## Saga Pattern and BPMN Compensation

* Mentioned in **Chapter 9 ("Saga Pattern and Compensation")** 
* There are various variations for the trip booking example:
  * [Java + Camunda Platform 7.x](https://github.com/berndruecker/trip-booking-saga-java) 
  * [C# + Camunda Platform 7.x](https://github.com/berndruecker/flowing-trip-booking-saga-c-sharp)
  * [Serverless Functions](https://github.com/berndruecker/trip-booking-saga-serverless)





## Message Buffering Workarounds

Some engines do not buffer messages if a process instance is not yet ready-to-receive, as discussed in **Chapter 9 ("Aggregating Messages")**. 

If you don't have message buffering at your disposal, you either

* buffer and retry messages in front of the workflow engine (e.g. using message brokers)
* accommodate this limitation in your model


As illustration:

* Camunda Platform 7.x does *not* support message buffering, so the following solution applies and the example linked below is done using Camunda Platform.
* Camunda Cloud *does* support message buffering, so you best rely on the built-in features for that.

The following model will always be ready-to-receive the next message, in parallel to processing any incoming message. This model is executable and will safely collect all messages, even if they arrive at the same time and your engine does not support message buffering. 

![Aggregator process model that buffers messages itself](/images/examples/aggregator-ready-to-receive.png)

This model uses a couple of BPMN elements which are new to you if you followed the book.

It leverages a non-interrupting subprocess whenever the next message arrives. This means that the main process is kept, but a parallel path of execution is spawned. And it uses an event-based gateway, as the main process waits for either the condition that all messages arrive is true, or a timeout happens. The condition event operates on data, so you might have a flag in the process variables to indicate if all variables have arrived.



You can find an example using Camunda Platform here: [https://TODO](https://TODO).



## Serverless Function Orchestration

* Mentioned in **Chapter 4 ("Serverless Functions")**
* You can find various example of serverless function orchestration in the [Trip Booking Saga Serverless](https://github.com/berndruecker/trip-booking-saga-serverless/) showcase, especially this one (using Camunda Cloud and AWS Lambda Functions) is interesting to look at: https://github.com/berndruecker/trip-booking-saga-serverless/tree/master/zeebe/aws




## Workflow Engine And Actors

* Mentioned in **Chapter 5 ("Actor Model")**
* See [POC using Axon + Camunda Platform: https://github.com/plexiti/axon-camunda-poc/](https://github.com/plexiti/axon-camunda-poc/)



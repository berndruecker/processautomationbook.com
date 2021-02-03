---
weight: 5
title: What To Expect From This Book
bookToc: false
---

# Summary 

In today's IT architectures, microservices and serverless functions play an increasingly important role. But how can you create meaningful, comprehensive, and connected business solutions if the individual components are decoupled and independent by design? This book provides a framework through examples and practical advice, and reveals how you can design complex processes in such an environment to deliver true business value.

Therefore, this book dives into a developer-friendly view on process automation and explains how process automation can be applied in modern system architectures and software development practices. 

It focuses on lightweight workflow engines as the core component to make this happen, which should be part of every developers tool belt. 

The book also discusses typical misconceptions around process automation and orchestration.


# Why You Should Read This Book

1. Digital transformation is happening everywhere and automation a must.
2. Many processes are tailor-made to an organization's needs, as this allows to differentiate from competition. Therefore they cannot be addresses by off-the-shelf application software.
3. Automating these processes is complex and requires software engineering, but with specific characteristics and requirements.
4. You will need a developer-friendly way to automate processes, leveraging lightweight workflow engine technology. This is exactly what this book explains to you.

# Who This Book is For

This book targets software developers, software engineers and software or system architects that want to learn about process automation.

If you are a software developer, you might want to use a workflow engine within your application, service or microservice to solve hands-on problems. This book will help you understand which problems a workflow engines solves for you, and how you get started. 

If you are a system architect, this book will help you understand opportunities and pitfalls around process automation. It will guide you through some tough architectural decisions and trade-offs, including how using a workflow engine compares to alternative approaches or if a workflow engine should be operated centrally or not.

But you can also benefit, if you work in another role:

* If you are an IT manager, the book can also help you to make better informed decisions and ask the right questions internally. 

* If you are a business analyst, this book can help you if you are motivated to think a bit out-of-the-box and understand the technical side of things.

You will only need some general experience in the field of software engineering, but no other specific knowledge. 

# Table Of Contents



    Preface
        Many Ways to Automate Processes
        The Scope Of This Book
        Who This Book is For
        The Architect Always Implements
        Accompanying Website and Code Examples
    
    1. Introduction
        Process Automation
        Wild West Integrations
        Workflow Engines And Executable Process Models
        A Business Scenario
        Long-Running Processes
        Business Processes, Integration Processes and Workflows
        Business-IT Collaboration
        Business Drivers and the Value of Process Automation
        Not Your Parents’ Process Automation Tools
        Conclusion

    Part I: Fundamentals

    2. Workflow Engines and Process Solutions
        The Workflow Engine
            Core Capabilities
            Additional Features of Workflow Platforms
            Architecture
        A Process Solution
        Executable Example
        Applications, Processes, Workflow Engines
        Typical Workflow Tools in a Project’s Life Cycle
            Graphical Process Modeler
            Collaboration Tools
            Operations Tooling
            Tasklist Applications
            Business Monitoring and Reporting
        Conclusion

    3. Developing Process Solutions
        Business Process Model and Notation (BPMN)
            Start and End Events
            The Token Concept: Implementing Control Flow
            Sequence Flows: Controlling the Flow of Execution
            Tasks: Units of Work
            Gateways: Steering Flow
            Events: Waiting for Something to Happen
            Message Events: Waiting for a Trigger from the Outside
        Combining Process Models and Programming Code
            Publish-Subscribe to a Process
            Referencing Code in Process Models
            Using Pre-Built Connectors
            Model or Code?
        Testing Processes
        Versioning of Process Solutions
        Conclusion

    4. Orchestrate Anything
        Orchestrate Software
            Service Oriented Architecture (SOA) Services
            Microservices
            Serverless Functions
            Modular Monoliths
            Deconstructing the Monolith
        Orchestrate Decisions
            Decision Model And Notation (DMN)
            Decisions in a Process Model
        Orchestrate Humans
            Task Assignment
            Additional Tool Support
            The User Interface of User Tasks
        Orchestrate RPA (Robotic Process Automation) Bots
        Orchestrate Physical Devices and Things
        Conclusion

    5. Championing Workflow Engines And BPMN
        Limitations of Other Implementation Options
            Hard-coded Processes
            Batch Processing
            Data Pipelines and Streaming
            Actor Model
            Stateful Functions
        Process Modeling Languages
            Workflow Patterns
            Benefits Of Graphical Process Visualizations
            Textual Process Modeling Approaches
            Typical Concerns About Graphical Modeling
            Graphical vs. Textual Approaches
        Process Automation With Blockchain?
        Conclusion

    Part II: Process Automation in the Enterprise

    6. Solution Architecture
        When to Use a Workflow Engine
        Architecture Tradeoffs
            Running The Workflow Engine
            Decentralized Engines
            Sharing Engines
            Ownership of Process Models
            Using The Workflow Engine As Communication Channel
            In-House Workflow Platforms
            Performance And Scalability
            Developer Experience and Continuous Delivery
        Evaluating Your Workflow Engine
        Conclusion

    7. Autonomy, Boundaries and Isolation
        Strong Cohesion And Low Coupling
        Domain Driven Design, Bounded Contexts and Services
        Boundaries And Business Processes
            Respect Boundaries and Avoid Process Monoliths
            Foster Your Understanding Of Responsibilities
            Long-Running Behavior Helps You to Defend Boundaries
        How Processes Communicate Across Boundaries
            Call Activities - Handy Shortcuts Only Within The Boundary
            Crossing Boundaries Is An API Call
        Decentralized Workflow Tooling
        Conclusion

    8. Balancing Orchestration and Choreography
        Event-driven Systems
            Emergent Behavior
            Event Chains
            The Risk Of Distributed Monoliths
        Contrasting Orchestration and Choreography
            Introducing Commands
            Messages, Events and Commands
            Terminology and Definitions
            Avoiding Event Chains By Using Commands
            The Direction Of Dependency
        Finding The Right Balance
            Deciding About Using Commands or Events
            Mix Commands And Events
            Designing Responsibilities
            Evaluate Change Scenarios To Validate Decisions
        Debunking Common Myths
            Commands Do Not Require Synchronous Communication
            Orchestration Does Not Need To Be Central
            Choreography Does Not Automatically Lead To More Decoupling
        The Role of Workflow Engines
        Conclusion

    9. Workflow Engines And Integration Challenges
        Communication Patterns For Service Invocation
            Synchronous Request-response
            Asynchronous Request-response
            BPMN and Being Ready-to-receive
            Aggregating Messages
            Poisoned and dead messages
            Synchronous Facades Hiding Asynchronous Communication
        Transactions and Consistency
            Eventual Consistency
            Business Strategies to Handle Inconsistency
            Saga Pattern and Compensation
            Chaining Resources by Using the Outbox Pattern
        Eventual Consistency Applies to Every Form of Remote Communication
        The Importance of Idempotency
        Conclusion

    10. Business-IT Collaboration
        A Typical Project
        Including All The People: BizDevOps
        The Process Automation Lifecycle
        The Power of One Joined Model
        Who Does the Modeling?
        Creating Better Process Models
            Extract (Integration) Logic Into Subprocesses
            Distinguishing Between Results, Exceptions, and Errors
            Increasing Readability
        Conclusion

    11. Process Visibility
        The Value Of Process Visibility
        Getting the Data
            Leverage Audit Data From Your Workflow Engine
            Model Events To Measure Key Performance Indicators (KPIs)
        Status Inquiries
        Understanding Processes That Span Multiple Systems
            Observability And Distributed Tracing Tools
            Custom Centralized Monitoring
            Data Warehouses, Data Lakes And Business Intelligence Tools
            Process Mining
            Process Event Monitoring
            Current Market Dynamics
        Setting Up Process Reporting And Monitoring
            Typical Metrics And Reports
            Allow For a Deeper Understanding
        Conclusion

    Part III: Get Going!

    12. The Journey to Introduce Process Automation
        Understanding The Adoption Journey
            Failures You Want to Avoid
            A Success Story
            The Pattern of Successful Adoption Journeys
            Different Journeys For Different Scenarios
        Starting Your Journey
            Bottom-up vs Top-Down Adoption Motion
            Proof Of Concepts
            Presenting The Business Case
            Don’t Build Your Own Platform
            Do’s and Don’ts Around Reuse
        From Project to Program: Scaling Adoption
            Perception Management: What Is Process Automation?
            Establishing a Center of Excellence
            Managing Architecture Decisions
            Decentralized Workflow Tooling
            Roles And Skill Development
        Conclusion

    13. Parting Words
        Current Architecture Trends Influence Process Automation
        Rethink Business Processes and User Experience
        Where To Go From Here



# Praise

> Weaving together ideas from microservices, event-driven systems, and Domain-Driven Design, this book describes when, why, and how to effectively leverage workflows within a modern software architecture. Taking a pragmatic practitioner's approach, it uses real-world examples and explores the pros and cons of multiple alternative patterns in detail. It should be on every architect's bookshelf.

***Randy Shoup**, VP Engineering and Chief Architect at eBay*

> Bernd has championed and delivered developer-friendly process automation tools for the best part of the last decade. Now, in this pragmatic new book, Bernd brings that wealth of experience to show how process automation models, methods, and tools can be applied to tame the complexity of microservices and cloud-native architectures which are becoming ever more prevalent in today’s technology landscape. I highly recommend this book for architects and developers who want to add process automation thinking to their design toolkit.
 
***Richard Tarling**, Digitization & Workflow Engineering Co-lead at Goldman Sachs*

> Process automation has often been viewed as the antithesis of modern, agile software development: snazzy "doodleware" demos that don't scale to real use cases, poor testability, and version control only for the fortunate ones. No one better than Bernd to show us that this perception has little to do with workflow and process automation but merely with past implementations. Seeing process automation as an extension of well-established software development methods and architectures breathes a much welcome breeze of fresh air into the field.

***Gregor Hohpe**, author of Enterprise Integration Patterns and The Software Architect Elevator*




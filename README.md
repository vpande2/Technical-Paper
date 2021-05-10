# What are Messaging Queues? Why they are used? What are popular tools? What is Enterprise Message Bus?

A message queue is a component of messaging middleware solutions that enables independent applications and services to exchange information. Message queues store “messages”—packets of data that applications create for other applications to consume—in the order they are transmitted until the consuming application can process them. This enables messages to wait safely until the receiving application is ready, so if there is a problem with the network or receiving application, the messages in the message queue are not lost.

This model, known as asynchronous messaging (15:11), prevents data loss and enables systems to continue to function if processes or connections fail. This allows developers to keep processes and applications separate, keeping their communications self-contained and event-driven to make the architecture more reliable.

Message queues are available in messaging solutions across numerous deployment options, including optimized physical appliances, cloud services, mainframes, and as software.

https://www.ibm.com/cloud/learn/message-queues

 

## This information highlights some features and benefits of message queuing. It describes features such as security and data integrity of message queuing.

The main features of applications that use message queuing techniques are:
* There are no direct connections between programs.
* Communication between programs can be independent of time.
* Work can be carried out by small, self-contained programs.
* Communication can be driven by events.
* Applications can assign a priority to a message.
* Security.
* Data integrity.
* Recovery support.
### No direct connections between programs
Message queuing is a technique for indirect program-to-program communication. It can be used within any application where programs communicate with each other. Communication occurs by one program putting messages on a queue (owned by a queue manager) and another program getting the messages from the queue.
Programs can get messages that were put on a queue by other programs. The other programs can be connected to the same queue manager as the receiving program, or to another queue manager. This other queue manager might be on another system, a different computer system, or even within a different business or enterprise.

There are no physical connections between programs that communicate using message queues. A program sends messages to a queue owned by a queue manager, and another program retrieves messages from the queue. 

As with electronic mail, the individual messages that are part of a transaction travel through a network on a store-and-forward basis. If a link between nodes fails, the message is kept until the link is restored, or the operator or program redirects the message.

The mechanism by which a message moves from queue to queue is hidden from the programs. Therefore the programs are simpler.

### Time-independent communication

Programs requesting others to do work do not have to wait for the reply to a request. They can do other work, and process the reply either when it arrives or at a later time. When writing a messaging application, you need not know (or be concerned) when a program sends a message, or when the target is able to receive the message. The message is not lost; it is retained by the queue manager until the target is ready to process it. The message stays on the queue until it is removed by a program. This means that the sending and receiving application programs are decoupled; the sender can continue processing without waiting for the receiver to acknowledge receipt of the message. The target application does not even have to be running when the message is sent. It can retrieve the message after it is has been started.

### Small programs
Message queuing allows you to use the advantages of using small, self-contained programs. Instead of a single, large program performing all the parts of a job sequentially, you can spread the job over several smaller, independent programs. The requesting program sends messages to each of the separate programs, asking them to perform their function; when each program is complete, the results are sent back as one or more messages.
### Message-driven processing
When messages arrive on a queue, they can automatically start an application using triggering. If necessary, the applications can be stopped when the message (or messages) have been processed.

### Event-driven processing
Programs can be controlled according to the state of queues. For example, you can arrange for a program to start as soon as a message arrives on a queue, or you can specify that the program does not start until there are, for example, 10 messages above a certain priority on the queue, or 10 messages of any priority on the queue.
### Message priority
A program can assign a priority to a message when it puts the message on a queue. This determines the position in the queue at which the new message is added.
Programs can get messages from a queue either in the order in which the messages are in the queue, or by getting a specific message. (A program might want to get a specific message if it is looking for the reply to a request that it sent earlier.)

### Security
Security facilities are provided, including authentication of applications when they use a queue manager, authorization checks when they use resources such as a queue on the queue manager, and encryption of message data as it travels over the network, and as it resides on queues. For more information about security.
### Data integrity
Data integrity is provided by units of work. The synchronization of the start and end of units of work is fully supported as an option on each MQGET or MQPUT, allowing the results of the unit of work to be committed or rolled back. Sync point support operates either internally or externally to IBM® MQ depending on the form of sync point coordination selected for the application.
### Recovery support
For recovery to be possible, all persistent IBM MQ updates are logged. If recovery is necessary, all persistent messages are restored, all in-flight transactions are rolled back, and any sync point commit and backouts are handled in the normal way of the sync point manager in control. For more information about persistent messages.

https://www.ibm.com/docs/en/ibm-mq/9.2?topic=queuing-main-features-benefits-message

## There are some popular tools for  Messaging Queues

1. MuleSoft Anypoint Platform.
2. IBM MQ.
3. Azure Scheduler.
4. Apache Kafka.
5. Google Cloud Pub/Sub.
6. Apache ActiveMQ.
7. RabbitMQ.
8. ZeroMQ.

https://www.g2.com/categories/message-queue-mq

## Enterprise Message Bus

An ESB, or enterprise service bus, is an architectural pattern whereby a centralized software component performs integrations between applications.  It performs transformations of data models, handles connectivity, performs message routing, converts communication protocols and potentially manages the composition of multiple requests. The ESB can make these integrations and transformations available as a service interface for reuse by new applications. 

The ESB pattern is typically implemented using a specially designed integration runtime and toolset (i.e., esb product) that ensures the best possible productivity.


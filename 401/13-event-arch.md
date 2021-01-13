# Event Driven Architecture

## Links

- [AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)
- [Azure Event Hubs](https://www.youtube.com/watch?v=DDDjFQSQyF4)
- [FIFO Queues within AWS and Azure](https://vunvulear.medium.com/fifo-and-queues-inside-aws-and-azure-d21145473d5a)

---

1. **What’s the difference between a FIFO and a standard queue?**

    FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers. [Source](https://aws.amazon.com/about-aws/whats-new/2016/11/amazon-sqs-introduces-fifo-queues-with-exactly-once-processing-and-lower-prices-for-standard-queues/#:~:text=FIFO%20queues%20have%20essentially%20the,being%20received%20by%20message%20consumers.)

2. **How can the server be assured a message was properly received?**

    Store them

3. **What classic design pattern is best represented by event driven programming?**

    object oriented design

4. **How do you test an event driven system?**

    tests for the functions or by emitting events

## Vocabulary

- **FIFO Queue** - First In First Out Queue

- **Pub/Sub** - async messaging that separates event creation from event processing
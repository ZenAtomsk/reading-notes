# AWS: Cloud Servers

## Links

- [Virtual Machines](https://www.youtube.com/watch?v=yIVXjl4SwVo)
- [VMS and the Cloud ](https://www.youtube.com/watch?v=l0DfHUWMjsU)
- [AWS EC2](https://aws.amazon.com/ec2/?ec2-whats-new.sort-by=item.additionalFields.postDateTime&ec2-whats-new.sort-order=desc)
- [EC2 For Humans](https://www.youtube.com/watch?v=lZMkgOMYYIg)
- [Elastic Beanstalk](https://www.youtube.com/watch?v=SrwxAScdyT0)

## Research

1. **What’s the difference between a FIFO and a standard queue?**

    FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers. [Source](https://aws.amazon.com/about-aws/whats-new/2016/11/amazon-sqs-introduces-fifo-queues-with-exactly-once-processing-and-lower-prices-for-standard-queues/#:~:text=FIFO%20queues%20have%20essentially%20the,being%20received%20by%20message%20consumers.)

2. **How can the server be assured a message was properly received?**

    Store them

3. **What classic design pattern is best represented by event driven programming?**

    object oriented design

4. **How do you test an event driven system?**

    tests for the functions or by emitting events

## Vocabulary

- **Server** - a piece of computer hardware or software (computer program) that provides functionality for other programs or devices, called "clients".

- **Pub/Sub** - async messaging that separates event creation from event processing

- **WRRC** - Web Request Response Cycle
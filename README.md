# MessageQueues - AWS SQS
creating a few Message Queues and Broadcasters and wiring them through code.

## Get Started
### Create Queue in AWS SQS
1. Click on Create New Queue button.
2. Enter a queue name and select standard queue.
3. Click create queue bottom on the low right side of page.

Notes: 
1. Under permissions tab, click add permissions, select Everybody(*). Then a pop up box appears, check Receive Message and 
Delete Message.
2. Make sure the user has AmazonSQSFullAccess permissions. 

### Create a java application
1. gradle init
2. add dependencies in build.gradle file
```
dependencies {
    implementation platform('com.amazonaws:aws-java-sdk-bom:1.11.228')
    implementation 'com.amazonaws:aws-java-sdk-sqs'
    testCompile group: 'junit', name: 'junit', version: '4.11'
}
```

## Run application
./gradlew run


## Resources
https://github.com/awsdocs/aws-doc-sdk-examples/blob/master/java/example_code/sqs/src/main/java/aws/example/sqs/SendReceiveMessages.java
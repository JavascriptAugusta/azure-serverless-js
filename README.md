# azure-serverless-js
Code for Azure functions and description of serverless computing

<b>What is serverless architecture?</b>

A model where a third-party service manages the allocation of computing resources. 

<b>Is it really serverless?</b>

No. It’s called serverless because the tasks of server management and capacity planning are hidden from the developer or operator.

<b>What is the difference between PaaS (Platform as a Service) and FaaS (Function as a Service)?</b>

PaaS providers like Heroku, Azure Web Apps and AWS Elastic Beanstalk eliminate the need for managing servers. However, your application is typically deployed in a traditional way using a type of web framework.

With FaaS, your application is composed of individual, independent functions.

<b>What are the benefits of serverless computing?</b>

Cost – resources are consumed as needed instead of provisioning the servers and having large amounts of idle time

Developer time – developers don’t need to spend time setting up servers and tuning up autoscale policies or resources

Simpler backend programming – using simple functions eliminates the need to worry about multithreading and handling HTTP requests in an application

<b>What are the disadvantages of serverless computing?</b>

Performance – Greater latency can be experienced because services typically spin down serverless code when it’s not in use. After idle time, the runtime takes time to start up to run the code.

Monitoring and debugging – It’s more difficult to diagnose performance problems because tools like profilers and debuggers aren’t available. Since the environment where the code is run is not open source it’s hard to replicate its performance characteristics.

Security – Serverless can be more secure in that OS vulnerabilities are managed by the cloud provider. However, with more functions there can be more entry points to an application. Also, network-level security cannot be implemented by an individual.

<b>What type of applications work well on serverless architecture? Are there any applications that shouldn’t be implemented as serverless?</b>

Use it especially if you have a small number of functions that need to be hosted.

For a more complex application, pieces of it can be implemented as serverless and part of it as a more traditional, unified application.

High-performance computing or a large computing workload are less likely to be a good fit for serverless. It may be cheaper to provision the servers yourself. There are also resource limits for cloud providers.

Sources:
https://medium.com/@MarutiTech/what-is-serverless-architecture-what-are-its-criticisms-and-drawbacks-928659f9899a

https://en.wikipedia.org/wiki/Serverless_computing

https://www.twilio.com/docs/glossary/what-is-serverless-architecture

<b>Specific information on Azure Functions</b>

Write functions using your choice of C#, F#, or JavaScript

Pay-per-use pricing model. More on pricing at https://azure.microsoft.com/en-us/pricing/details/functions/

Functions supports NPM

Development can be done in the portal or through GitHub or Visual Studio Team Services

The Functions runtime is open-source and available on GitHub

Triggers are ways to start execution of your code

Bindings are ways to simplify coding for input and output data

Here are some of the templates available based on how functions are triggered:
<ul>
<li>HTTPTrigger
<li>TimerTrigger
<li>GitHub webhook
<li>Generic webhook
<li>CosmosDBTrigger
<li>BlobTrigger
</ul>

The following service integrations are supported by Azure Functions:
<ul>
<li>Azure Cosmos DB
<li>Azure Event Hubs
<li>Azure Event Grid
<li>Azure Mobile Apps (tables)
<li>Azure Notification Hubs
<li>Azure Service Bus (queues and topics)
<li>Azure Storage (blob, queues, and tables)
<li>GitHub (webhooks)
<li>On-premises (using Service Bus)
<li>Twilio (SMS messages)
</ul>

Source: https://docs.microsoft.com/en-us/azure/azure-functions/functions-overview

Other useful links:

https://docs.microsoft.com/en-us/azure/azure-functions/functions-reference

https://docs.microsoft.com/en-us/azure/azure-functions/functions-reference-node

https://docs.microsoft.com/en-us/azure/azure-functions/functions-bindings-storage-table

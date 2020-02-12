## Solution Design

A Technical Solutions Consultant from the Apigee Customer Success team works
with Developer Dane to create a High Level Solution Design and initial scope.


```
+-------------+    +-----------+    +-------------+
| Kitchen App |    | Order App |    | Drivers App |
+-------------+    +-----------+    +-------------+
         |               |                |
+--------------------------------------------------+
|                  API Platform                    |
+--------------------------------------------------+
         |                                |
+------------------+               +---------------+
| Identity Service |               | Order Service |
+------------------+               +---------------+

```

At this stage, the team do not worry about specific details of this design, but
instead look for something they can rapidly prototype and test with real 
customers. 

They also discuss that the APIs built here can be reused for third-parties.

However, they do identify the need to integration with the following components
in order to follow best practices:

- Developer Portal for third-party onboarding and documentation
- Message Logging to help with customer support
- Monitoring to identify issues in production
- Source Control system for storing coding
- Continuous Integration system to manage the test and deploy pipeline
- An Open ID Connect Compliant Identity Provider


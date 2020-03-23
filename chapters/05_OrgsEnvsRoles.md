## Orgs, Environments and Roles

### Organizations and Environments

The team would like to structure their environments such that they ensure
increasing quality as code progresses to the production environment. However
a heavy governance structure may stifle innovation and speed to value. Here
is the structure that they agree on.

| Environment	| Organization	| Backend	| Testing Type	|
|---------------|---------------|---------------|---------------|
| dev		| pizza-nonprod | mock		| @all		|
| intg		| pizza-nonprod | intg		| @all not @mock|
| perf		| pizza-nonprod | mock/perf	| @benchmark	|
| uat		| pizza-nonprod | uat		| @all		|
| preprod	| pizza-prod 	| prod		| @smoke	|
| sandbox	| pizza-prod 	| mock		| @all not @mock|
| prod		| pizza-prod 	| prod		| @smoke	|

### Traffic Isolation

The team would like to use the SaaS version of Apigee Edge to reduce their total
cost of ownership, however they are aware that means using some shared infrastructure.

They would like to ensure that their performance tests are physically isolated so
that any downtime caused won't affect other environments. In addition they would ike
to isolate ther production environment from non-prod environmments.

They learn that it is possible to isolate an organisation or environment by applying a 
Traffic Isolation Pack. The team requests two TIPs for prod and perf.

### Multi-Region Support

TODO Adding an addition region
TODO Leaving the Google backbone

### Role Based Access Control

In addition to physical separation of runtimes, we must separate users.

- We don't want an intern accessing production
- We only want CI/CD processes to deploy to all envs
- We only want the ops team to trace in production
- We want business users to only see Analytics

TODO how to do it

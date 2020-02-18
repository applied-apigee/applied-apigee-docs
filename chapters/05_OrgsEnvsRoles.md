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

Apigee Edge in the cloud is multitenant and uses shared infrastructure. 

It is possible to isolate an organisation or environment by applying a 
Traffic Isolation Pack.

The team choose to isolate the perf and prod environments to ensure that
downtime does affect the runtime of other environments.

### Role Based Access Control

In addition to physical separation of runtimes, we must separate users.

- We don't want an intern accessing production
- We only want CI/CD processes to deploy to all envs
- We only want the ops team to trace in production
- We want business users to only see Analytics



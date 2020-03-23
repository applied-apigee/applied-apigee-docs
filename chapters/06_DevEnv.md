## Development Environment Setup

The team are happy to learn about Apigee using the UI, but they want to be able
to use the tools that they are used to. These include source control, their 
favourite IDE and a continuous integration system. They set up the following:

### Editor

After learning evaluating VS Code, vim, Eclipse and Notepad++, they decide
to use VS Code. One of the team refuses and continues to use vim, but that is
ok!

### Build tools

They learn that interaction with Apigee is all done through the Management API. Whilst
they could use curl or Postman directly, they would like something a bit higher
level to speed up the development process.

After evaluating apigeetool and Maven, they choose Maven as it has the largest community
and the team are already familiar with it.

### Testing tools

Whilst most Apigee policies are XML configuration, some callouts contain custom
Java, Javascript or Python. The team decide that they will write unit tests in the
same language as the custom code that they are writing.

They decided that the following:

- First, they will try to configure out of the box policies
- If they have a requirement that requires programming, they will use Javascript
- If they have a complex requirement that requires high performance, they will use Java
as this just perform the best on the Apigee SaaS platform

### Documentation

The team decide to document their project in markdown using Plant UML diagrams. Ideally
they would collaborate with GSuite or Confluence, but this approach will allow them to
version docs alongside their code.

### Debugging

Apigee Trace
Third party logging
Analytics

TODO video of how to actually set it up

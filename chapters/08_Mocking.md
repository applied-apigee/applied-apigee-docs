## Mocking

### Static Mocks

The simplest way that the team can mock an endpoint, is to use an Assign Message 
policy. 

TODO video

This is great for one or two responses, but it is possible that addition logic will
be required to handle multiple responses, simulate latency and add error handling.
To easily implement this, the team implement a Hosted Targets based mock using the
`apimocker` library.

TODO video

Many pieces of test data are provided to provide a lifelike experience for developers
to code against.

### Specification-based Mocking

It is possible to derive dummy responses from Open API Specifications. The quality
of this data is only as good as the specification, and typically contains values
such as `"Sample String"`.

TODO video 

At the time of writing, these mocks are used as a short term solution when specifications
are complex and mocks require a low cost of maintenance.

### Dynamic Mocks

If the team want to provide the most realistic experience, then they must implement
dynamic mocks that allow data to be persisted.

In order to reduce cost of maintenance, this should use the same code based as the
real backend. This way, the team don't have to maintain two separate code bases.

On the other hand, this still requires a dedicated team and more infrastructure to be
maintained, so should only be implemented for premium consumers.

TODO video

# CH1

Programming - outputting a solution
Soft Eng - Maintaining and Evolving that solution as the usecase changes.

**Hyrum's Law** - The contracts defined in an API don't need to be upheld - what should define the development is how your users use the API.
    - IMO this means the contracts were ill-defined and need to be renewed and that's okay - this is a cycle that is defined by the change in user behaviour.

Data-driven design is important but usually data is not the only thing used to create a soln. It's usually Data + asumption + precendent (IMO pre-existing setup for how we build) + argument.

Data-driven design requires changing the design as the data changes. **Mistakes are inevitable**.

Migrations & Upgrades can be painful - the first one usually is. Instead of avoiding further migrations & upgrades (which inhibits growth and moving forward with tech), learn from the mistakes and of the first one and **improve the process**.
- Doing Migrations / Upgrades more often will allow for a more streamlined process over time.
- Case Study: Google mentioned their Compiler Migration of 2006 being painful.

**Shift left**: In the phase of development to release of software, shifting problem identification to the left (problem identification: testing, checking if dependencies are up to date & what vulnerabilities are there) reduces cost.
- Doing these things after prod release can be very expensive.
- Catching it early allows for it to be incorporated it into the design.

**Internal Google Policy: Beyonce Rule**
- If you like it you should've put a CI test on it
- Infrastucture changes that result in downtime for a service are not the fault of the infra structure change (or the Google SRE org) rather it's from only have 1-off tests for that service that have not been incorporated into the CI.

If your code that you wrote is long-term then you cannot guarantee that what it depends on will not change.
- The hash ordering example ex. the long-term answer for hashing is that the order is never guaranteed. But in the short-term if there's no changes to your hardware, data structure or language runtime then it's safe to assume the order will be guaranteed
- If nothing the code depends on will change during it's life time then it's safe.


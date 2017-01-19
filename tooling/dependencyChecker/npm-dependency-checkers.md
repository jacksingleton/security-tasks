## Task: Add an npm dependency checker into the CI pipeline
**Description:**

Several tools exist to attempt to detect when updates for JavaScript packages
managed using npm are available due to publicly disclosed security
vulnerabilities. These include:

* Node Security Project nsp (free) https://github.com/nodesecurity/nsp
* Snyk (commercial; also for Ruby) https://snyk.io/

The team should evaluate these tools and choose one that is right for their
needs.

The tool should be configured to email the development team when updates are
found due to security vulnerabilities. The team can then investigate the
vulnerable component and apply an upgrade if it is found to be a risk.

There are two scenarios to regularly run the tool:

* Per check-in for applications in active development. The team can choose
  whether to break the build when a new vulnerable component is identified.
* On a schedule for deployed versions of the application. This way the team will
  still be alerted in case the current development branch has already been
  updated but the deployed version has not, or when the application is no longer
  being actively maintained.

**Acceptance criteria:**

* When a check-in is made to the revision control system, then the tool should
  be run against the dependency manifest for the branch the check-in was made
  into.
* When a regular interval of time elapses, then the tool should be run against
  the dependency manifest for any deployed versions of the application.
* When a vulnerable component is identified, then it should send an email to
  inform the team.
* When an error occurs running the dependency checking tool, then it should send
  an email to inform the team.

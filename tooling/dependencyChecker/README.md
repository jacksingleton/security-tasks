# Dependency Checkers for the Automated Pipeline

## What is it?
* A dependency checker is a tool that attempts to detect when updates are
  available for third party dependencies (libraries, frameworks, etc) used in
  your application due to publicly disclosed security vulnerabilities.

## Why is it needed?
* Up to 90% of many applications are comprised of third party components.
* Applications often inadvertently introduce vulnerabilities by failing to
  update components in a timely manner or by pulling in outdated components with
  vulnerabilities.

## When should I use this?
* If you leverage technologies that use third party components and that have a
  dependency checker available.

## Tasks
Below are tasks organized by technical stack to introduce dependency checkers
into your automated CI Pipeline.

* Java, .NET: [OWASP Dependency-Check](owasp-dependency-check.md)
* JavaScript (npm, Node.js): [npm dependency checkers](npm-dependency-checkers.md)

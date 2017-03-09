# Secret Management

## What is it?
* Secrets such as passwords, credentials, access tokens, certificates, and other
  confidential information are something we can't allow to fall into the wrong
  hands. A secret management tool makes it possible to manage these kinds of
  secrets safely.

## Why is it needed?
* Applications rely on secrets to access services such as databases, encrypted
  files, and to securely communicate with other applications and systems.
* Team members may also need a way to manage and share similar confidential
  information.
* Writing secrets in a place they can be easily retrieved exposes projects to
  unnecessary risks. This includes doing things like writing them on sticky
  notes or in source code or configuration files.

## Tasks
More than one tool may be needed if there is a need to manage secrets for both
team members and applications. Security needs to be useable and a secret manager
intended for use by applications automatically deployed in a container may not
be the best choice for human users. In addition, we can use tools to help reduce
the risk of committing sensitive information to source control.

* [Choose a secret management tool for use by the team](password-manager.md)
* Choose a secret management tool for use by the applications
* [Choose a tool to help keep secrets out of source control](secrets-source-control.md)

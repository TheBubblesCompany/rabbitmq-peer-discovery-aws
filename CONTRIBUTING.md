## Overview

RabbitMQ projects use pull requests to discuss, collaborate on and accept code contributions.
Pull requests is the primary place of discussing code changes.

## How to Contribute

The process is fairly standard:

 * Fork the repository or repositories you plan on contributing to
 * Clone [RabbitMQ umbrella repository](https://github.com/rabbitmq/rabbitmq-public-umbrella)
 * `cd umbrella`, `make co`
 * Create a branch with a descriptive name in the relevant repositories
 * Make your changes, run tests, commit with a [descriptive message](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html), push to your fork
 * Submit pull requests with an explanation what has been changed and **why**
 * Submit a filled out and signed [Contributor Agreement](https://github.com/rabbitmq/ca#how-to-submit) if needed (see below)
 * Be patient. We will get to your pull request eventually

If what you are going to work on is a substantial change, please first ask the core team
of their opinion on [RabbitMQ mailing list](https://groups.google.com/forum/#!forum/rabbitmq-users).


## Code of Conduct

See [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).


## Running Tests

Integration tests of this plugin need AWS credentials and an SSH key pair.
The credentials can be set in two ways:

 * Via a `$HOME/.aws/credentials` file
 * Using the `AWS_SECRET_ACCESS_KEY` and `AWS_ACCESS_KEY_ID`

Below is an example of a `.aws/credentials` file:

``` ini
[default]
aws_access_key_id = EXAMPLEACCESSKEYID
aws_secret_access_key = a-secret-access-key
```

A private SSH key is also required to transfer a locally compiled version
of the repository and transfer it to all remote nodes. It is set via the `SSH_KEY` environment
variable.

    make ct-integration

will run integration tests [on AWS] only.

    make tests

will run all suites.


## Contributor Agreement

If you want to contribute a non-trivial change, please submit a signed copy of our
[Contributor Agreement](https://github.com/rabbitmq/ca#how-to-submit) around the time
you submit your pull request. This will make it much easier (in some cases, possible)
for the RabbitMQ team at Pivotal to merge your contribution.


## Where to Ask Questions

If something isn't clear, feel free to ask on our [mailing list](https://groups.google.com/forum/#!forum/rabbitmq-users).

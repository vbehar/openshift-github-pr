# OpenShift GitHub Pull-Request

**Work In Progress: This is RDD: Readme Driven Development. So there is no code yet, just ideas for the moment.**

The idea is to automatically create a new "environment" for your application each time your create a Pull Request on GitHub.

Basically, you create a Pull Request, and automatically this controller will:

* create a new BuildConfig to build the pull request
* create a new DeploymentConfig to deploy the newly build image
* create the service/route to expose your pods
* comment on the pull request with the URL of the route
* use the [GitHub Status API](https://developer.github.com/v3/repos/statuses/) to publish the build/deployment status on the PR page

And when you close the PR, everything will be deleted.

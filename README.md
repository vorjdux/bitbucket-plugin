bitbucket-plugin
================

[![Build Status](https://jenkins.ci.cloudbees.com/job/plugins/job/bitbucket-plugin/badge/icon)](https://jenkins.ci.cloudbees.com/job/plugins/job/bitbucket-plugin/)

See details on [wiki](https://wiki.jenkins-ci.org/display/JENKINS/BitBucket+Plugin)

# Job DSL
The plugin supports the following dsl extension to enable bitbucket pushes to trigger a build:

```
freeStyleJob('test-job') {
  triggers{
    bitbucketPush()
  }
}
```

# Get source, Compile, and Install
To compile the plugin and install on Jenkins:

```
$ sudo apt update
$ sudo apt install maven
$ git clone git@github.com:vorjdux/bitbucket-plugin.git
$ cd bitbucket-plugin
$ mvn install
$ mvn package
# Upload the generated target/bitbucket.hpi in the plugins manager on your Jenkins web cli instance. 
```

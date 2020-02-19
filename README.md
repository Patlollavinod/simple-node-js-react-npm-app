# simple-node-js-react-npm-app

This repository is for the
[Build a Node.js and React app with npm](https://jenkins.io/doc/tutorials/build-a-node-js-and-react-app-with-npm/)
tutorial in the [Jenkins User Documentation](https://jenkins.io/doc/).

The repository contains a simple Node.js and React application which generates
a web page with the content "Welcome to React" and is accompanied by a test to
check that the application renders satisfactorily.

The `jenkins` directory contains an example of the `Jenkinsfile` (i.e. Pipeline)
you'll be creating yourself during the tutorial and the `scripts` subdirectory
contains shell scripts with commands that are executed when Jenkins processes
the "Test" and "Deliver" stages of your Pipeline.

## Installation

# SonarScanner

Login to Jenkins server and download sonarscanner to the /opt directory.
```sh
$ cd /opt

$ wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-4.2.0.1873-linux.zip

$ unzip sonar-scanner-cli-4.2.0.1873-linux.zip

$ mv sonar-scanner-cli-4.2.0.1873-linux sonar-scanner

This will the set to global configuration.

$ export PATH=/opt/sonar-scanner/bin:$PATH

$ sonar-scanner –version
```

# Configuring SonnarScanner in Jenkins

1. Go to Manage Jenkins > Global Tool Configuration.
![alt text](https://github.com/edsherwin/simple-node-js-react-npm-app/blob/master/img/1.png)
2. Find SonarQube Scanner and click on SonarQube Scanner.
3. Input any Name and the path of sonar scanner.
4. Unselect the Install automatically.
![alt text](https://github.com/edsherwin/simple-node-js-react-npm-app/blob/master/img/2.png)
5. Then, Save configurations.

# Creating a declarative Pipeline Job Project

1. Go to Jenkins > New Item > Pipeline.
2. Input any name for your Job
3. Input the details below on the configuration.
![alt text](https://github.com/edsherwin/simple-node-js-react-npm-app/blob/master/img/3.png)
- Definition: Pipeline script from SCM
- SCM: Git
- Repostiries: Git URL and Git Credentials
- Branches to Build: */master ("depends on your preference")
- Script Path: Jenkinsfile




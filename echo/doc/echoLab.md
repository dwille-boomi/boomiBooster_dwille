# Echo Service Lab

This document will walk you step-by-step through building out your echo service. By the end of this lab, you should have a Web Service Listener to which you can POST a sample payload and have it echoed back to the requesting client.

## Process Overview

This is a very basic Process with only two shapes:

- Start Shape: This defines your Listener (Protocol, Operation, Profile)
- Reflect Current Document: This will return your Document (payload/message body) back to the requesting client.

Your final process will look similar to this:

![Process Overview](../res/processOverview.png "Process Overview")

## Build the Start Shape

![Start Shape](../res/startShape.png "Start Shape")

## Build the Web Services Server Listen Operation

![Connector Operation](../res/connectorOperation.png "Connector Operation")

## Build the JSON Profile

![JSON Profile](../res/jsonProfile.png "JSON Profile")

## Buildout the Process

![End Shape](../res/endShape.png "End Shape")

## Package and Deploy the Process

## Configure the Webserver

![Atom Management](../res/atomManagement.png "Atom Management")
![Web Server Setup](../res/webServerSetup.png "Web Server Setup")
![Web Server Auth](../res/webServerAuth.png "Web Server Auth")

## Test your Process


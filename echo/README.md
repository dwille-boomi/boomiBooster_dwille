# Basic Echo Service

Step-by-Step procedure for creating a simple Process that will listen for and echo (reflect) back a sample HTTP Request payload.

## Purpose and Background

The objective of this exercise is to build a Process that will Listen for an HTTP POST with a payload, and reflect it back to the requestor. This is useful for the following reasons:

- To learn some of the very basics of the Boomi platform.
- To lay the foundation of a sandbox Process to inject and test different shapes.

## Prerequisites

The following prerequisites should be completed before the workshop starts.

- Have access to the Boomi Atomsphere Platform
- Basic knowledge of how to work in the Boomi Platform
- Have a deployed Atom/Environment
- Know how to create a Packaged Component
- Know how to Deploy a Process
- Basic knowledge on how to use a test client like Postman or CURL

I strongly suggest completing the Boomi Essentials course before this lab if you have not done so already.

## Process

- ***Step One***: [Build the Start Shape](doc/echoLab.md#build-the-start-shape)
- ***Step Two***: [Build the Web Services Server Listen Operation](doc/echoLab.md#build-the-web-services-server-listen-operation)
- ***Step Three***: [Build the JSON Profile](doc/echoLab.md#build-the-json-profile)
- ***Step Four***: [Buildout the Process](doc/echoLab.md#buildout-the-process)
- ***Step Five***: [Package and Deploy the Process](doc/echoLab.md#package-and-deploy-the-process)
- ***Step Six***: [Configure the Webserver](doc/echoLab.md#configure-the-webserver)
- ***Step Seven***: [Test your Process](doc/echoLab.md#test-your-process)

## Terminology

To execute on this lab, you should be familiar with the following terms and concepts:

- Process
- Web Server Connector/Operation
- Shapes
- JSON Profile
- Atom

## Additional Documentation

Boomi Docs: https://help.boomi.com/bundle/integration/page/c-atm-Getting_started.html

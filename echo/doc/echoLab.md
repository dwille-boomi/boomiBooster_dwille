# Echo Service Lab

This document will walk you step-by-step through building out your echo service. 

## Expected Outcome
By the end of this lab, you should have a Web Service Listener to which you can POST the provided sample payload and have it echoed back to the requesting client. Note: If you wish to work with different request payloads, you will need to modify your JSON Profile accordingly, which is not covered in this lab.

## Process Overview

This is a very basic Process with only two shapes:

- ***Start Shape***: This defines your Listener (Protocol, Operation, Profile)
- ***Reflect Current Document***: This will return your Document (payload/message body) back to the requesting client.

Your final Process will look similar to this:

![Process Overview](../res/processOverview.png "Process Overview")

## Prerequisites

- Download the [Sample JSON Profile](samples/sampleProfile.json "Sample JSON Profile")
- Download the [Sample Request](test/sampleRequest.json "Sample Request")

## Build the Start Shape

1. Create a new Process in your directory of choice.
2. Modify the Process name at the top of the tab as desired (eg Basic Echo).
3. Modify your Start Shape as follows, completing the Web Service Operation step in the section below as required:
	* ***Type***: Connector
	* ***Display Name***: Any alias you desire, eg. Generic HTTP Listener
	* ***Connector***: Web Services Server
	* ***Action***: Listen
	* ***Operation***: Click the '+' to [Build the Web Services Server Listen Operation](#build-the-web-services-server-listen-operation)
4. Click OK to finish the Start Shape. Save.

Once complete, it should look similar to the following:

![Start Shape](../res/startShape.png "Start Shape")

## Build the Web Services Server Listen Operation

After being redirected to the New Web Services Server Connector Operation dialog, complete the following steps:

1. Modify your Operation name at the top of the tab as desired (eg Listen for POST).
2. Modify the Options as follows, completing the JSON Profile step in the section below as required:
	* ***Simple URL Path***: This will be automatically updated as you modify the rest of the options. You will want to capture this value for later use.
	* ***Operation Type***: CREATE (this will listen for a POST with a payload we can reflect)
	* ***Object***: Whatever you desire. For my test I used 'dwille'. This will be used in defining your resource path.
	* ***Expected Input Type***: Single JSON Object (we will use a very basic JSON Payload for this lab).
	* ***Request Profile***: Click the '+' to [Build the JSON Profile](#build-the-json-profile)
	* ***Response Output Type***: Single JSON Object (as we are simply reflecting the request payload)
	* ***Response Profile***: Select the same JSON Profile you build for the Request Profile as we are simply reflecting the request payload.
3. Click Save and Close. This should take you back to the Process interface to finish the [Build the Start Shape](#build-the-start-shape) step above.

Once complete, it should look similar to the following:

![Connector Operation](../res/connectorOperation.png "Connector Operation")

Ensure you capture:

- Simple URL Path (eg /ws/simple/createDwille)

## Build the JSON Profile

After being redirected to the New JSON Profile dialog, complete the following steps:

1. Modify your Operation name at the top of the tab as desired (eg Basic JSON TEST Profile).
2. Click either the "Import a Profile" or "Import" button. Select JSON File and chooe the [Sample JSON Profile](samples/sampleProfile.json "Sample JSON Profile") you downloaded in the [Prerequisites](#prerequisites) section. The Import interface should look similar to the below image. Click Next, Finish.

![JSON Import](../res/jsonImport.png "JSON Import")

3. Save and Close. This should take you back to the to the interface to complete the [Web Services Server Listen Operation](#build-the-web-services-server-listen-operation) step.

Your finished JSON Profile should look similar to the following:

![JSON Profile](../res/jsonProfile.png "JSON Profile")

## Buildout the Process

Now that we have created our Web Service Listener and Profile, we need to return the request payload back to the requesting client.

1. Drag the Return Documents Shape onto the Process Canvas.
2. Change the Display Name as desired and click OK.

![End Shape](../res/endShape.png "End Shape")

3. Connect the Start Shape to the Return Documents Shape.
4. Save.

Your Process should now look similar to the image shown:

![Process Completed](../res/processOverview.png "Process Completed")

## Package and Deploy the Process



## Configure the Webserver

![Atom Management](../res/atomManagement.png "Atom Management")
![Web Server Setup](../res/webServerSetup.png "Web Server Setup")
![Web Server Auth](../res/webServerAuth.png "Web Server Auth")

## Test your Process




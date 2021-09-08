# Create Events in Instana

This article explains about how to create Events in Instana.

<img src="../images/image-instana-waiops-integration.png">

## Pre-Requisite

- The `kubernetes based application` is deployed in an Openshift Container Platform or on Kubernetes Cluster.

- `Application Perspective` is already created in Instana for the above deployed application. 

- `Custom Payload` is already created in Instana. 

## Objective

The Objective is to create / configure an Event based on JVM memory usage for a given Application Perspective.

- Application called `iLender` is deployed in `ilend-ns` namespace. 
- Application Perspective called `iLend` is already created and available in the Instana.
- When the `JVM memory usage` is more than `80%` then an event named `CreditScore memory high issue` to be created.

## Steps

1. Choose the menu `Events` under the configuration section. 

1. Click on `New Event` button. 

<img src="images/6-event-00001.png">

3. Enter the values for the below fields as shown in the screenshot. 

- Name
- Description
- Issue Severity
- Incident
- Grace Period

<img src="images/6-event-00002.png">

4. Enter the values for the below fields as shown in the screenshot. 

- Source
- Entity Type
- Metric
- Time Window
- Aggregation
- Operator
- Percentage
- Apply On

5. Click on `Add Application Perspective` link.

<img src="images/6-event-00003.png">

6. Choose the `iLend` from the given list. You can choose any as per your need.

7. Click on `Add 1 Application Perspective` button.

<img src="images/6-event-00004.png">

8. Click on the `Create` button to create an event.

<img src="images/6-event-00005.png">

9. An event called `CreditScore memory high issue` is created and displayed like the below.

<img src="images/6-event-00006.png">

## Next Step

Event is created here. You can create `Alert Channels` and `Alerts` and etc to complete Instana with Watson AIOps Integration.

Prev : [Create Custom Payload in Instana](../3-custom-payload)

Next : [Create Alert Channels in Instana](../5-alert-channel)

Home : [Integrating Instana with Watson AIOps](../)
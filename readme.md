# Integrating Instana with Watson AIOps

This article explains about how to integrate Instana with Watson AIOps.

<img src="images/image-instana-waiops-integration.png">

## Integration flow

1. The managed environment containing kubernetes based application is observed by using Instana. The application perspective created in Instana would show the dashboard.

2. An event is generated when the observations meets the specified critera for the event 

3. Based on the generated event, alert is created  

4. Custom Payload data is also get appended to the alert data.

5. Alert is send to the alert channel

6. Alert Channel would send the alert to the Webhook associated with the Watson AIOps.


## Integration Steps

Integration consists of the below steps. Perform all the steps below to integrate Instana with Watson AIOps.

### Create Instana Webhook in Watson AIOps Event Manager (NOI)

Contains steps to create Webhook in Watson AIOps Event Manager (NOI) Console to receive events from Instana.

[Create Instana Webhook in Watson AIOps Event Manager (NOI)](1-webhook)


### Create Application in Instana

Contains steps to create Application or Application Perspective in Instana for the kubernetes based microservices application.

[Create Application in Instana](2-application)


### Create Custom Payload in Instana

Contains steps to create Custom Payload in Instana.

This helps the Instana to send additional info along with the alert data to the alert channels.

[Create Custom Payload in Instana](3-custom-payload)


### Create Event in Instana

Contains steps to create Event in Instana based on JVM memory usage for a given Application Perspective.

[Create Event in Instana](4-event)


### Create Alert Channel in Instana

Contains steps to create Alert Channels in Instana that points to the Webhook in IBM Watson AIOps Event Manager (NOI).

[Create Alert Channel in Instana](5-alert-channel)


### Create Alert in Instana

Contains steps to create Alert in Instana about memory high issue pointing to above created alert channel.

[Create Alert in Instana](6-alert)
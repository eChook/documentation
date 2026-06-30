# Node-RED Integration

{% hint style="warning" %}
This page assumes knowledge of Node-RED and JavaScript. If you are familiar with Node-RED, then eChook is simple to integrate. If you have not used it before, the best path is to go to [nodered.org](https://nodered.org/) or your search engine of choice to get started, and return once you are up and running.

There is a Node-RED getting started guide here: [https://nodered.org/docs/getting-started/](https://nodered.org/docs/getting-started/)
{% endhint %}

### Connecting Node-RED to eChook Live Data

This section assumes that Node-RED is already installed and running.

1. Create an account for your car at [live.echook.uk](https://live.echook.uk/) and go to settings > API and copy the Get Live Data (polling) url that is provided and includes your unique car ID.
2. In the Omni app, select upload to eChook Private Live Data enter your login details.
3. For Node-RED setup, download the JSON file below and import it to your Node-RED dashboard by right-clicking on the background > insert > import, then selecting the downloaded file.

{% file src="../.gitbook/assets/eChook-node-red-flows.json" %}

You should now have a dashboard that looks like this:

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

Double click the http request block, and enter the URL you copied in step 1, then deploy the changes.

#### How it works

Every 2 seconds the inject block on the left triggers the HTTP request. This asks the server for the latest data from the car, which is formatted into a JSON object by the JSON block, and then split out into separate flows in the 'eChook Data Split' block. Mouse over the output connectors to see what data each provides. The output data is in the format of '{name:xyz, value:123}, so is accessible in later blocks using msg.payload.value and msg.payload.name.

{% hint style="warning" %}
PLEASE PLEASE PLEASE - stop Node-RED, or disable the inject node when you are not using it. Node-RED runs continually in the background, and it would be very easy to leave it pinging the eChook server 24/7 unnecessarily, which will just increase its load, increase my costs, and degrade the service for everyone.
{% endhint %}

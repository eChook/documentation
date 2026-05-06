# Node-RED Integration

{% hint style="warning" %}
This page assumes knowledge of Node-RED and JavaScript. If you are familiar with Node-RED, then eChook is simple to integrate. If you have not used it before, the best path is to go to [nodered.org](https://nodered.org/) or your search engine of choice to get started, and return once you are up and running.

There is a Node-RED getting started guide here: [https://nodered.org/docs/getting-started/](https://nodered.org/docs/getting-started/)
{% endhint %}

#### Farewell Dweet.io

This section used to rely on the dweet.io service provided by Bug Labs, which has unfortunately been suspended. The work around is in some ways an improvement - as it uses eChook's own server, your telemetry data is no longer publicly exposed, and as a result the apps will allow location to be sent. The only downside being you do need to create an account on [data.echook.uk](https://data.echook.uk).

### Connecting Node-RED to eChook Live Data

This section assumes that Node-RED is already installed and running.

1. Create an account for your car at [data.echook.uk](https://data.echook.uk), then bring up the developer tools in your browser (normally F12, or Ctrl+Shift+i) and select the 'Console' tab. After a fresh login to the website, near the top of the console should be a printed web address, along the lines of https://data.echook.uk/api/get/-----Long-Unique-Key------. This address is unique to your car. Copy it for later.<br>

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

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

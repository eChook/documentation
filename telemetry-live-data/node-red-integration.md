# Node-Red Integration

{% hint style="warning" %}
This page assumes a knowledge of Node-Red and Javascript. If you are familiar with Node-Red then the eChook is simple to integrate. If you've not used it before, best path would be to go to [nodered.org](https://nodered.org/) or your search engine of choice to get started, and return to this once you're up and running.
{% endhint %}

For those that need it, there is a  node-red getting started guide here: [https://nodered.org/docs/getting-started/](https://nodered.org/docs/getting-started/)

#### Farewell Dweet.io

This section used to rely on the dweet.io service provided by Bug Labs, which has unfortunately been suspended.

### Connecting Node Red to eChook Live Data

This section assumes that node-red is already installed and running.

1. Create an account for your car at data.echook.uk. Bring up the developer tools in your browser (normally F12, or Ctrl+Shift+i) and select the 'Console' tab. After a fresh login to the website, near the top of the console should be a printed web address, along the lines of https://data.echook.uk/api/get/-----Long-Unique-Key------. This address is unique to your car. Copy it for later.\


<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

2. In the Omni app, select upload to eChook Private Live Data enter your login details.
3. Download the json file below, then go to your node red dashboard and import it by right clicking on the background > insert > import, and selecting the downloaded file.

{% file src="../.gitbook/assets/eChook-node-red-flows.json" %}

You should now have a dashboard that looks like this:

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

Double click the http request block, and enter the URL you copied in step 1, then deploy the changes.

#### How it works

Every 2 seconds the inject block on the left triggers the HTTP request. This asks the server for the latest data from the car, which is formatted into a JSON object by the JSON block, and then split out into separate flows in the 'eChook Data Split' block. Mouse over the output to see what data it gives. The output data is in the format of {name:xyz, value:123}, so id accessible in later blocks using msg.payload.value and msg.payload.name.

{% hint style="warning" %}
PLEASE PLEASE PLEASE - stop node red, or disable the inject node when you are not using it. Node red runs continually in the background, and it would be very easy to leave it pinging the eChook server 24/7 unnecessarily, which will just increase it's load, increase my costs and degrade the service for everyone.
{% endhint %}

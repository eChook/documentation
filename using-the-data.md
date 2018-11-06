# Using the Data

It’s time to get the data off the phone and onto a computer for some useful analysis.

## Retrieving data from phone

In the eChook app settings, the top option is to share data. Tap this to display a list of ways to send the data file to via service you wish.

Alternatively, the data is saved in a .csv file in the phone's downloads folder so can also be retrieved via a file manager app, or via a USB connection to a computer.

## Opening the Data

Open the arduino.csv file in a spreadsheet programme such as Excel. Data identifying names will be along the top, and the data below. The one bit of data that is not immediately readable is the timestamp, as this is recorded in [Unix Time](https://en.wikipedia.org/wiki/Unix_time), as milliseconds since 00:00:00 1st January 1970.

This needs to be converted in excel using the following formula:

`=A2/(1000*60*60*24)+"1/1/1970"`

Create a new column for Time and set the cell number format to Time. Enter the formula above, replacing ‘A2’ with the timestamp cell on the same row. Once the cell shows a legible timestamp, select it and double click the bottom right corner of the cell to propagate the calculation down the whole sheet.

This converts milliseconds to days \(the multiplication\) and adds them to the start point of Unix Time. This is now a value that excel will recognise as a time and date when the cell format is set to time.

![](https://lh3.googleusercontent.com/jIqXy8nnbeA0GAnkM9vsIVyZVOtupkB5ZFSBlOhHQITRr30Bi7VPci9UwKNB8gqG6S8jBHSXbglZ-cJTD6mTFXAP6u8ZtIOHtFBheuZfx_9AXf1sHQN0Z6yoInT1ycdAZAHPh88A)

## Graphing the data <a id="graphing-the-data"></a>

To start looking at the data in a meaningful way, graphs are needed. To start with, select the columns Time, Voltage and Current, then go to Insert&gt;Charts&gt;Scatter with Smooth lines. This will give a voltage and current over time graph. Add and remove data to see what you want!


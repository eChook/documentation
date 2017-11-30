## Premium Telemetry

Caution - here there be bugs. You can get premium up and running for free, but messages are limited to 1 every 5 seconds instead of one per second.

The ‘premium’ option makes the telemetry data private, and also stores all data on the dweet.io servers for a month. It involves signing up to [dweetpro.io](https://dweetpro.io/pricing.html) and purchasing a locked ‘thing’. At the time of writing that is 1.99USD per month. I will note that my experience with dweet pro has not been amazing... it works but is slower than the free version and the website is still in beta and not the most clear.

### Setting up premium telemetry

First, set up an account on dweetpro.io. Go to collections and set up a new ‘Thing’ named as you like.

![](https://lh4.googleusercontent.com/LIMSicMbtBDXTbU027QrvsGb6boTXS5CwlDAUk6uzNTvzbxHXWz6C2JJFoSEbzDlG6gAMZ0F5TexZ3T0ZuI1Q8ebdgfnwmkEmmqBGj5W1SbAn9jgroFGT8sORYaKCfwmyy50nVL8)

Click on the ‘thing’ and you will see the following page:

![](https://lh6.googleusercontent.com/_2vLSecHstpyoBPu2DotuAUNpP6VJu0aU2ebft83fphci-wrfBMQO_RQfaRhV3ukIAb9KWCjWHsIkY7gfWweEsx-x1R_iM0OEkJ95noI5YEZwVm7moApmgbUj_By_nF-AyvVp425)

  


Copy the ‘Thing Master Key’ and send it to the Android phone that the eChook app is on - you will need to paste it into the apps settings.

Now go to the eChook app settings:

![](https://lh5.googleusercontent.com/t3cOYXqG8h-55je1e3r1fELEk7WRAksZSf0odKzjkv3qNB0__1MHuSgK5Komaw8Ce_Pr6bQrHAAt_TeZajTNHgZB-IIgs5opDZdQkJVY0jKn_Ty7TNgo-gGgkse9j-GpSxlm_Wqn "Screenshot\_2017-09-16-21-42-15-288\_com.ben.drivenbluetooth.png")Enter the ‘Thing’ name you chose, then enter your DweetPro login details in the username and password boxes. Finally, copy the master key in. Now enable ‘Use DweetPro’. Ensure the box above, ‘Enable live data’is also enabled. This should start the data upload.

To view the data, go to[freeboard.io](https://freeboard.io/)and create an account. Start a new dashboard or make a clone of one we have created here:[https://freeboard.io/board/WwX85W](https://freeboard.io/board/WwX85W)

Assuming you have cloned the existing board, click on the weChookLocked data source. You will see the following:

![](https://lh4.googleusercontent.com/mZWuYAfM0ipZqgn8orJYU-SKFGnJY-oN_UemF2UH1PIIBUp3v5xSF-ELkisy7NWLNq9CeBNCV4DjegB-Bm7IWLl-U3titHiuneaA3zfrtpvrE_CofQioJ7oD55wLkRagPtIQcUhB)

Leave the ‘Name’ alone as changing this will break the preconfigured displays. If you are creating your own board name the data source as you like.

Replace ‘Thing Name’ with your thing name. Go back to the page on dweetpro.io that you got the master key from and copy the read key into freeboard.

Return to dweetPro and click on the dweet icon in the top left to return to the account overview page:  


![](https://lh3.googleusercontent.com/Xk9PLU-WG47zrSJ__7bo4M-GgULdBca3TVh-PnU0bpgD6EjfP7BCpJKrZzksGG_NgyyztHRA-NGwsrdaGAbYHrw1ip93Bap8J64t8rrnRCnk9d52WWAqJx5dDDSmbamzc780zEMA)

Use the button circled in red to copy your account token. Paste this into the final box on freeboard and press save. To start receiving data ensure the phone is set up and on with the eChook app running \(maybe put it in demo mode to make it easier to see if data is coming through\). On freeboard press the refresh button next to your datasource a few times to start receiving data \(a bug freeboard are aware of\).

  



# Lap Counting

Lap detection requires that Location detection is enabled in settings and that the throttle signal is wired into the eChook.

Before the race an ‘observer’ position needs to be set on the map, ideally in the middle of the racing circuit. To do this move the map so you can see the centre of the circuit \(or a best guess if the circuit isn’t shown\) and tap where you want the observer to be. A pin will be dropped with prompt to click to confirm. Tap again to confirm location. A prompt will now appear asking to confirm if you are racing in a clockwise or anticlockwise direction. This is shown below, unfortunately nowhere near a race track.

![](https://lh4.googleusercontent.com/ELcx8VIJh70IqE_Hvh8jAgMxzxmKkgDGAm9PCp0vCwxtNl_ZizVJ_ii0aGgTfXy74kKWgK64IaF3mtXZ--2C1vcbw4We66jHoK1xVNWOh7V6IuqtnJSe3gYNAIFWe_XPAuc6TltH "507dqH\_OzyS7QIlNWe9HSlaO-qXyr9Wuh\_\_FmwYWKM7awGnwEJDlOd2vVvw9jAYB96kPWxDlRv1yjuCOCbqVtiBz8BC87ewOQ5wuv\_457Qc8NrOvloYX5X\_pXwMS88g3pePK5oGrslmDgiWpwnUezBaJvenW02\_fzJy4sF9dDtW9kj3-CxRSkgRbB7ST\_2N8kAa7F-tLY4H\_iWiYOEqT-7SSdsI6QPAy3drYPaawP82wedw9tKfzgNY71BKGmSOI61j2grXWNG47IN139\_aKylrmVKC7z5nawV2T\_y90dM0LrhIzorKv5PVelPqE37jDwCO00\_vJ0Q4117BMO18jNvFhOlkkzyPwkN1E5QZeVZSifaWH7TC9Z9fXyegvCkBllAUt05viWqC0u-qUEjJrWVjuJV1i7\_tzr-uJLqB1fOu4wAS-u9SkWxttRf3N6p-B65AElzGOfO6V\_n1BuPrTp8CMAW4zoLlwOcT6PAxbexc7wUtYj1jO\_82vR1lQF8nAt9fKLla1uZI1Qnpa1u00Fp9Ko7flrBjQr6ecYo7WAjYjJebw2Ju6LEWwJBp9MHjsZgR7aPUrug4yRKrvbNK-sQCJJd5Cv3KvZ5SDz5\_zitfUdRajGIcinQ=w600-h338-no")

Pressing the Launch button starts launch detection. Now once the throttle is pressed \(&gt;20% for a variable throttle\) the app starts the lap timer, and notes the cars bearing to the observer position set earlier. Every time the car passes this position in the race, a lap is counted.

### How It Works

Each GPS update, the app calculates the bearing from the observer to the car in degrees. During the race the car moves in circles around the observer. When the throttle was initially pressed in launch mode, that bearing was recorded. During the race every time the car passes that original bearing, a lap is recorded.

  



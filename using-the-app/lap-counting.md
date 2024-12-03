# Lap Counting

Lap detection requires that Location is enabled in settings and that the throttle signal is wired into the eChook.

{% tabs %}
{% tab title="OMNI Telemetry" %}
On start-up, the app is waiting for 30%+ throttle input to start lap detection (dismissible via the notification at the bottom of the screen).

The lap detection is automatic from here - no more configuration required.
{% endtab %}

{% tab title="eChook App" %}
Before the race an ‘observer’ position needs to be set on the map, somewhere in the middle of the racing circuit. To do this move the map so you can see the centre of the circuit (or a best guess if the circuit isn’t shown) and tap where you want the observer to be. A pin will be dropped with prompt to click to confirm. Tap again to confirm location. A prompt will now appear asking to confirm if you are racing in a clockwise or anticlockwise direction. This is shown below, unfortunately nowhere near a race track.

![](https://lh4.googleusercontent.com/ELcx8VIJh70IqE_Hvh8jAgMxzxmKkgDGAm9PCp0vCwxtNl_ZizVJ_ii0aGgTfXy74kKWgK64IaF3mtXZ--2C1vcbw4We66jHoK1xVNWOh7V6IuqtnJSe3gYNAIFWe_XPAuc6TltH)

Pressing the Launch button starts launch detection. Now once the throttle is pressed (>20% for a variable throttle) the app starts the lap timer, and notes the cars bearing in degrees to the observer position set earlier. Every time the car passes this position in the race, a lap is counted.

## How It Works

Each GPS update, the app calculates the bearing from the observer to the car in degrees. During the race the car moves in circles around the observer. When the throttle was initially pressed in launch mode, that bearing was recorded. During the race every time the car passes that original bearing, a lap is recorded.
{% endtab %}
{% endtabs %}


# PWM Output

![](https://lh4.googleusercontent.com/mk6F9d-bMzF6-ahLecNQvt065uJKWdKmUQIoep-Y10aA3uWrqFt35Vax9ZluOVd9H3RqlNEyfwfk1cHga_LHQJCUswCi6vR_9bd1ienbtBoaVx3HHcQwB75tm-sYYiwiT3G6Mlc5)

The PWM output directly from the Arduino is unlikely to be able to provide enough current to drive a motor controller some distance away, so a transistor based PWM buffer is implemented.

R13 provides a strong pull down to the PWM output when the transistor is closed. R14 provides some termination to the ‘transmission line’ between the eChook and whatever the PWM is driving. Ideally this would be tuned to application.

The LED simply indicates the PWM state - on when PWM is 100% and fades with PWM percentage. R15 drops the voltage for the LED.


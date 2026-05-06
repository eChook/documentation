# PWM Output

![](https://lh4.googleusercontent.com/mk6F9d-bMzF6-ahLecNQvt065uJKWdKmUQIoep-Y10aA3uWrqFt35Vax9ZluOVd9H3RqlNEyfwfk1cHga_LHQJCUswCi6vR_9bd1ienbtBoaVx3HHcQwB75tm-sYYiwiT3G6Mlc5)

The PWM output directly from the Arduino is unlikely to provide enough current to drive a motor controller some distance away, so a transistor-based PWM buffer is implemented.

R13 provides a strong pull-down to the PWM output when the transistor is off. R14 adds termination for the line between the eChook and the driven device. Ideally this is tuned to the specific harness and load.

The LED indicates PWM state: fully on at 100% duty cycle and dimmer at lower duty cycles. R15 limits LED current.

For connector-level wiring details, see [PWM Output](../connecting-the-echook-to-the-car/pwm-output.md).


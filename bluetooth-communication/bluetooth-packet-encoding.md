# Bluetooth Packet Encoding

This is the c code used to construct the packets on the Arduino:

```text
/** ================================== */
/** BLUETOOTH DATA PACKETING FUNCTIONS */
/** ================================== */
/** The two functions in this section handle packeting the data and sending it over USART to the bluetooth module. The two functions are
 *  identically named so are called the in the same way, however the first is run if the value passed to it is a float and the second is
 *  run if the value passed into it is an integer (an override function). For all intents and purposes you can ignore this and simply call
 *  'sendData(identifier, value);' using one of the defined identifiers and either a float or integer value to send informaion over BT.
 *
 * identifier:  see definitions at start of code
 * value:       the value to send (typically some caluclated value from a sensor)
*/

void sendData(char identifier, float value)
{
  if (!DEBUG_MODE) // Only runs if debug mode is LOW (0)
  {
    byte dataByte1;
    byte dataByte2;

    if (value == 0)
    {
      // It is impossible to send null bytes over Serial connection
      // so instead we define zero as 0xFF or 11111111 i.e. 255
      dataByte1 = 0xFF;
      dataByte2 = 0xFF;

    }
    else if (value <= 127)
    {
      // Values under 128 are sent as a float
      // i.e. value = dataByte1 + dataByte2 / 100
      int integer;
      int decimal;
      float tempDecimal;

      integer = (int) value;
      tempDecimal = (value - (float) integer) * 100;
      decimal = (int) tempDecimal;

      dataByte1 = (byte) integer;
      dataByte2 = (byte) decimal;

      if (decimal == 0)
      {
        dataByte2 = 0xFF;
      }

      if (integer == 0)
      {
        dataByte1 = 0xFF;
      }

    }
    else
    {
      // Values above 127 are sent as integer
      // i.e. value = dataByte1 * 100 + dataByte2
      int tens;
      int hundreds;

      hundreds = (int)(value / 100);
      tens = value - hundreds * 100;

      dataByte1 = (byte)hundreds;
      //dataByte1 = dataByte1 || 0x10000000; //flag for integer send value
      dataByte1 += 128;
      dataByte2 = (byte) tens;

      if (tens == 0)
      {
        dataByte2 = 0xFF;
      }

      if (hundreds == 0)
      {
        dataByte1 = 0xFF;
      }
    }

    // Send the data in the format { [id] [1] [2] }
    Serial.write(123);
    Serial.write(identifier);
    Serial.write(dataByte1);
    Serial.write(dataByte2);
    Serial.write(125);

  }

}

/** override for integer values*/
void sendData(char identifier, int value)
{
  if (!DEBUG_MODE)
  {
    byte dataByte1;
    byte dataByte2;

    if (value == 0)
    {
      dataByte1 = 0xFF;
      dataByte2 = 0xFF;

    }
    else if (value <= 127)
    {

      dataByte1 = (byte)value;
      dataByte2 = 0xFF; //we know there's no decimal component as an int was passed in
    }
    else
    {
      int tens;
      int hundreds;

      hundreds = (int)(value / 100);
      tens = value - hundreds * 100;

      dataByte1 = (byte)hundreds;
      dataByte1 += 128;   //sets MSB High to indicate Integer value
      dataByte2 = (byte) tens;

      if (tens == 0)
      {
        dataByte2 = 0xFF;
      }

      if (hundreds == 0)
      {
        dataByte1 = 0xFF;
      }
    }

    Serial.write(123);
    Serial.write(identifier);
    Serial.write(dataByte1);
    Serial.write(dataByte2);
    Serial.write(125);
  }

}
```

If you adapt it to any other languages we would be keen to show the code here!


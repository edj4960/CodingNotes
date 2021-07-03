# Pins

## PinMode

Tells your board how a particular pin is going to be used. The options are:

1. `OUTPUT` - Pin causes something to occur (turning a light on).
2. `INPUT` - Pin reads info (battery level).
3. `INPUT_PULLUP`

```C++
pinMode(1, OUTPUT);
```

## DigitalWrite

Sets the value of a pin set to `OUTPUT` mode.

```C++
void setup() {
  pinMode(13, OUTPUT);    // sets the digital pin 13 as output
}

void loop() {
  digitalWrite(13, HIGH); // sets the digital pin 13 on
  delay(1000);            // waits for a second
  digitalWrite(13, LOW);  // sets the digital pin 13 off
  delay(1000);            // waits for a second
}
```

# Blynk

## Summary

Blynk is an IoT platform for streamlining IoT development. It gives tools to easily connect and control devices.

## Core Concepts

### Virtual Pins

Represent a data point saved on the Blynk servers. Virtual pins can either be set to read data or to cause changes in a device.

## Functions

### BLYNK_WRITE

Function that executes when the specified virtual pin changes

```C++
void setup() {
  pinMode(2, OUTPUT); // Initialise digital pin 2 as an output pin
}

// Executes when the value of virtual pin 0 changes
BLYNK_WRITE(V0) {
  if(param.asInt() == 1) {
    // execute this code if the switch widget is now ON
    digitalWrite(2,HIGH);  // Set digital pin 2 HIGH
  } else {
    // execute this code if the switch widget is now OFF
    digitalWrite(2,LOW);  // Set digital pin 2 LOW    
  }
}
```

## BLYNK_CONNECTED

Function that runs everytime the device connects to the Blynk server. This can be used for ensuring the device and Blynk are synced.

```C++
BLYNK_CONNECTED() {
    // Will cause the BLYNK_WRITE(V0) to be executed
    Blynk.syncVirtual(V0);
}
```

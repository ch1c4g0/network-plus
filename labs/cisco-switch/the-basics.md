

# Requirements

To connect to my 2960-G I am using a USB-Console cable and PuTTY as a terminal emulator. 

## Connecting with PuTTY

To connect you need to identify the COM port your device is using. **COM** short for **Communication** port is an interface that uses a serial medium (one bit at a time) to communicate with another device.

How you identify your COM port depends on your operating system. I am using Windows so I will open "Device Manager" and find "Ports(COM&PLT)" and note what COM port my USB-Console cable is on.

Now, I will change the connection type to "Serial" and enter my COM port "COM4" and click enter.

Hit enter a few times and you should see:

```bash
switch>
```

### Serial Communication

- One bit at a time on the transmission medium
- Commonly found w/ CNC Machines, Programmable Logic Controllers (PLCs), and lab equipment.
- Transmitter(TX) pin to send data | Receiver(RX) pin to get data.
- TX and RX must match speed, this is known as **Baud Rate**.
- TX and RX must agree on start and stop bits.
- TX and RX must agree on **parity**

Parity is an error-checking method that adds an extra bit to data chunks to check for corruption. Even, Odd, or None can be selected here.

## Initial Configurations

### Privilege Modes

First we need to change privilege modes. Upon initial connection to a Cisco switch you will be in "User EXEC Mode" with limited functionality.

To complete any form of changes we need to enter "Privileged EXEC Mode" we can do this with "enable"

```bash
switch> enable
```

Our prompt will know change alerting us we are in privileged mode.

```bash
switch#
```

#### User EXEC Mode 
This is Level 1 access and can be used for reading and basic testing commands. 

#### Privileges EXEC Mode 
This is Level 15 "Full-Access Mode". You will use this mode for Configuration, Troubleshooting, and Management of your switch.


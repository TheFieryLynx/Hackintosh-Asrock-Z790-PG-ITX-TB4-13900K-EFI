# Hackintosh Build

![system info](./assets/main.png)

## System info

| Component   |      Model      |
|----------|-------------|
| CPU   | 13th Gen Intel Core i9-13900K |
| Motherboard |    Asrock Z790 PG-ITX/TB4   |
| Ethernet | Intel Killer E3100X (aka I225-K2)|
| Wifi + Bluetooth | Intel AX211 |
| RAM | 2 x 32GB DDR5 Kingston Fury Beast KF556C40BB|
| GPU | Saphire RX6600 XT 8GB |
| Audio | ALC4082 |
| NVMe | WD Black SN850X 2Tb WDS200T2X0E |

**OpenCore version**: 1.0.0\
**MacOs Version**: Sonoma 14.5 (23F79)\
**SystemProductName**: MacPro7,1

### Note: 
I'm not a professional Hackintosh builder; this is only my second build ever. So, I might have missed something, although I tried to understand every step. Therefore, if you have a similar build and managed to make something work that doesn't for me (described below), please share it through an issue in this repository - **I would be very grateful**.

## What doesn't work::
- **Ethernet**. Strangely, I couldn't get it to work. The chip family should be supported almost natively, but for some reason, this K2 version doesn't work. 

## Partially not working:
- **Bluetooth** - Initially, it didn't work at all. After installing three kexts (IntelBTPatcher.kext, IntelBluetoothFirmware.kext, BlueToolFixup.kext), Bluetooth started detecting all devices but couldn't connect to them. After *logging* into my Apple ID account, I was able to connect AirPods smoothly, but non-Apple devices don't connect, although they are detected. (This problem is encountered on the internet and in forums - I didn't understand how to solve it - recommendations didn't work out)

- **Sound via DisplayPort** (*works via HDMI*) (I haven't tested direct connection of headphones/microphones - I might update it in future)

## Instruction
All serial numbers in macOS must be unique, so I erased mine from the config.plist. 

To generate them, use a script [(GenSMBIOS)](https://github.com/corpnewt/GenSMBIOS) that will automatically create and write them into your configuration file.
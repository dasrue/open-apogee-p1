# Master To Slave Packet Format
| Sequence | Sample Byte | Meaning | Determined by |
|----------|-------------|-----------------------------------------|----------------------------------------------------------------|
| 1 | 0x16 | Unsure, possibly frame start |  |
| 2 | 0x04 | Number of bytes following | Testing different packets |
| 3 | 0x01 | Controller Address (AKA "Drop" Address) | Building a number of different points on different controllers |
| 4 | 0x80 | Command | Using FLN Linetest feature of PXC |
| 5 |  | Data 0..n | Using FLN Linetest feature of PXC |
| 6 | 0x45 | CRC16 Low Byte | Testing sequences in online CRC calculators |
| 8 | 0xB9 | CRC16 High Byte |  |
# Command List
| Command Byte | Command/Info |
|--------------|--------------------------------------------------------------------------|
| 0x80 | Ping Controller? (Sent when point is built and no controller responding) |
|  |  |
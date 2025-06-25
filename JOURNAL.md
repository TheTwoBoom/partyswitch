---
title: "PartySwitch"
author: "TheTwoBoom"
description: "Ethernet Switch with USB-C instead of RJ-45 ports"
created_at: "2025-06-19"
---

# June 20th: Wrote 1st revision of BOM (excluding power)

I first looked for a fitting switch chip that supported 2.5Gbit and was in stock.  
After looking for a little bit I found this one
![switch-chip](https://github.com/user-attachments/assets/ada3f5be-8ac4-447d-b369-e6494a72d15c)

Following that, I read the datasheet and I discovered that 2 transceivers were needed for 2.5gbit
![transceivers](https://github.com/user-attachments/assets/21c77b5d-c138-41db-94bc-030f508d163e)

Because I want to keep some compatability with existing ethernet devices, I added 4 RJ-45 ports (two 2.5gbit ports, two 1gbit ports)
![ethernet-connectors](https://github.com/user-attachments/assets/d8d368e1-82cf-49a1-880f-8474144363e4)

Some ethernet specs said I need to use magnetics so I also added them to the BOM (1 per RJ-45 Port, 4 total)
![magnetics](https://github.com/user-attachments/assets/86499d5c-ed67-4e26-b07b-2c35f4e197eb)

To connect the USB-Devices I added 3 USB-C Ports and USB to Ethernet Converters
![usb-port](https://github.com/user-attachments/assets/93403097-43bd-4d1d-ba3c-262236324b09)
![usb-to-ethernet](https://github.com/user-attachments/assets/5ea9fec6-aaef-4c3f-b540-4fcea4bfa964)

![grafik](https://github.com/user-attachments/assets/0b0e2714-b582-44f4-bf44-56ba4645fa4c)
![grafik](https://github.com/user-attachments/assets/4cb43028-932f-4c24-a5ec-dbd0e04e944a)


**Total time spent: 4h**

# June 22th: Wrote 1st revision of BOM (power management)

I discovered that the USB-C Connectors I previously chose were kind of weird, so I chose this one instead
![usb-port](https://github.com/user-attachments/assets/675f4ecf-fb14-4066-9231-04981d3cc018)

Because most components needed 3.3V, I added a buck converter to convert 5V to 3.3V
![buck-converter](https://github.com/user-attachments/assets/75f1b1a1-1452-4f11-9ea2-68c934edbdbf)

To protect my design from power surges, I "copied" the methods from this jam for a USB-Hub and added some methods from ChatGPT:
https://jams.hackclub.com/batch/usb-hub/part-1
![schottky-diodes](https://github.com/user-attachments/assets/509b0395-f654-4b7b-800e-1d2f40fdd11d)
![1nF (2kV) Capacitors](https://github.com/user-attachments/assets/084b014e-c619-43e8-ba0b-23fdacf3d1ae)
![100nF Capacitors](https://github.com/user-attachments/assets/1fdbca7d-6ae8-4c22-b071-6aa572e41520)
![1uF Capacitors](https://github.com/user-attachments/assets/27f498fb-cdcb-4162-8dd7-34512a45f758)
![10uF Capacitors](https://github.com/user-attachments/assets/7bc1a24b-63b2-4b27-963c-2b4e49479863)
![1MΩ Resistors](https://github.com/user-attachments/assets/558dc875-2cc7-4d4b-9351-10bd8a96f93d)

I also added an 5.1kΩ Resistor to trigger 5V power via USB-C
![5.1kΩ Resistor](https://github.com/user-attachments/assets/0501d8ba-e0fa-4e3a-b332-01296476f82c)

**Total time spent: 2h**



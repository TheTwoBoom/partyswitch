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

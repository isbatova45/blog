---
title: Parallel and Serial Ports
summary: Features of using computer ports - connection points between a computer and peripheral devices
tags:
  - Deep Learning
date: '2023-05-05T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart


url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

To communicate with peripheral devices, one or more I/O controller chips are connected to the computer bus. The main function of a port is to act as a connection point where a cable is connected from a peripheral device and to allow data to be transferred from one device to another. Usually, it is the very end of the connector located on the motherboard that is called the port. Any computer must have a minimum set of ports, without which operation is impossible - these are ports for connecting a monitor, mouse, keyboard, a network connection connector, a universal USB port and an audio connector for a sound card. If necessary, the number of computer ports can be increased using expansion boards connected to the main board.

Ports can be divided into two types - serial and parallel. They are divided depending on the type used for communication.

Serial ports (also called COM port) are ports through which peripheral devices are connected using a serial protocol. In other words, information is transmitted through them one bit at a time, bit by bit. The name "serial port" is assigned to a port that has the RS-232C standard, so although other interfaces (such as USB) also use a serial method of exchange, they are not classified as serial ports. Serial connectors typically have 9 to 25 pins, and a personal computer typically has one to four serial ports. Serial ports are usually built into the motherboard.

A feature of serial ports compared to other "serial" technologies (such as USB or Ethernet) is the presence of time requirements only between bits of one byte (baud rate is the time gap between them). There are no timing requirements between the 2 bytes.

Initially, the serial port was used to connect the terminal, later it was used for the modem and mouse. Serial ports are now rarely used, as they are unsuitable for entertainment and office purposes. However, they are indispensable for applications, so they are mainly used to connect to uninterruptible power supplies, to communicate with hardware for the development of embedded computing systems, satellite receivers, as well as with devices for security systems of objects.

Parallel ports are ports through which communication between a computer and its peripheral device is carried out in parallel. That is, data transmission is carried out simultaneously over several communication lines or wires. Sometimes a parallel port is called a printer or Centronics port. Parallel ports are often identified in a computer system as "LPT1" and "LPT2" and, like serial ports, are built into the motherboard.

On personal computers, parallel ports can be used to send 8 bits simultaneously over 8 wires. Parallel ports allow you to match the low speed of an external device and the high speed of the microprocessor's system bus.

Before the advent of USB, the parallel port was adapted to a large number of peripherals. The first such device was dongles used to protect software from copying. Soon it began to be used with other devices - magnetic disks, scanners, modems, sound cards, and so on.

The first bidirectional ports had a speed of 2.4 Mb / s. However, in order to achieve higher speeds, advanced parallel ports have been developed: ERP (Advanced Parallel Port) and EDP (Enhanced Port). RPP reaches speeds from 8 to 16 Mb / s. PRV has the same characteristics as RPP, but with the additional possibility of automatic configuration (allows the computer to recognize connected peripherals).

USB has now replaced the printer's parallel port. Many PC and laptop manufacturers regard the parallel port as a legacy from the past and no longer support the parallel port. For example, USB to Parallel adapters have been developed and available for printers that allow you to connect printers with a parallel interface to USB ports.

# RPiHTPC
## Instructions for building out a Raspberry Pi based Home Theater PC
I've done this several times now, and eventually the wheels fall off, necessitating another build. Rather than continuously starting from square one and researching what to do from scratch, I'm putting this instructional together in the hopes of saving some time on my subsequent rebuilds. 

### Requirements
The description in the brackets is my build
* A Raspberry Pi computer [Raspberry Pi 2 Model B]
* A micro SD card with at least an 8 GB capacity [SanDisk 8 GB MicroSD with PiHut SD adapter]
* A functioning computer with an SD or micro SD card reader [Lenovo ThinkPad T500 running Lubuntu 20.04]

### Step by Step Installation
1. Install Raspberry Pi OS (formerly Raspbian) to your SD card using the image writer of your choice. For simplicity's sake, I used the official Raspberry Pi Imager (v 1.4) to install the [Raspberry Pi OS with Desktop image](https://downloads.raspberrypi.org/raspios_armhf/images/raspios_armhf-2020-08-24/2020-08-20-raspios-buster-armhf.zip).

2. Mount the SD card on your computer and navigate to the `boot` directory of the SD card. Once you're there, create a new, blank file with no extensions called `ssh`. By creating this file before inserting the SD card into the Raspberry Pi, we enable SSH connections to the new machine, enabling it to run in headless mode. 

2. Insert the SD card into the Raspberry Pi, boot it up, and connect the device to the internet. 

3. Establish an ssh connection to the headless Raspberry Pi from your computer (or navigate to the terminal on the Raspberry Pi if you are running it with peripherals). For ssh users, the connection can be opened with the command `ssh pi@XXX.XXX.XX.XX` where `XXX.XXX.XX.XX` is the IP address of your Pi. When prompted, enter the default password, which is `raspberry`. 

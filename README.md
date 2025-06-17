# Horizon Avionics

## Building a fully open-source flight computer.

### Hardware By @Scooter Y, and @Meddy B.
### Software By: @Stars, and @YourLocalDndNerd

------

#### About:

The Goal of Horizon Avionics is to be able to build a full-fledged, and open-source flight computer for amateur rocketry. There is no such board online, and we are hoping for this board to streamline open-sourcing products instead of charging upwards of $400 for a ~$130 board.



#### Features:

- This whole board including antennas are under $150 USD.

- IMU/Baro for our sensor data.

- GPS for navigation of where the rocket landed and it's flight path.

- RF - Including a transmit tower for receiving/sending data from the rocket live during the flight.

- NAND + Micro SD Card Storage for logging.

- 3 MCU's each controlling different ascpetcs of the flight computer- MMCU, TMCU, NMCU.

- H-Bridge for servo movement.

- Working PWM for TVC and/or Reaction Wheel

- Pyro-channels for parachute deployment

  ------

#### How it's all gonna work:

For the most part, this will all be explained over on the software repo, but a short synopsis will be provided below.

In short, we have 3 micro-controllers, the MMCU, the TMCU, and the NMCU. Each one of these MCU's is responsible for a different aspect of the functionality of the flight computer.  

- **The TMCU**

​	The TMCU is responsible for a number of different things. It takes in all the raw data from the IMU, Baro and the GPS data and sending it to the MMCU via SPI for filtering and logging. It is also resposible for sending and receiving the radio packets. In-short, the TMCU does a lot of different things for this board to make room for the MMCU to do the heavy lifting.

- **The NMCU**

  The NMCU is responsible for more of the physical actions of the rocket. It's main jobs are to on boot, load the saved state, for position movements, and while in-flight, it's jobs are to take in the filtered data from the MMCU, and use it to control the Camera, servo lines, reaction wheel, and pyro-channels.

- **The MMCU**

  The MMCU is our main MCU. It's main responsibilities are to, while in flight, take in all the data from the TMCU, put it through a filter (we will be using the Kalman Filter for our board as it is the best one we have found to remove noise and such), package the data, and send it back off to the TMCU for radio sending or to the NMCU for movments. Along with sending it to the nessecary MCU's, it also sends the packaged, and filtered data to the NAND which will eventually be moved to the SD Card + the Camera footage upon landing.

------

#### Getting Started

To view the different changes between commits, check it out over on [CADLAB.io](https://cadlab.io/project/29344).

##### Checkout locally

1. `git clone https://github.com/Horizon-Avionics/Horizon-Avionics-Hardware`

2. Open the corresponding folder in KiCad 9.0


### Some Photos So Far

![image](https://github.com/user-attachments/assets/4f798576-2a2a-40cc-96e8-24cf39a89057)
![image](https://github.com/user-attachments/assets/c83f1a7a-d0c4-47c1-934c-d2f711475afa)
![image](https://github.com/user-attachments/assets/bed94868-f991-4d4c-bf15-8acd95b8b909)
![image](https://github.com/user-attachments/assets/17ecafb4-b945-414b-a132-3ecccd010a7f)
![image](https://github.com/user-attachments/assets/4cf7e7c3-a743-48ac-b4f1-7bfc19de2636)



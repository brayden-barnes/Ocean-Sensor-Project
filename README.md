# Ocean-Sensor-Project

This was the final project of Dalhousie University's ECED4402, Real Time Operating Systems. Please see Ocean-Sensor-Project/Project_Description.pdf for the nitty gritty details on the project objective.

Our goal was to simulate 2 underwater sensors exhanging and processing data in real time using FreeRTOS and 2 stm32f411RE microcontrollers. By sending commands (custome protocol that we made) to one STM32F411E from a host PC, we simulated the microcontroller receiving real time data from various sensors (ex. temperature sensor, hydrophone, whatever we choose...) based on the specific command received. One microcontroller received this data, compressed it, and sent it to a second microcontroller. The receiving microcontroller would add all data to a queue and reconstruct it based on priority before sending it as text to the destination host PC.

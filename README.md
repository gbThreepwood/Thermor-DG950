# Thermor-DG950
Reception of wireless sensors from Thermor DG950 Weather Station

Reverse engineering and reception software for the Thermor DG950 Wireless Home Weather Station. The station consists of a outside wind speed, wind direction, rainfall and temperature sensor. All outside sensors are connected to a wireless transission unit. The transmission frequency is stated as 433.92 MHz, in my experience there may be some drift however.

A set id button is available on the transmission unit, the purpose is to transmit a ID to the inside receive unit. When activated the ID is transmitted continuously.

When operating in normal mode, the transmission unit is transmitting the measured data every 128 seconds. The manufacturer states a maximum transmission range of 60 meters.

FCC test reports are available at: https://fccid.io/S24DG950R

## Reverse engineering

A rtl-sdr (http://www.rtl-sdr.com/) and a HackRF (https://greatscottgadgets.com/hackrf/) is used for reception of the signals. GNU radio and Gqrx is used as reception software, and Audacity is used to analyze the recorded wave files.

The captured audio is available in the raw-data folder.


## Reception system

The system is using the popular rlt-sdr as a receiver, and a GNU Radio based Python script as decoder.


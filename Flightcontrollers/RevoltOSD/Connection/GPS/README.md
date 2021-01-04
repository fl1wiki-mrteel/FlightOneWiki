# RevoltOSD - GPS Connection

Each GPS is different and may require 3.3v or 5v for power, please check your specific GPS before connecting! The required GPS format is glonass, which is sold by may popular vendors such as TBS. The UART protocol requires connecting the crossover cables in this way:

- RX from GPS to TX from flight controller
- TX from GPS to RX from flight controller

You must connect the GPS to UART 4 ​​of the flight controller, therefore Tx4 and Rx4. You will notice that the pad Tx4 is a pad easy to access, the pad Rx4 is very small and in the middle of the flight card … Be careful with this one, if you heat it too long with your soldering iron, you may destroy it.


Once the GPS connected, remember to solder a jumper between Tx4 and NOR to put the UART 4 ​​in normal.

![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/RevoltOSD_GPS.png)


## External links

- [Flightone - Connecting a GPS (Legacy)](https://support.flightone.com/index.php/knowledge-base/connecting-a-gps/)
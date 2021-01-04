# Lightning H7 - GPS Connection


Each GPS is different and may require 3.3v or 5v for power, please check your specific GPS before connecting! The required GPS format is glonass, which is sold by may popular vendors such as TBS. The UART protocol requires connecting the crossover cables in this way:

- RX from GPS to TX from flight controller
- TX from GPS to RX from flight controller

 
Unlike the RevoltOSD and MillivoltOSD the Lightning H7 does NOT require any specific UART for GPS. 
<b>BUT as of now you should use UART 3.</b>



## External links

- [Flightone - Connecting a GPS (Lightning H7)](https://support.flightone.com/index.php/knowledge-base/connect-a-gps-to-the-h7/)
- [Flightone - Connecting a GPS (Legacy)](https://support.flightone.com/index.php/knowledge-base/connecting-a-gps/)
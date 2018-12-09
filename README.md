First of all I want to thank OE1ACM Bernd for his approval to use his code for my experiments.
He is the author of BG_RF95!

All user settings can be found in TTGO_T-Beam_LoRa_APRS.h

If you start the FW for teh first time you are asked to program your callsign and SSID(s).<br>
Once the callsign is programmed you can reenter the programming mode by pressing the BUTTON (39) for 3secs while switching on the racker.<br>

<b>"sTable"</b> should contain the value for the primary or secondary symbol table<br>
<b>"sSymbol"</b> contains finally the symbol to be sent with the position report

<b>"wxTable"</b> should contain the value for the primary or secondary symbol table used for weather reports<br>
<b>"wxSymbol"</b> contains finally the symbol to be sent with the weather report

<b>"nextTX"</b> is the transmit intervall in ms (milli seconds) - don't use to short intervalls as it overloads the APRS servers<br>
60000L is a could starting point and means a intervall of 60secs or 1 minute.

The MODE of the tracker can now be changed by pressing button at <b>GPIO39 for 10secs</b>!<br>
<b>The modes are</b><br>
TRACKER ...     normal APRS tracker<br>
WX&TRACKER ...  alternate transmission of normal position packet and WX packet (if DHT22 is mounted)<br>
WX-MOVE ...     only WX packets are sent but with position from GPSLED<br>
WX-FIXED ...    only WX packets are transmitted but with fixed position given in Header-File<br>

the following lines are used to define the fixed position<br>
<b>#define LATITUDE "4813.62N"</b>  // please in APRS notation DDMM.mmN or DDMM.mmS used for FIXED_POSITION<br>
<b>#define LONGITUDE "01539.85E"</b>

for DHT22 I used the library from https://github.com/beegee-tokyo/DHTesp, as the standard library gives to many wrong readings

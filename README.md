# 12vdc-extension
Description of a 50m 12v DC power extension

The aim is to produce a waterproof 12v DC power source using a 50m long 1mm<sup>2</sup> area cable. The problem is that the resistance would cause significant voltage drop over this length (100m round journey) but this will depend on the current being drawn. The strategy here is to start with a 24V source and then use a buck/boost regulator to get a 12V supply at the end of 50m of cable irrespective of the voltage drop. The regulator (along with a amp/volt meter to monitor power usage) are housed in a waterproof enclosure with at 12V 'cigarette lighter' socket.

|Item|Cost|
|---|---|
|Automotive Twin Core Cable (16.5 AMP Rated 1mm² 18 AWG) 10/30/50/100 Metre (50M Roll)|£34.95 for 50m|
|DC Voltage Reducer Automatic Buck Boost Converter DC 8V-40V to 12V 6A 72W | £23.99 |
|DC Power Analyzer High Precision Watt Volt Amp Energy Meter Analyzer Tool (0-100A 0-60V)|£10.99|
|Junction Box Universal Project Enclosure, ABS Waterproof IP65 Electrical Box Hinged Shell w PC Transparent Cover with Lock 150 x 100 x 70 mm|£12.99|
|Waterproof Cigarette Lighter Outlet Universal 12V/24V DC |£9.99|
|M12 Cable Gland Waterproof|£5.99 for 20|
|24v DC power supply||

### Predicted voltage drop
V<sub>drop</sub> = 2·I·R·L
- I: the current through the wire
- R: the length-specific resistance of the wires
- L: the one-way length

Cable area: 1.0 mm<sup>2</sup>
Copper resistance: 16.61 Ω/km

1A current (2A at 12V)
V<sub>drop</sub> = 2 x 1.0 x 16.61 x 0.050 = 1.66V

3A current (6A at 12V)
V<sub>drop</sub> = 2 x 3.0 x 16.61 x 0.050 = 4.98V

### Measurements
Input voltage 23.9V

Equipment attached:
ZWO AM5 mount
ZWO ASIAIR Plus computer
ZWO ASI533MC Pro camera (cooling on)
ZWO ASI174MM mini camera
Refractor objective dew heater

| activity | current 1 | voltage 1 | V<sub>drop</sub> 1 | power 1 | current 2 | voltage 2 | power 2 |
|---|---|---|---|---|---|---|---|
|Stationary | 1.08A | 21.8V	| 2.1V | 23.5W | 2.0A | 11.7V | 23.3W |
|Tracking | 1.19A | 21.6V |	2.3V | 25.6W | 2.2A | 11.7V | 25.3W |
|Slewing | 1.28A | 21.3V | 2.6V | 27.2W | 2.2A | 11.6V | 25.9W |
1. Measured at the end of the cable by the power meter
2. Measured by the ZWO ASIAIR Plus

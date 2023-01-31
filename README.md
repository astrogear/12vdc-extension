# 12vdc-extension
Description of a 50m 12v DC power extension

The aim is to produce a waterproof 12v DC power source using a 50m long 1mm<sup>2</sup> area cable. The problem is that the resistance would cause significant voltage drop over this length (100m round journey) but this will depend on the current being drawn. 

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

The strategy here is to start with a 24V source and then use a buck/boost regulator to get a 12V supply at the end of 50m of cable irrespective of the voltage drop. The regulator (along with a amp/volt meter to monitor power usage) are housed in a waterproof enclosure with at 12V 'cigarette lighter' socket.

|Item|Cost|
|---|---|
|Automotive Twin Core Cable (16.5 AMP Rated 1mm² 18 AWG) 10/30/50/100 Metre (50M Roll)|£34.95 for 50m|
|DC Voltage Reducer Automatic Buck Boost Converter DC 8V-40V to 12V 6A 72W | £23.99 |
|DC Power Analyzer High Precision Watt Volt Amp Energy Meter Analyzer Tool (0-100A 0-60V)|£10.99|
|Junction Box Universal Project Enclosure, ABS Waterproof IP65 Electrical Box Hinged Shell w PC Transparent Cover with Lock 150 x 100 x 70 mm|£12.99|
|Waterproof Cigarette Lighter Outlet Universal 12V/24V DC |£9.99|
|M12 Cable Gland Waterproof|£5.99 for 20|
|24v DC power supply||

Setting a 24v power supply:
![IMG_4894](https://user-images.githubusercontent.com/686405/215772963-129688d6-0c6c-404b-b7d6-26a342f68e64.jpeg)

After 50m of cable, drawing close to one Amp, the voltage had dropped to 22V (close to the theoretical calculation above). The meter is on the supply side of the DC converter so the gear will be drawing ~2As at 12Vs.
![IMG_4895](https://user-images.githubusercontent.com/686405/215773089-488023bb-84c6-40b1-8b2d-7fe134f2a6e1.jpeg)

### Measurements
I did a few measurements with my actual equipment using different power. The measurements were taken using the amp/volt meter before the converter and in the ZWO ASIAIRs internal meters (not sure how accurate these are).

Input voltage 23.9V

Equipment attached:
- ZWO AM5 mount
- ZWO ASIAIR Plus computer
- ZWO ASI533MC Pro camera (cooling on)
- ZWO ASI174MM mini camera
- Refractor objective dew heater

ZWO quotes the AM5 power usage as Standby	0.386A, 4.632W, Tracking 0.58A, 6.96W, Slewing 1.7A, 20.4W 

ZWO ASI2600MC camera power usage: 1.15A at 5V, 5.75W

ZWO ASI2600MC cooler power usage: 12V at 3A Max, 36W

| activity | current<sup>1</sup> | voltage<sup>1</sup> | V<sub>drop</sub><sup>1</sup> | power<sup>1</sup> | current<sup>2</sup> | voltage<sup>2</sup> | power<sup>2</sup> |
|---|---|---|---|---|---|---|---|
|Stationary | 1.08A | 21.8V	| 2.1V | 23.5W | 2.0A | 11.7V | 23.3W |
|Tracking | 1.19A | 21.6V |	2.3V | 25.6W | 2.2A | 11.7V | 25.3W |
|Slewing | 1.28A | 21.3V | 2.6V | 27.2W | 2.2A | 11.6V | 25.9W |

<sup>1</sup> Measured at the end of the cable by the power meter

<sup>2</sup> Measured by the ZWO ASIAIR Plus

### Notes

Reducing the voltage at the supply end would increase the current in the cable which would increase power loss due to heating (by the square of the current). 

| voltage at supply | current | resistance | power heating cable |
|---|---|---|---|
|24v | 1.5A | 1.66ohm	| 3.74W |
|12v | 3A | 1.66ohm | 14W |
|8v | 4.5A | 1.66ohm | 33.6W |

Difference in power between meter and the ASIAIR due to loss in regulator?

Slewing measurement seems low - the mount documentation suggests it should draw more power. This may be an issue with the measurement by the ASIAIR averaging?



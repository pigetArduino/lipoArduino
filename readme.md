How to use lipo batteries with Arduino
---------------------------------------
[Version française](https://github.com/pigetArduino/lipoArduino/blob/master/readme.fr.md)

![Lipo batteries and arduino mini pro 3v Photo](https://github.com/pigetArduino/lipoArduino/raw/master/doc/lipo_arduino_photo.jpg)

Datasheet : https://dlnmh9ip6v2uc.cloudfront.net/datasheets/Prototyping/TP4056.pdf

![Warning sign](https://github.com/pigetArduino/lipoArduino/raw/master/doc/warning.png) 

**This is just my research ONLY based on experimentation, this will void the warranties on the batteries**     
**tp4056 can only charge 1C battery  and only one**      
* Voltage:3.7v    
* Capacity: 260mah    
* Discharge : 35 (constant) - 70 (burst)   
* Constant maximum discharge (0.260A * 35) = 9,1A
* Burst maximum discharge (0.260A * 70) = 18.2A

# Components
* Arduino mini pro 3v
* TP4056 Battery charger
* Turningy 3.7 nano tech 260 mah Battery

# Wiring
* You need to cut the cable of the batteries to solder it to the tp4056 charger. Do it with caution!
* You need to replace the rprog resistor on tp4056 with 5kOhm resistor
 
![Lipo batteries and arduino mini pro 3v Wiring](https://github.com/pigetArduino/lipoArduino/raw/master/doc/lipo_arduino_wiring.png)

# Charge test.
Estimation : 1h00 on 250ma     
260mah/250    

# How to get Ibat (Charging ma)
Ibat = VPROG/RPROG * 1200 (VPROG=1V)     
Ibat = 1/5 * 1200 = 240ma        
Ibat = 1/1.6 * 1200 = 750ma       


Source:    
* What's in a "C" Rating : https://www.commonsenserc.com/page.php?page=c_ratings_explained.html   
* https://dlnmh9ip6v2uc.cloudfront.net/datasheets/Prototyping/TP4056.pdf
* http://electronics.stackexchange.com/questions/152931/how-to-autoregulate-a-tp4056-for-maximum-solar-power-extraction
* http://www.electrodragon.com/w/Battery_Charge

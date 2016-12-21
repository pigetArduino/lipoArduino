Comment utiliser une batteries lipo avec un Arduino
---------------------------------------

**Attention: Je ne suis pas un expert en batteries, ceci n'est que mes recherches basés uniquement sur l'expérimentation**

**Le tp4056 ne peut recharger que des batteries de 1C et une seul batterie à la fois**

* Tension:3.7v    
* Capacité: 260mah    
* Décharge : 35 (constante) - 70 (en burstp)   
* Décharge constante maximal : (0.260A * 35) = 9,1A
* Décharge par àc-oup maximal : (0.260A * 70) = 18.2A

# Composants
* Arduino mini pro 3v
* TP4056 Battery charger
* Turningy 3.7 nano tech 260 mah Battery

# Branchement
* Vous devez coupé le cable de la batterie pour la souder au chargeur tp4056. Faites attention!
* Vous devez remplacer la résistance RPROG du tp4056 par une résistance de 5kOhm (pour cette capacité de batterie)
 
![Lipo batteries et arduino mini pro 3v](https://github.com/pigetArduino/lipoArduino/raw/master/doc/lipo_arduino_wiring.png)

# Test de charge.
Estimation : 1h00 on 250ma   
260mah/250    

# Test de décharge
* Croquis utilisé: Blink
Estimation : 2h30 (100ma / 260 --> 2.6h)

Sources (en anglais):    
* What's in a "C" Rating : https://www.commonsenserc.com/page.php?page=c_ratings_explained.html   
* https://dlnmh9ip6v2uc.cloudfront.net/datasheets/Prototyping/TP4056.pdf
* http://electronics.stackexchange.com/questions/152931/how-to-autoregulate-a-tp4056-for-maximum-solar-power-extraction
* http://www.electrodragon.com/w/Battery_Charge

# 4 Smart-Home Ideen

## Vorabinformationen: 
Die hier aufgeführten Ideen sind als Inspiration zu verstehen. \
Für Verbesserungen bin ich immer offen und dankbar :smiley:

## Vorraussetzungen

### Hardware 
* Open-Hab  [Link](https://www.openhab.org/) zum Beispiel auf Raspberry PI
* ESP8266/ESP32 

### Umgebung
* WLAN (2.4GHz) muss am jeweiligen Standort verfügbar sein

## Smarte Überwachung von Waschmaschine/ Trockner

### Idee: 
Steht die Waschmaschine/ Trockner beispielsweise im Keller und ist somit nicht im Sichtfeld, ist man sich als Nutzer nicht sicher, wann der Wasch-Trockenvorgang beendet ist. \
Praktisch wäre es, wenn man via Smartphone benachrichtigt werden würde. Allerdings bieten in die Jahre gekommene Geräte eine solche Funktionalität nicht. 
Mit Hilfe eines ESP8266 werden diese Benachrichtigungen nun nachgerüstet. \
Während des Wäschvorgang entstehen bei einer Waschmaschine/ Trockener Erschütterungen, welche über einen Shocksensor gemessen werden. \
Es wird ein Algorithmus entworfen, welche in regelmäßigen Abständen prüft, ob weiterhin Erschütterungen auftreten.  \
Werden Vibrationen gemessen, so prüft der ESP8266 nach 10 Minuten erneut auf Vibrationen.
Dies wird solange wiederholt, bis keine Erschütterungen messbar sind (= die Waschmaschine/Trockner hat ihr Programm beendet).

### Versand: 
Der Versand erfolgt der Benachrichtug erfolgt mit dem [MQTT-Protokoll](https://mqtt.org/). 

### Code: 
* to be uploaded

### Erfahrungen:
* to be uploaded

### Erweiterungen:

* Anbau eines Buttons, der bei Druck die Meldung über eine Beendigung eines Waschprogramms löscht


## Temperaturgesteuerter Ventilator im Sommer:

### Bestandteile:
* Relais mit AC 230V
* Temperatursensor DHT11
* ESP8266 / Arduino

### Idee:
Ventilatoren sind im Sommer echt praktisch :smiley: \
Allerdings kann man bei besonders günstigen Produkten meist nur zwischen AUS/EIN unterscheiden. \
Damit ist man dauerhaft dem nervigen Geräusch des Lüfters ausgesetzt. \
Dieses Problem kann man mit Hilfe des ESP8266 beheben, indem man über ein Relais den Ventilator ein und ausschaltet. Dabei wird die Raumtemperatur über einen Temperatursensor gemessen und mit der SOLL-Temperatur vergliechen. Sobald diese überschritten wird, schaltet sich der Ventilator ein. Ist die Wunschtemperatur erreicht, schaltet sich der Ventilator aus.

### Steuerung

Die Steuerung kann entweder über eine Webschnittstelle oder über den Code auf dem ESP8266 übernommen.\
Es ist möglich, den SOLL-Wert, nachfolgend Wunschtemperatur genannt, im Code selbst festzulegen oder über eine Website, welche auf dem ESP8266 läuft, einzustellen.

### Code
* to be uploaded
### Erweiterungen
* Potentiometer zum einstellen der Wunschtemperatur am Gerät selbst










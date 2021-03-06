# MifareGame
Jeu regroupant plusieurs challenges exploitant les vulnérabilités de certaines cartes sans-contact MIFARE.
Recquiert une carte Arduino et un lecteur MFRC522.

## Installation
Cloner le dossier build dans le dossier MifareGame du GitHub secyourdev.
Lancer l’exécutable main.exe sur Windows ou main sur Linux.

## Configuration
Pour brancher le lecteur MFRC 522, il faut faire correspondre les pin selon la disposition suivante :

|     Signal    | Lecteur MFRC522 |  Arduino Uno  |
| :-----------: | :-----------:   | :-----------: |
| Alimentation  |      +3.3V      |      +3.3V    |
|      GND      |       GND       |       GND     |
|   RST/Reset   |       RST       |        9      |
|     SPI SS    |     SDA (SS)    |       10      |
|    SPI MOSI   |       MOSI      |       11      |
|    SPI MISO   |       MISO      |       12      |
|    SPI SCK    |       SCK       |       13      |

Pensez également à téléverser le programme arduinoMain sur la carte Arduino, disponible dans le dossier arduino/arduinoMain/.

## Compilation depuis les sources (déconseillée)
Pour exécuter directement le projet, il faut installer la librairie Arduino rfid (actuellement en 1.4.6), développée par miguelbalboa.
Le programme Python nécessite d'installer pygame avec :
```
pip install pygame
```

Si vous voulez créer un nouvel exécutable, en fonction de la version de python utilisée :
```
python setup.py build
```

ou
```
python3 setup.py build
```

##Erreurs
Si la carte Arduino ne semble plus répondre, vous pouvez la réinistialiser en appuyant brièvement sur le bouton RESET.

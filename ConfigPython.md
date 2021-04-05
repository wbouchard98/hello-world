![Pyhton](https://github.com/wbouchard98/hello-world/blob/b0a1c2ca098754fc5b32db06101120003069b15e/pyhton.PNG)
# Étapes pour l’installation des librairies Python

1) Premièrement, il faut s’assurer que Pyhton3 soit bien installé : sudo apt-get install python3 .
2) Une fois installé, il faut pouvoir accéder au I/O du Raspberry Pi. La librairie suivante va faire ce travail : sudo pip3 install RPI.GPIO
3) Pour pouvoir lire les données du capteur SEN0227 qui va lire la température de l’environnement dans lequel le Raspberry Pi se situe (et non l’environnement que l’on souhaite contrôler) : sudo pip3 install sht20 .
4) Maintenant, pour être capable de faire les communications MQTT, il nous faut un ‘’Broker MQTT’’ : sudo apt-get install mosquitto : et : sudo apt-get install mosquitto-clients .
5) Une fois le ‘’Broker’’ installé, il nous faut la librairie pour accéder à ce ‘’Broker’’ : sudo pip3 install paho-mqtt .
6) Maintenant, il faut que notre ‘’GUI’’ puisse accéder aux librairies PYQT5 : sudo apt-get install qt5-default pyqt5-dev pyqt5-dev-tools
7) Pour contrôler la plupart des éléments de l’environnement, l’utilisation d’un PID est importante. La librairie suivante va nous permettre d’utiliser des PID : sudo pip3 install simple-pid .

![RPIlogo](https://github.com/wbouchard98/hello-world/blob/1bab890407de53b6081342bc769ee3ec7076baf6/RPILOGO.png) 
# Étapes de l’installation de l’image du Raspberry Pi 

1)	Allez chercher une image de Raspberry Pi Buster Desktop lit
2)	”Flash” une carte SD d’au moins 8Go avec cette image. Nous avons utilisé Balena Etcher pour cette étape.
3)	Faire la configuration du Raspberry Pi lors de son premier démarrage. Lorsqu’il vous est demandé de redémarrer le Raspberry Pi, redémarrer le.
4)	Maintenant, il faut activer les interfaces dont on aura besoin. Ouvrez un terminal, et tapez la commande : sudo raspi-config
5)	Une fois la fenêtre de configuration ouverte sélectionner l’index 5(Interfacing Options).
6)	Activer ’’Camera’’, ‘’SSH’’, ‘’VNC’’, ‘’I2C’’ et ‘’1-Wire’’. Il faut aussi activer le ‘’Serial’’. Cependant lorsqu’il va être demandé s’il est désiré que le ‘’login shell’’ soit accessible depuis le serial, faire non, et lorsque l’usager est demandé de vouloir activer le ‘’Serial port hardware’’ faire oui.
7)	Redémarrez le Raspberry Pi pour effectuer les changements.
8)	Maintenant, il faut se connecter au serveur de temps pour pouvoir automatiquement mettre à jour le temps du Raspberry Pi. Ouvrez le fichier /etc/systemd/timesyncd.conf .
9)	Modifiez les lignes ‘’NTP’’ et ‘’FallbackNTP’’ pour que leur valeur sois : time.apple.com .
10)	Effectuez un : sudo systemctl restart systemd-timesync.service .
11)	Effectuer par la suite : sudo systemctl daemon-reload .
12)	Maintenant faire les ‘’update’’ et ‘’upgrade’’.
13)	Si vous utilisez un écran de petite taille, comme un écran 7" comme nous, nous vous recommandons de changer la résolution de l'écran. Pour ce faire, cliquer le logo Raspberry dans le haut de l'écran, puis aller sur "Preferences" et "Raspberry Pi Configuration". Aller dans l'onglet "Display" et puis "Set Resolution...". Nous utilisons "DMT mode 9 800x600 60Hz 4:3".




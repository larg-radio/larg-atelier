# Installation de CentOS

## Installation de CentOS 7

### Télécharger CentOS 7

[wiki.centos.org/Download](https://wiki.centos.org/Download)

```bash
wget http://centos.crazyfrogs.org/7.7.1908/isos/x86_64/CentOS-7-x86_64-Everything-1908.iso
```

### Copier sur une clef

```bash
sudo dd if=CentOS-7-x86_64-Everything-1908.iso of=/dev/sdX
```

### Boot

Apres insertion de la clef USB, démarer le PC.

* F12 -> boot menu boot USB
* Install CentOS 7
* choisir la langue francais
* Séléction des logiciels
  * Séléctionner Bureau Gnome sur la gauche
  * Séléctionner Application GNOME, Suite de bureautique, Outils de sécurité, Outils d'aministration systéme, puis Terminé
* DESTINATION DE L'INSTALLATION
  * Selectionner votre disque dure

| Pour une installation de Rivendell:
|
| * Installer le second disk sur /var/snd

* Aprés installation rebooter

* Accepter les license
* Changer le nom de l'hote et activer le réseau

* Tester votre/vos cartes son au premier démarage.

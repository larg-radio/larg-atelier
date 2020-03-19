# Installation de Rivendell

Il est important de décrire votre installation.

Elle peut réster telquel pendand plusieurs année.
Si la documentation évolue, la votre doit être a jour de ce que vous avez installé.

## Prérequis

avoir installé CentOS 7

Est une trés bonne source d'information:

[https://rivendellfr.frama.wiki/installation](https://rivendellfr.frama.wiki/installation)

[http://download.paravelsystems.com/CentOS/](http://download.paravelsystems.com/CentOS/)

Pour toutes question sur rivendell il existe un group gmail:

[https://groups.google.com/forum/#!forum/rivendell-fr](https://groups.google.com/forum/#!forum/rivendell-fr)

```bash
su -
yum -y install wget

wget http://download.paravelsystems.com/CentOS/7rd3/Paravel-Rivendell3.repo -P /etc/yum.repos.d/
wget http://download.paravelsystems.com/CentOS/7rd3/RPM-GPG-KEY-Paravel-Broadcast -P /etc/pki/rpm-gpg
yum -y install rivendell-install
```

Pour une installation du server:

```bash
/root/install_rivendell.sh --standalone
```

Pour une installation d'un client:

```bash
/root/install_rivendell.sh --client
```

Pour valider la connection du client avec le server:

Récupérer l'IP du IP_CLIENT_RIVENDELL
```bash
ip -c a
```
Puis connecter vous a la DB de Rivendell

```bash
ssh rd@IP_SERVER_RIVENDELL
mysql -uroot Rivendell

GRANT ALL PRIVILEGES ON *.* TO 'rduser'@'IP_CLIENT_RIVENDELL' IDENTIFIED BY 'letmein' WITH GRANT OPTION;
```

a noter que vous devez changer le mot de pass aprés installation

```bash
passwd rd
```

Supprimez le script d'installation avec :

yum -y remove rivendell-install

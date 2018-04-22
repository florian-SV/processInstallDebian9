
# Processus d'installation de mon environnement Debian 9

### Après l'installation de l'iso (sans environnement graphique):

    apt-get update && apt-get upgrade

### Installation autre

    apt-get install ssh git ntfs-3g sudo dirmngr
    git config --global core.editor "vim"


### Installation du serveur web

    apt install apache2
    apt install php7.0 php7.0-cli php7.0-common php7.0-curl php7.0-fpm php7.0-gd php7.0-imap php7.0-intl php7.0-json php7.0-mbstring php7.0-mysql php7.0-opcache php7.0-snmp php7.0-tidy php7.0-xml php7.0-zip php7.0-mysql php7.0-odbc php7.0-mcrypt php7.0-pgsql php7.0-sqlite3 php7.0-bz2
    apt install mariadb-server
    mysql_secure_installation


### Installation de Xorg:

    apt-get install xorg

### Installation du driver nvidia pour carte graphique 1050 ti : (https://linuxconfig.org/how-to-install-the-latest-nvidia-drivers-on-debian-9-stretch-linux)

    apt install llvm-3.9 clang-3.9

Ajout sur toute les lignes du fichier */apt/apt/source.list*  les repos : **contrib non-free**	après le **main**
Activer l'i386 : `dpkg --add-architecture i386`

    apt install firmware-linux build-essential gcc-multilib
    apt build-dep linux

Trouver le driver sur https://www.nvidia.com/Download/Find.aspx?lang=en-us, et le télécharger
Lui mettre les droits d’exécution et le lancer (télécharger les dépendances qui lui manque si besoin)

Lancer **startx**

### Installation de i3

    apt-get install i3 i3-wm

Concernant la taille de police toute petite sur la console, par défaut debian utilise ces options la du fichier */etc/default/console-setup* :

    CHARMAP="UTF-8"
    CODESET="Lat15"
    FONTFACE="Fixed"
    FONTSIZE="8x16"

 Pour modifier les fonts : `sudo dpkg-reconfigure console-setup`

### Installation de Oh My zsh (https://github.com/robbyrussell/oh-my-zsh)

    apt-get install zsh
    sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

Prendre le thème **avit**

Si zsh n'est pas mis en temps que shell par défaut : `chsh -s /bin/zsh`

### Installation et utilisation imprimante Canon
Aller sur la page driver de l'imprimante sur le site de Canon
Téléchager le .deb
Lancer le **install.sh**

### Installation de JAVA https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-get-on-debian-8

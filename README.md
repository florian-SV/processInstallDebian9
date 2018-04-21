# processInstallDebian9

### Après l'installation de l'iso (sans environnement graphique):

    apt-get update && apt-get upgrade

### Installation de xorg:

    apt-get install xorg

### Installation du driver nvidia pour carte graphique 1050 ti : (https://linuxconfig.org/how-to-install-the-latest-nvidia-drivers-on-debian-9-stretch-linux)

    apt install llvm-3.9 clang-3.9

Ajout sur toute les lignes du fichier */apt/apt/source.list*  les repos : **contrib non-free**	après le **main**
Activer l'i386 : `dpkg --add-architecture i386`

    apt install firmware-linux build-essential gcc-multilib
    apt build-dep linux
    
Trouver le driver sur https://www.nvidia.com/Download/Find.aspx?lang=en-us, et le télécharger
Lui mettre les droits d’exécution et le lancer (télécharger les dépendances qui lui manque si besoin)

### Installation de i3

    apt-get install i3 i3-wm
    
### Installation de Oh My zsh (https://github.com/robbyrussell/oh-my-zsh)

    apt-get install zsh
    sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

Prendre le theme **avit**

Si zsh n'est pas mis en temps que shell par défaut : `chsh -s /bin/zsh`

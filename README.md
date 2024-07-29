# maven_docs
## Installer Maven 3.9.6 Manuellement sous ubuntu

- Téléchargez Maven 3.9.6 depuis le site officiel d'Apache :
```bash
wget https://downloads.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz
```

- Extrayez l'archive :
```bash
tar xzvf apache-maven-3.9.6-bin.tar.gz
```

- Déplacez les fichiers extraits vers un répertoire approprié :
```bash
sudo mv apache-maven-3.9.6 /opt/maven
```

- Configurez les variables d'environnement en créant un fichier de configuration :
```bash
sudo nano /etc/profile.d/maven.sh
```

- Ajoutez les lignes suivantes dans ce fichier :
```sh
export M2_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}
```

- Rendez le script exécutable :
```bash
sudo chmod +x /etc/profile.d/maven.sh
```

- Chargez les nouvelles variables d'environnement dans la session courante :
```bash
source /etc/profile.d/maven.sh
```

- Vérifiez l'installation :
```bash
mvn -version
```
## Desinstaller Maven 3.9.6 Manuellement sous ubuntu
- Si vous avez installé Maven via apt, désinstallez-le en utilisant :

```bash
sudo apt remove maven
```

- Si vous avez installé Maven manuellement, supprimez les fichiers :
```bash
sudo rm -rf /opt/maven
sudo rm /etc/profile.d/maven.shant.d
```

## Installation de Maven sous Windows 11
### Télécharger Maven
- Allez sur la page de téléchargement de Maven : [Apache Maven Downloads](https://maven.apache.org/download.cgi).

- Téléchargez le fichier d'archive binaire (par exemple, `apache-maven-3.9.6-bin.zip`).

### Extraire Maven
- Extrayez le contenu du fichier ZIP téléchargé dans un répertoire de votre choix (par exemple, `C:\Program Files\Apache\maven`).

### Configurer les variables d'environnement
- Ouvrir les Paramètres de l'ordinateur :
    - Appuyez sur `Win + R`, tapez `sysdm.cpl`, et appuyez sur `Entrée`.

- Accéder aux variables d'environnement :
    - Cliquez sur l'onglet `Avancé`, puis sur `Variables d'environnement`.

- Ajouter `M2_HOME` :
    - Cliquez sur `Nouveau` sous les `Variables système`.
    - Entrez `M2_HOME` comme nom de la variable et le chemin où vous avez extrait Maven (par exemple, `C:\Program Files\Apache\maven\apache-maven-3.9.6`) comme valeur de la variable.

- Ajouter `MAVEN_HOME` :
    - Répétez le processus ci-dessus et ajoutez `MAVEN_HOME` avec le même chemin que pour `M2_HOME`.

- Mettre à jour la variable Path :
    - Sélectionnez la variable `Path` sous les `Variables système` et cliquez sur `Modifier`.
    - Cliquez sur `Nouveau` et ajoutez `%M2_HOME%\bin`.

- Appliquer les changements :
    - Cliquez sur `OK` pour fermer toutes les fenêtres des variables d'environnement.

### Vérifier l'installation
- Ouvrez un terminal (Invite de commandes ou PowerShell).
- Tapez `mvn -v` et appuyez sur `Entrée`.
- Vous devriez voir les informations de version de Maven si l'installation a réussi.

## Désinstallation de Maven sous Windows 11
### Supprimer le répertoire de Maven
- Supprimez le répertoire où vous avez extrait Maven (par exemple, `C:\Program Files\Apache\maven\apache-maven-3.9.6`).

### Supprimer les variables d'environnement
- Ouvrir les Paramètres de l'ordinateur :
    - Appuyez sur `Win + R`, tapez `sysdm.cpl`, et appuyez sur `Entrée`.

- Accéder aux variables d'environnement :
    - Cliquez sur l'onglet `Avancé`, puis sur `Variables d'environnement`.

- Supprimer `M2_HOME` et `MAVEN_HOME` :
    - Sélectionnez `M2_HOME` et cliquez sur `Supprimer`.
    - Répétez le processus pour `MAVEN_HOME`.

- Mettre à jour la variable Path :
    - Sélectionnez la variable Path sous les `Variables système` et cliquez sur `Modifier`.
    - Recherchez et supprimez l'entrée `%M2_HOME%\bin`.

- Appliquer les changements :
    - Cliquez sur `OK` pour fermer toutes les fenêtres des variables d'environnement.
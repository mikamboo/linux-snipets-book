# SCP : Copy files and folder

> Required : SSH installed

Copie d'un fichier d'une machine serveur1 vers une autre machine serveur2:

```text
$ scp Login1@Serveur1:Chemin1/NomFichier1 Login2@Serveur2:Chemin2/NomFichier2
```

Copie d'un fichier depuis le répertoire courant vers un répertoire du serveur:

```text
$ scp Fichier login@serveur:Chemin
```

Copie d'un répertoire, avec éventuellement ses sous-répertoires, vers un répertoire du serveur:

```text
$ scp -r Repertoire login@serveur:Chemin
```

Copie d'un fichier du serveur vers le répertoire courant:

```text
$ scp login@serveur:Chemin/Fichier .
```

Copie d'un répertoire du serveur vers le répertoire courant:

```text
$ scp -r login@serveur:Chemin/Repertoire .
```

**Sample :**

```text
# copy file
$ scp user01@server.fr:/home/c/calvat/Readme.txt .

# copy folder
$ scp -r user01@server.fr:/home/c/calvat/toto .
```


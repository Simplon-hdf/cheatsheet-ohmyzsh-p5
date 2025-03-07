# Cheatsheet des Plugins Oh My Zsh

Oh My Zsh propose une large collection de plugins qui améliorent votre expérience en ligne de commande. Voici un guide des plugins les plus utiles et comment les utiliser.

## Comment activer un plugin

Pour activer un plugin, modifiez votre fichier `~/.zshrc` et ajoutez le nom du plugin dans la liste des plugins :

```zsh
plugins=(git aliases npm ...)
```

## Plugins Essentiels

### 1. git
Le plugin le plus populaire qui ajoute de nombreux alias pour les commandes Git.

Alias principaux :
- `g` : git
- `ga` : git add
- `gc` : git commit
- `gco` : git checkout
- `gp` : git push
- `gl` : git pull
- `gst` : git status

### 2. aliases
Un plugin très pratique qui permet de gérer facilement vos alias.

Commandes principales :
- `acs` : affiche tous vos alias actuels
- `alias-finder` : trouve les alias correspondant à une commande
- `al` : liste tous les alias
- `als` : recherche un alias spécifique
- `acl` : efface tous les alias définis

### 3. npm
Raccourcis pour les commandes npm courantes.

Alias principaux :
- `npmI` : npm init
- `npmS` : npm install -S (save to dependencies)
- `npmD` : npm install -D (save to dev dependencies)
- `npmg` : npm install -g (installation globale)
- `npmR` : npm run
- `npmrd` : npm run dev
- `npmst` : npm start
- `npmt` : npm test
- `npmrb` : npm run build

### 4. z
Navigation rapide entre les répertoires fréquemment utilisés.
- Utilisation : tapez `z` suivi d'une partie du nom du répertoire

### 5. sudo
Appuyez deux fois sur la touche `ESC` pour ajouter `sudo` au début de votre commande.

### 6. web-search
Recherchez directement depuis votre terminal.
- `google query` : recherche Google
- `ddg query` : recherche DuckDuckGo
- `github query` : recherche GitHub

### 7. copypath
Copie le chemin du fichier actuel dans le presse-papiers.
- `copypath` : copie le chemin absolu
- `copyfile` : copie le contenu du fichier

### 8. extract
Décompresse n'importe quel type d'archive avec une seule commande.
- Utilisation : `extract archive.zip`

## Plugins pour Développeurs

### 1. vscode
Intégration avec Visual Studio Code
- `vsc` : ouvre VS Code
- `vsca` : ouvre VS Code avec tous les arguments
- `vscd` : ouvre VS Code dans le répertoire courant

### 2. docker
Alias pour Docker et Docker Compose
- `dps` : docker ps
- `dpa` : docker ps -a
- `di` : docker images
- `dex` : docker exec -it
- `dcup` : docker-compose up
- `dcdown` : docker-compose down

### 3. python
Alias pour Python et environnements virtuels
- `py` : python
- `pip` : pip install
- `venv` : python -m venv
- `activate` : source venv/bin/activate
- `deactivate` : désactive l'environnement virtuel


## Astuces

1. Pour voir tous les alias d'un plugin :
```zsh
alias | grep nomDuPlugin
```

2. Pour recharger les plugins après modification :
```zsh
source ~/.zshrc
```

## Plugins Recommandés pour Débutants

1. git
2. z
3. sudo
4. extract
5. web-search

Ces plugins sont un excellent point de départ pour améliorer votre productivité avec Oh My Zsh.
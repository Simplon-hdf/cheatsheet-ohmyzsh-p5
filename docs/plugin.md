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

## Plugins Avancés Super Utiles

### 1. autojump
Navigation rapide entre répertoires basée sur l'historique de navigation.
```bash
# Installation préalable nécessaire
# Sur macOS: brew install autojump
# Sur Ubuntu: apt-get install autojump

# Utilisation
j nom_partiel_du_dossier  # Saute directement au dossier correspondant
```

### 2. fzf
Recherche floue puissante pour filtrer l'historique, les fichiers et plus encore.
```bash
# Installation préalable nécessaire
# brew install fzf ou git clone https://github.com/junegunn/fzf.git ~/.fzf && ~/.fzf/install

# Utilisation
CTRL+R  # Recherche dans l'historique des commandes
CTRL+T  # Recherche de fichiers
ALT+C   # Navigation rapide entre répertoires
```

### 3. zsh-autosuggestions
Suggestions automatiques basées sur l'historique des commandes.
```bash
# Installation
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# Activation dans ~/.zshrc
plugins=(... zsh-autosuggestions)

# Utilisation
# Commencez à taper, acceptez la suggestion avec flèche droite
```

### 4. zsh-syntax-highlighting
Coloration syntaxique des commandes en temps réel.
```bash
# Installation
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# Activation dans ~/.zshrc
plugins=(... zsh-syntax-highlighting)
```

### 5. thefuck
Corrige automatiquement les commandes erronées.
```bash
# Installation préalable nécessaire
# pip install thefuck ou brew install thefuck

# Utilisation
apt-get install python  # Commande avec erreur
fuck  # Corrige automatiquement en sudo apt-get install python
```

### 6. dirhistory
Navigation rapide dans l'arborescence avec des raccourcis clavier.
```bash
# Utilisation
ALT+Gauche  # Revenir au dossier parent
ALT+Droite  # Aller au premier sous-dossier
ALT+Haut    # Naviguer dans l'historique des dossiers (précédent)
ALT+Bas     # Naviguer dans l'historique des dossiers (suivant)
```

### 7. history-substring-search
Recherche intelligente dans l'historique des commandes.
```bash
# Utilisation
# Tapez le début d'une commande
# Utilisez les flèches haut/bas pour parcourir les commandes correspondantes
```

### 8. colored-man-pages
Pages de manuel colorées pour une meilleure lisibilité.
```bash
# Utilisation
man ls  # Affiche la page de manuel avec coloration syntaxique
```

### 9. gitignore
Génération rapide de fichiers .gitignore.
```bash
# Utilisation
gi list                      # Liste tous les templates disponibles
gi python,node >> .gitignore # Génère un .gitignore pour Python et Node.js
```

## Astuces

1. Pour voir tous les alias d'un plugin :
```zsh
alias | grep nomDuPlugin
```

2. Pour recharger les plugins après modification :
```zsh
source ~/.zshrc
```

3. Configuration recommandée pour une productivité maximale :
```zsh
plugins=(
  git
  z
  sudo
  extract
  web-search
  zsh-autosuggestions
  zsh-syntax-highlighting
  history-substring-search
  colored-man-pages
  dirhistory
)
```

## Plugins Recommandés pour Débutants

1. git
2. z
3. sudo
4. extract
5. web-search
6. zsh-autosuggestions
7. colored-man-pages

Ces plugins sont un excellent point de départ pour améliorer votre productivité avec Oh My Zsh.
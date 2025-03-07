# Installation de OhMyZsh

### Prérequis : 

- Zsh (v4.3.9 ou plus récent, préférence pour v5.0.8+).
- curl ou wget.
- git (v2.4.11 ou supérieur recommandé).

## Oh My Zsh est compatible avec les systèmes d'exploitation suivants :

| Système d'exploitation | Statut |
|------------------------|--------|
| Android                | ✅     |
| freeBSD                | ✅     |
| Linux                  | ✅     |
| macOS                  | ✅     |
| OS/2 Warp              | ❌     |
| Windows (WSL2)         | ✅     |

## Installation de base 

Oh My Zsh est installé en exécutant l'une des commandes suivantes dans votre terminal. Vous pouvez l'installer via la ligne de commande avec l'un ou l'autre de curl, wget, ou un autre outil similaire.

| Méthode  | Commande |
|----------|----------|
| curl | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| wget     | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| Fetch    | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

## Autre methode 

Alternativement, l'installateur est également disponible en miroir en dehors de GitHub. Cette URL peut être nécessaire si vous êtes dans un pays comme la Chine ou l'Inde, où certains fournisseurs d'accès à Internet bloquent ```raw.githubusercontent.com```

| Méthode  | Commande |
|----------|----------|
| curl | `sh -c "$(curl -fsSL https://install.ohmyz.sh/)"` |
| wget     | `sh -c "$(wget -O- https://install.ohmyz.sh/)"` |
| Fetch    | `sh -c "$(fetch -o - https://install.ohmyz.sh/)"` |


## Installation Avancée Oh My Zsh

### Répertoire Personnalisé
Emplacement par défaut: `~/.oh-my-zsh`

Pour changer le répertoire:
```bash
ZSH="$HOME/.dotfiles/oh-my-zsh" sh install.sh
```

### Installation Automatisée
```bash

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" 

--unattended
```
Alternative si blocage: `https://install.ohmyz.sh`

### Installation depuis un Fork
Variables acceptées:
* `REPO` (défaut: `ohmyzsh/ohmyzsh`)
* `REMOTE` (défaut: `https://github.com/${REPO}.git`)
* `BRANCH` (défaut: `master`)

Exemple:
```bash
REPO=apjanke/oh-my-zsh BRANCH=edge sh install.sh
```

### Installation Manuelle
1. Cloner: `git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh`
2. Sauvegarder (optionnel): `cp ~/.zshrc ~/.zshrc.orig`
3. Créer config: `cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc`
4. Changer shell: `chsh -s $(which zsh)`
5. Redémarrer session

### Résolution de problèmes
* Vérifier `PATH` dans `~/.zshrc`
* Vérifier variable `ZSH` dans `~/.zshrc`



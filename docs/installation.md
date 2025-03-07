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

### Obtenir des Mises à Jour

Par défaut, un rappel pour vérifier les mises à jour vous sera proposé toutes les 2 semaines. Vous pouvez choisir d'autres modes de mise à jour en ajoutant une ligne dans votre fichier `~/.zshrc`, **avant le chargement de Oh My Zsh** :

1. Mise à jour automatique sans demande de confirmation :

```bash
zstyle ':omz:update' mode auto
```

2. Simplement offrir un rappel tous les quelques jours, s'il y a des mises à jour disponibles :

```bash
zstyle ':omz:update' mode reminder
```

3. Pour désactiver entièrement les mises à jour automatiques :

```bash
zstyle ':omz:update' mode disabled
```

**REMARQUE** : vous pouvez contrôler la fréquence à laquelle Oh My Zsh vérifie les mises à jour avec le paramètre suivant :

```bash
# Ceci vérifiera les mises à jour tous les 7 jours
zstyle ':omz:update' frequency 7
# Ceci vérifiera les mises à jour chaque fois que vous ouvrez le terminal (non recommandé)
zstyle ':omz:update' frequency 0
```

### Verbosité des Mises à Jour

Vous pouvez également limiter la verbosité des mises à jour avec les paramètres suivants :

```bash
zstyle ':omz:update' verbose default # invite de mise à jour par défaut

zstyle ':omz:update' verbose minimal # seulement quelques lignes

zstyle ':omz:update' verbose silent # seulement les erreurs
```

### Mises à Jour Manuelles

Si vous souhaitez effectuer une mise à jour à tout moment (peut-être que quelqu'un vient de publier un nouveau plugin et vous ne voulez pas attendre une semaine ?), vous devez simplement exécuter :

```bash
omz update
```

**Remarque**

Si vous souhaitez automatiser ce processus dans un script, vous devriez appeler directement le script `upgrade`, comme ceci :

```bash
$ZSH/tools/upgrade.sh
```

Consultez plus d'options dans la FAQ : Comment mettre à jour Oh My Zsh ?

**L'UTILISATION DE** `omz update --unattended` **A ÉTÉ SUPPRIMÉE, CAR ELLE PRÉSENTE DES EFFETS SECONDAIRES.**


## Désinstallation de Oh My Zsh

Oh My Zsh n'est pas pour tout le monde. Vous nous manquerez, mais nous voulons que cette séparation soit facile.

Si vous souhaitez désinstaller `oh-my-zsh`, exécutez simplement `uninstall_oh_my_zsh` depuis la ligne de commande. Il se supprimera et restaurera votre configuration précédente de `bash` ou `zsh`.


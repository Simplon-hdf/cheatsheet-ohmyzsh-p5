![Logo](https://camo.githubusercontent.com/41da1086e4c3ec341b78f7c4376f3b94aff529e61a5c3211cdae315bf92e97c3/68747470733a2f2f6f686d797a73682e73332e616d617a6f6e6177732e636f6d2f6f6d7a2d616e73692d6769746875622e706e67)

=======
# Oh My Zsh Cheat Sheet

## 1. Introduction
**Oh My Zsh** est un framework open-source pour la gestion de la configuration de **Zsh**, offrant plusieurs fonctionnalités telles que des thèmes personnalisables, des plugins utiles et des raccourcis pratiques.

### Avantages et caractéristiques :
- Installation et configuration faciles
- Support de nombreux thèmes
- Gestion avancée des plugins
- Amélioration de l'expérience en ligne de commande

---

## 2. Installation et configuration
### Installer Oh My Zsh :
Exécutez l'une des commandes suivantes :
```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
ou
```sh
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Changer le shell par défaut en Zsh :
```sh
chsh -s $(which zsh)
```

---

## 3. Gestion des plugins
### Activer des plugins :
- Modifiez le fichier `~/.zshrc` et ajoutez les plugins dans la section `plugins` :
```sh
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```
- Rechargez Zsh :
```sh
source ~/.zshrc
```

### Plugins populaires :
- `git` - Raccourcis pour Git
- `zsh-autosuggestions` - Suggestions automatiques de commandes
- `zsh-syntax-highlighting` - Coloration syntaxique des commandes

---

## 4. Thèmes (Themes)
### Changer de thème :
- Modifiez le fichier `~/.zshrc` et changez la valeur de `ZSH_THEME` :
```sh
ZSH_THEME="agnoster"
```
- Appliquez les modifications :
```sh
source ~/.zshrc
```

### Thèmes populaires :
- **agnoster** - Affiche les informations Git et les branches
- **powerlevel10k** - Hautement personnalisable avec de nombreuses fonctionnalités avancées

---

## 5. Commandes et raccourcis utiles
### Commandes principales :
- `cd -`  → Retour au répertoire précédent
- `!!`  → Réexécuter la dernière commande
- `alias ll='ls -lah'` → Créer un raccourci pour afficher la liste des fichiers

### Raccourcis pratiques :
- `Ctrl + R` → Rechercher dans l'historique des commandes
- `Ctrl + U` → Effacer toute la ligne
- `Ctrl + W` → Supprimer le dernier mot

---

## 6. Personnalisation des paramètres
### Modifier le fichier `.zshrc` :
```sh
nano ~/.zshrc
```
### Créer des alias personnalisés :
```sh
echo "alias gs='git status'" >> ~/.zshrc
source ~/.zshrc
```

---

## 7. Résolution des problèmes courants
### Problème : Les commandes ne s'exécutent pas correctement
**Solution :** Vérifiez le fichier `~/.zshrc` et assurez-vous que les plugins nécessaires sont bien activés.

### Problème : Le thème ne change pas après modification de `~/.zshrc`
**Solution :** Exécutez la commande suivante :
```sh
source ~/.zshrc
```
ou **redémarrez votre terminal**.

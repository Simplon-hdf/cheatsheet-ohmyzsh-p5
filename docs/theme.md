# 🎨 Thèmes Oh My Zsh

## ✨ Vue d'ensemble

Les thèmes transforment votre terminal en un outil à la fois esthétique et fonctionnel. Ils personnalisent le prompt pour afficher des informations essentielles comme le répertoire courant, l'état Git, et plus encore.

## 🚀 Utilisation

```bash
# Dans votre ~/.zshrc
ZSH_THEME="nom_du_theme"

# Puis rechargez
source ~/.zshrc
```

## 🌟 Thèmes populaires

### robbyrussell (défaut)
Simple et efficace, affiche l'état Git et le répertoire courant.
```bash
➜ projet git:(main) ✗
```

### agnoster
Un prompt segmenté élégant avec informations contextuelles.
> 💡 Nécessite une police Powerline

![Agnoster](https://cloud.githubusercontent.com/assets/2618447/6316862/70f58fb6-ba03-11e4-82c9-c083bf9a6574.png)

### powerlevel10k
Ultra-rapide et hautement personnalisable.
> 💡 Installation: `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`

![P10k](https://raw.githubusercontent.com/romkatv/powerlevel10k-media/master/prompt-styles-high-contrast.png)

### Autres pépites
- **avit**: Minimaliste avec heure
- **bira**: Deux lignes avec user@host
- **fino-time**: Élégant avec date et heure

## 🔧 Créer votre thème

1. Créez un fichier `~/.oh-my-zsh/custom/themes/mon_theme.zsh-theme`
2. Définissez votre PROMPT:

```bash
# Exemple simple
PROMPT='%{$fg[cyan]%}%c%{$reset_color%} $(git_prompt_info)> '

# Variables utiles
# %n - utilisateur
# %m - machine
# %~ - répertoire
# %c - dossier actuel
# $(git_prompt_info) - info Git
```

## 🎭 Astuces

### Palette de couleurs
```bash
%{$fg[red]%}     # Rouge
%{$fg_bold[red]%} # Rouge gras
%{$bg[blue]%}    # Fond bleu
%{$reset_color%} # Réinitialiser
```
> Couleurs: black, red, green, yellow, blue, magenta, cyan, white

### Prompt sur deux lignes
```bash
PROMPT='%{$fg[yellow]%}%~%{$reset_color%} $(git_prompt_info)
%{$fg[red]%}❯ %{$reset_color%}'
```

### Intégration Git avancée
```bash
$(git_prompt_info)    # Info basique
$(git_prompt_status)  # Statut détaillé
```

## 🔍 Dépannage

- **Caractères cassés?** → Installez la police Nerd Font
- **Prompt lent?** → Essayez powerlevel10k ou un thème plus léger

## 📚 Ressources

- [Galerie de thèmes](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)
- [Variables pour thèmes](https://github.com/ohmyzsh/ohmyzsh/wiki/Theme-Variables)
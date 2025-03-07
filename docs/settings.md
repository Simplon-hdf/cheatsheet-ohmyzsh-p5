# ⚙️ Paramètres Oh My Zsh

## Configuration de base

Oh My Zsh se configure principalement via le fichier `~/.zshrc`. C'est là que vous définirez vos préférences pour adapter le shell à votre workflow.

```bash
# Où est installé Oh My Zsh
export ZSH="$HOME/.oh-my-zsh"

# Choix du thème
ZSH_THEME="robbyrussell"

# Gestion des mises à jour
DISABLE_AUTO_UPDATE="false"
UPDATE_ZSH_DAYS=13
```

## Autocomplétion et correction

Zsh est réputé pour sa puissante autocomplétion. Voici comment l'ajuster:

```bash
# Sensibilité à la casse dans la complétion
CASE_SENSITIVE="false"

# Traiter les tirets et underscores comme équivalents
HYPHEN_INSENSITIVE="false"

# Correction automatique des commandes
ENABLE_CORRECTION="true"

# Afficher des points pendant la recherche de complétion
COMPLETION_WAITING_DOTS="true"
```

## Mises à jour et maintenance

Gérez quand et comment Oh My Zsh se met à jour:

```bash
# Désactiver complètement les mises à jour
DISABLE_AUTO_UPDATE="true"

# Installer les mises à jour sans demander
DISABLE_UPDATE_PROMPT="true"
```

## Comportement du terminal

Personnalisez l'apparence et le comportement de votre terminal:

```bash
# Gestion du titre automatique de la fenêtre du terminal
DISABLE_AUTO_TITLE="false"

# Activer les couleurs pour ls et autres commandes
DISABLE_LS_COLORS="false"

# Format des dates dans l'historique
HIST_STAMPS="yyyy-mm-dd"

# Taille de l'historique
HISTSIZE=10000
SAVEHIST=10000
```

## Plugins et extensions

Les plugins sont l'un des grands atouts d'Oh My Zsh:

```bash
# Liste des plugins à charger
plugins=(git docker vscode npm)

# Charger Oh My Zsh avec les plugins configurés
source $ZSH/oh-my-zsh.sh
```

## Variables d'environnement

Configurez votre environnement de travail:

```bash
# Langue et encodage
export LANG=fr_FR.UTF-8

# Éditeur préféré
export EDITOR='vim'

# Pager pour l'affichage de contenu long
export PAGER='less'
```

## Optimisation des performances

Si votre shell devient lent, ces réglages peuvent aider:

```bash
# Éviter de vérifier les fichiers non suivis dans Git
# Améliore considérablement les performances dans les grands dépôts
DISABLE_UNTRACKED_FILES_DIRTY="true"

# Cache pour l'autocomplétion
ZSH_COMPDUMP="$ZSH/cache/.zcompdump"
```

## Personnalisation

Adaptez Oh My Zsh à votre environnement spécifique:

```bash
# Dossier pour vos personnalisations
ZSH_CUSTOM="$HOME/.oh-my-zsh-custom"

# Configuration conditionnelle selon la machine
if [[ "$HOST" == "laptop" ]]; then
  # Configuration spécifique au laptop
  ZSH_THEME="agnoster"
else
  # Configuration pour autres machines
  ZSH_THEME="robbyrussell"
fi
```

## Problèmes courants et solutions

- **Démarrage lent**: Réduisez le nombre de plugins ou utilisez des alternatives plus légères
- **Conflits entre plugins**: Changez l'ordre de chargement dans la liste des plugins
- **Problèmes de caractères**: Vérifiez que votre terminal utilise une police compatible

## Bonnes pratiques

- Gardez une copie de sauvegarde de votre configuration
- Commentez votre fichier `.zshrc` pour vous rappeler pourquoi vous avez fait certains choix
- Testez les nouvelles configurations dans une session temporaire avant de les adopter définitivement
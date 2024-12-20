# Configuration des outils Git

**La configuration de Git se fait généralement à l'aide de la commande `git config`.** Voici quelques commandes courantes pour configurer Git :

```
 git config --global user.name "[nom]"
```
Définit le nom que vous voulez associer à vos commits.

```
 git config --global user.email "[adresse email]"
```
Définit l'email que vous voulez associer à vos commits.

```
 git config --global color.ui auto
```
Active la colorisation de la sortie en ligne de commande.

```
 git config --list
```
Affiche toutes les configurations Git actuelles.

# Créer des repositories

**Démarrer un nouveau repository ou en obtenir un depuis une URL existante**

```
 git init [nom-du-projet]
```

Crée un dépôt local à partir du nom spécifié

```
 git clone [url]
```

Télécharge un projet et tout son historique de versions

# Effectuer des changements

**Consulter les modifications et effectuer une opération de commit**

```
 git status
```

Liste tous les nouveaux fichiers et les fichiers modifiés à commiter

```
 git diff
```

Montre les modifications de fichier qui ne sont pas encore indexées

```
 git add [fichier]
```

Ajoute un instantané du fichier, en préparation pour le suivi de version

```
 git diff --staged
```

Montre les différences de fichier entre la version indexée et la dernière version

```
 git reset [fichier]
```

Enleve le fichier de l'index, mais conserve son contenu

```
 git commit -m "[message descriptif]"
```

Enregistre des instantanés de fichiers de façon permanente dans l'historique des versions

# GROUPER DES CHANGEMENTS

**Nommer une série de commits et combiner les résultats de travaux terminés**

```
 git branch
```
Liste toutes les branches locales dans le dépôt courant.

```
 git branch [nom-de-branche]
```
Crée une nouvelle branche.

```
 git checkout [nom-de-branche]
```
Bascule sur la branche spécifiée et met à jour le répertoire de travail.

```
 git merge [nom-de-branche]
```
Combine dans la branche courante l'historique de la branche spécifiée.

```
 git branch -d [nom-de-branche]
```
Supprime la branche spécifiée.

# CHANGEMENTS AU NIVEAU DES NOMS DE FICHIERS

**Pour gérer les changements de noms de fichiers dans Git, vous pouvez utiliser les commandes suivantes :**

```
 git rm [fichier]
```
Supprime le fichier du répertoire de travail et met à jour l'index.

```
 git rm --cached [fichier]
```

Supprime le fichier du système de suivi de version mais le préserve
localement

```
 git mv [fichier-origine] [fichier-renommé]
```
Renomme un fichier et prépare le changement pour un commit.

## EXCLURE DU SUIVI DE VERSION

1. **Créer un fichier `.gitignore`** à la racine de votre dépôt, si ce n'est pas déjà fait.
2. **Ajouter les fichiers ou répertoires** que vous souhaitez ignorer. Par exemple :

```
# Ignorer les fichiers temporaires
*.tmp

# Ignorer le dossier de build
/build/

# Ignorer les fichiers de configuration
config/*.json
```

```
 git ls-files --other --ignored --exclude-standard
```
Liste tous les fichiers exclus du suivi de version dans ce projet.

# Enregistrer des fragments

**Mettre en suspens des modifications non finies pour y revenir plus tard**

```
 git stash
```

Enregistre de manière temporaire tous les fichiers sous suivi de version qui ont été modifiés ("remiser son travail")

```
 git stash list
```

Liste toutes les remises

```
 git stash pop
```

Applique une remise et la supprime immédiatement

```
 git stash drop
```

Supprime la remise la plus récente

# VÉRIFIER L'HISTORIQUE DES VERSIONS

**Pour examiner l'historique des commits et des changements dans un dépôt Git, vous pouvez utiliser les commandes suivantes :**

```
 git log
```
Affiche l'historique des commits pour la branche actuelle.

```
 git log --follow [fichier]
```
Affiche l'historique des versions d'un fichier, y compris les renommages.

```
 git diff [première-branche]...[deuxième-branche]
```
Montre les différences de contenu entre deux branches.

```
 git show [commit]
```
Affiche les métadonnées et les changements de contenu du commit spécifié.

# Refaire des commits

**Corriger des erreurs et gérer l'historique des corrections**

```
 git reset [commit]
```

Annule tous les commits après `[commit]`, en conservant les modifications localement

```
 git reset --hard [commit]
```

Supprime tout l'historique et les modifications effectuées après le commit spécifié

# SYNCHRONISER LES CHANGEMENTS

**Référencer un dépôt distant et synchroniser l'historique de versions**

```
 git fetch [nom-de-depot]
```
Récupère tout l'historique du dépôt nommé.

```
 git merge [nom-de-depot]/[branche]
```
Fusionne la branche du dépôt dans la branche locale courante.

```
 git push [alias] [branche]
```
Envoie tous les commits de la branche locale vers GitHub.

## Git Rebase

`git rebase` est une commande puissante qui permet de réorganiser l'historique des commits. Voici un aperçu de son utilisation :

### Utilisation de base

```bash
git rebase <base>
```

Cette commande prend les commits de la branche courante et les réapplique sur le sommet de la branche `<base>`.

### Rebase interactif

```bash
git rebase -i <base>
```

Le mode interactif permet de modifier les commits pendant le rebase. Vous pouvez :

- Réorganiser l'ordre des commits
- Supprimer des commits
- Fusionner plusieurs commits
- Modifier les messages de commit

#### Argument de rebase 

Chaque ligne dans l'éditeur représente un commit et commence par une commande (par défaut "pick"). Vous pouvez changer ces commandes pour modifier l'historique :

- `pick` : utiliser le commit tel quel
- `reword` : modifier le message du commit
- `edit` : modifier le contenu du commit
- `squash` : fusionner le commit avec le précédent
- `fixup` : comme squash, mais en ignorant le message de commit
- `drop` : supprimer le commit

Après avoir modifié et sauvegardé le fichier, Git appliquera vos changements.

### Cas d'utilisation courants

1. **Nettoyer l'historique** : Fusionner plusieurs petits commits en un seul plus significatif.
2. **Intégrer les derniers changements** : Mettre à jour une branche de fonctionnalité avec les derniers changements de la branche principale.
3. **Résoudre les conflits** : Gérer les conflits commit par commit plutôt qu'en une seule fois.

### Précautions

- Ne jamais rebase des commits qui ont déjà été poussés sur un dépôt public.
- Toujours créer une sauvegarde (branche) avant de commencer un rebase.

### Résolution des conflits

Si des conflits surviennent pendant le rebase :

1. Résolvez les conflits manuellement.
2. Ajoutez les fichiers résolus avec `git add`.
3. Continuez le rebase avec `git rebase --continue`.

### Annuler un rebase

Si quelque chose se passe mal, vous pouvez annuler le rebase :

```bash
git rebase --abort
```

Cette commande restaure l'état de votre branche avant le début du rebase.

# Les bases de Python : Variables

## Définition et utilisation

- Les variables permettent de stocker des données en mémoire
- Elles sont créées avec le signe `=` (opérateur d'affectation)
- Syntaxe : `nom_variable = valeur`

## Nommage des variables 

- Utilisez des noms explicites et en anglais
- Commencez par une lettre minuscule
- Utilisez des underscores pour séparer les mots (snake_case)
- Évitez les caractères spéciaux et accentués

## Types de données

- Nombres entiers (int) : `age = 25`
- Nombres décimaux (float) : `price = 9.99`
- Chaînes de caractères (str) : `name = "Alice"`
- Booléens (bool) : `is_student = True`

## Opérations sur les variables

- Arithmétiques : `+`, `-`, `*`, `/`, `//` (division entière), `%` (modulo)
- Concaténation de chaînes : `full_name = first_name + " " + last_name`
- Conversion de types : `int()`, `float()`, `str()`

## Bonnes pratiques

- Initialisez vos variables avant de les utiliser
- Utilisez des constantes (en majuscules) pour les valeurs fixes
- Commentez votre code pour expliquer l'utilité des variables

# Types de données en Python

## Types de base

- **Entiers (int)** : Nombres entiers sans décimales
  - Exemple : `age = 25`

- **Nombres à virgule flottante (float)** : Nombres décimaux
  - Exemple : `prix = 19.99`

- **Chaînes de caractères (str)** : Texte entre guillemets simples ou doubles
  - Exemple : `nom = "Alice"`

- **Booléens (bool)** : Valeurs `True` ou `False`
  - Exemple : `est_etudiant = True`

## Collections

- **Listes** : Séquences ordonnées et modifiables
  - Syntaxe : `ma_liste = [1, 2, 3, "quatre"]`
  - Accès aux éléments par index : `ma_liste`

- **Tuples** : Séquences ordonnées et immuables
  - Syntaxe : `mon_tuple = (1, 2, 3)`

- **Dictionnaires** : Collections de paires clé-valeur
  - Syntaxe : `mon_dict = {"nom": "Alice", "age": 30}`
  - Accès aux valeurs par clé : `mon_dict["nom"]`

## Vérification et conversion de types

- Fonction `type()` pour vérifier le type d'une variable
- Conversion entre types : `int()`, `float()`, `str()`, `bool()`

## Opérations spécifiques aux types

- Concaténation de chaînes : `"Hello" + " " + "World"`
- Opérations mathématiques sur les nombres
- Méthodes spécifiques pour les listes et dictionnaires

# Les listes en Python

## Définition et création

- Les listes sont des collections ordonnées et modifiables d'éléments
- Création avec des crochets : `ma_liste = [1, 2, 3, "quatre"]`
- Peuvent contenir différents types de données

## Accès aux éléments

- Utilisation d'index (commence à 0) : `ma_liste`
- Index négatifs pour accéder depuis la fin : `ma_liste[-1]`
- Slicing pour extraire des sous-listes : `ma_liste[1:3]`

## Modification des listes

- Ajout d'éléments : 
  - `append()` pour ajouter à la fin
  - `insert()` pour insérer à une position spécifique
- Suppression d'éléments :
  - `remove()` pour supprimer par valeur
  - `pop()` pour supprimer par index
- Modification d'un élément : `ma_liste[index] = nouvelle_valeur`

## Opérations sur les listes

- Concaténation : `liste1 + liste2`
- Répétition : `liste * n`
- Longueur d'une liste : `len(ma_liste)`

## Méthodes utiles

- `sort()` pour trier la liste
- `reverse()` pour inverser l'ordre
- `count()` pour compter les occurrences d'un élément
- `index()` pour trouver l'index d'un élément

## Itération sur les listes

- Utilisation de boucles `for` pour parcourir les éléments
- Exemple : `for element in ma_liste:`

# Les dictionnaires en Python

## Définition et création

- Les dictionnaires sont des collections non ordonnées de paires clé-valeur
- Création avec des accolades : `mon_dict = {"clé1": valeur1, "clé2": valeur2}`
- Les clés doivent être uniques et immuables (généralement des chaînes ou des nombres)

## Accès aux valeurs

- Utilisation des clés entre crochets : `mon_dict["clé1"]`
- Méthode `get()` pour un accès sécurisé : `mon_dict.get("clé1", valeur_par_défaut)`

## Modification des dictionnaires

- Ajout ou modification d'une paire clé-valeur : `mon_dict["nouvelle_clé"] = nouvelle_valeur`
- Suppression d'une paire : 
  - `del mon_dict["clé"]`
  - Méthode `pop()` pour supprimer et retourner la valeur

## Méthodes utiles

- `keys()` : retourne toutes les clés
- `values()` : retourne toutes les valeurs
- `items()` : retourne toutes les paires clé-valeur
- `update()` : fusionne deux dictionnaires

## Itération sur les dictionnaires

- Parcourir les clés : `for clé in mon_dict:`
- Parcourir les valeurs : `for valeur in mon_dict.values():`
- Parcourir les paires clé-valeur : `for clé, valeur in mon_dict.items():`

## Dictionnaires imbriqués

- Possibilité de créer des structures de données complexes
- Exemple : `utilisateurs = {"user1": {"nom": "Alice", "age": 30}, "user2": {"nom": "Bob", "age": 25}}`

## Cas d'utilisation

- Stockage de données structurées
- Représentation d'objets avec attributs
- Optimisation des performances pour la recherche de données

# Contrôle du déroulement avec des conditions en Python

## Instruction if

- Permet d'exécuter du code si une condition est vraie
- Syntaxe de base :
  ```python
  if condition:
      # code à exécuter si la condition est vraie
  ```

## Instruction else

- S'exécute si la condition du if est fausse
- Syntaxe :
  ```python
  if condition:
      # code si vrai
  else:
      # code si faux
  ```

## Instruction elif

- Permet de vérifier plusieurs conditions
- Syntaxe :
  ```python
  if condition1:
      # code si condition1 est vraie
  elif condition2:
      # code si condition2 est vraie
  else:
      # code si aucune condition n'est vraie
  ```

## Opérateurs de comparaison

- `==` (égal à)
- `!=` (différent de)
- `<` (inférieur à)
- `>` (supérieur à)
- `<=` (inférieur ou égal à)
- `>=` (supérieur ou égal à)

## Opérateurs logiques

- `and` (et logique)
- `or` (ou logique)
- `not` (négation)

## Bonnes pratiques

- Indenter correctement le code dans les blocs conditionnels
- Utiliser des parenthèses pour clarifier les conditions complexes
- Éviter les conditions imbriquées trop profondes pour maintenir la lisibilité

# Les boucles en Python

## Boucle for

- Utilisée pour itérer sur une séquence (liste, chaîne, etc.)
- Syntaxe de base :
  ```python
  for element in sequence:
      # code à exécuter pour chaque élément
  ```
- Exemple avec `range()` pour générer une séquence de nombres :
  ```python
  for i in range(5):
      print(i)  # Affiche les nombres de 0 à 4
  ```

## Boucle while

- Exécute un bloc de code tant qu'une condition est vraie
- Syntaxe :
  ```python
  while condition:
      # code à exécuter tant que la condition est vraie
  ```
- Attention aux boucles infinies, assurez-vous que la condition devient fausse à un moment donné

## Contrôle de boucle

- `break` : sort immédiatement de la boucle
- `continue` : passe à l'itération suivante
- `else` avec les boucles : s'exécute si la boucle se termine normalement (sans `break`)

## Boucles imbriquées

- Possibilité de placer une boucle à l'intérieur d'une autre
- Utile pour travailler avec des structures de données multidimensionnelles

## Compréhensions de liste

- Méthode concise pour créer des listes basées sur des séquences existantes
- Syntaxe : `[expression for item in iterable if condition]`
- Exemple :
  ```python
  carres = [x**2 for x in range(10) if x % 2 == 0]
  ```

## Bonnes pratiques

- Évitez les boucles trop complexes ou trop imbriquées
- Utilisez des noms de variables significatifs dans les boucles
- Préférez les boucles `for` aux boucles `while` quand c'est possible
- Utilisez les compréhensions de liste pour un code plus concis et lisible

# Les fonctions en Python

## Définition d'une fonction

- Utilisation du mot-clé `def`
- Syntaxe de base :
  ```python
  def nom_fonction(parametre1, parametre2):
      # corps de la fonction
      return resultat
  ```

## Paramètres et arguments

- Les paramètres sont définis lors de la déclaration de la fonction
- Les arguments sont les valeurs passées lors de l'appel de la fonction
- Paramètres par défaut : `def fonction(param=valeur_par_defaut)`
- Arguments nommés : `fonction(param1=valeur1, param2=valeur2)`

## Retour de valeurs

- Utilisation du mot-clé `return`
- Possibilité de retourner plusieurs valeurs : `return valeur1, valeur2`

## Portée des variables

- Variables locales : définies à l'intérieur de la fonction
- Variables globales : définies en dehors des fonctions
- Mot-clé `global` pour modifier une variable globale dans une fonction

## Fonctions lambda

### Définition et syntaxe

Les fonctions lambda sont des fonctions anonymes et concises en Python. Leur syntaxe est :

```python
lambda arguments: expression
```

### Caractéristiques principales

- Fonctions anonymes (sans nom)
- Limitées à une seule expression
- Peuvent avoir plusieurs arguments mais une seule expression
- Retournent automatiquement le résultat de l'expression

### Utilisations courantes

1. Avec les fonctions d'ordre supérieur=:
   - `map()`: 
     ```python
     list(map(lambda x: x * 2, [1, 2, 3, 4, 5]))
     ```
   - `filter()`:
     ```python
     list(filter(lambda x: x % 2 == 0, [1, 2, 3, 4, 5, 6, 7, 8, 9]))
     ```
   - `sorted()`:
     ```python
     sorted([(1, 5), (3, 2), (8, 10)], key=lambda x: x[1])
     ```

2. Pour des opérations simples et ponctuelles

3. Comme arguments de fonction

### Alternative moderne

Les compréhensions de liste sont souvent préférées aux lambdas avec `map()` et `filter()` pour une meilleure lisibilité:

```python
[x * 2 for x in [1, 2, 3, 4, 5]]  # Équivalent à map()
[x for x in [1, 2, 3, 4, 5, 6, 7, 8, 9] if x % 2 == 0]  # Équivalent à filter()
```

## Docstrings

### Définition et utilisation

- Les docstrings sont des chaînes de caractères placées juste après la définition d'une fonction, méthode, classe ou module.
- Elles servent à documenter le code de manière standardisée.
- Elles sont accessibles via l'attribut `__doc__` ou la fonction `help()`.

### Syntaxe

- Utilisation de triples guillemets : `"""` ou `'''`
- Placées immédiatement après la définition, sans ligne vide

### Types de docstrings

1. Docstring sur une ligne :
   ```python
   def fonction():
       """Description courte de la fonction."""
   ```

2. Docstring multi-lignes :
   ```python
   def fonction():
       """
       Description plus détaillée.

       Arguments:
       Retours:
       """
   ```

### Bonnes pratiques

- Commencer par une ligne résumant brièvement l'objet
- Décrire les paramètres, valeurs de retour et exceptions levées
- Utiliser un style cohérent (ex: style Google, NumPy ou reStructuredText)
- Inclure des exemples d'utilisation si pertinent

### Avantages

- Améliore la lisibilité et la maintenabilité du code
- Permet de générer automatiquement de la documentation
- Facilite l'utilisation des fonctions/classes par d'autres développeurs

### Outils

- Peuvent être utilisées par des outils comme Sphinx pour générer de la documentation
- Utilisées par les IDE pour fournir de l'aide contextuelle

# Importation des packages Python

## Concepts de base

- Un package est un ensemble de modules Python
- Les modules sont des fichiers Python contenant du code réutilisable

## Types d'importations

1. Import complet :
   ```python
   import nom_du_module
   ```

2. Import avec alias :
   ```python
   import nom_du_module as alias
   ```

3. Import de fonctions ou classes spécifiques :
   ```python
   from nom_du_module import fonction1, fonction2
   ```

4. Import de tout le contenu d'un module :
   ```python
   from nom_du_module import *
   ```
   (à utiliser avec précaution)

## Packages standards vs tiers

- Packages standards : inclus avec Python (ex: `math`, `os`, `datetime`)
- Packages tiers : installés via pip (ex: `numpy`, `pandas`, `requests`)

## Installation de packages tiers

- Utilisation de pip :
  ```
  pip install nom_du_package
  ```

## Bonnes pratiques

- Placer les imports en haut du fichier
- Grouper les imports : standards, tiers, locaux
- Éviter les imports circulaires
- Préférer les imports explicites aux imports généraux (`import *`)

## Gestion des dépendances

### Installation des dépendances

- Installation simple : `pip install nom_package`
- Installation avec version spécifique : `pip install nom_package==1.2.3`
- Installation avec contrainte de version : `pip install "nom_package>=1.2,<2.0"`

### Fichier requirements.txt

- Liste les dépendances du projet
- Format : une dépendance par ligne
- Exemple :
  ```
  requests==2.25.1
  numpy>=1.18.0,<2.0.0
  pandas
  ```
- Installation : `pip install -r requirements.txt`

### Résolution des dépendances

- Pip résout automatiquement les dépendances transitives
- En cas de conflit, pip tente de trouver une combinaison compatible
- Utilise un algorithme de backtracking pour explorer les possibilités

### Gestion des versions

- Pip installe la dernière version compatible par défaut
- Utilisation de spécificateurs de version pour contrôler les versions installées :
  - `==` : version exacte
  - `>=`, `<=`, `>`, `<` : comparaisons
  - `~=` : compatible release
  - `!=` : exclusion de version

### Environnements virtuels

- Isolent les dépendances par projet
- Création : `python -m venv nom_env`
- Activation : 
  - Windows : `nom_env\Scripts\activate`
  - Unix : `source nom_env/bin/activate`

### Outils avancés

1. `pip-tools` : 
   - Génère `requirements.txt` à partir de `requirements.in`
   - Assure la reproductibilité des installations

2. `pipdeptree` : 
   - Affiche l'arbre des dépendances
   - Aide à identifier les conflits

3. `pip-compile` (partie de pip-tools) :
   - Crée un fichier de dépendances verrouillées

### Bonnes pratiques

1. Utiliser des environnements virtuels pour chaque projet
2. Spécifier les versions précises dans `requirements.txt`
3. Mettre à jour régulièrement les dépendances
4. Utiliser `pip freeze > requirements.txt` pour capturer l'état exact de l'environnement
5. Vérifier les incompatibilités avec `pip check`

### Limitations de pip

- Ne gère pas automatiquement les conflits de dépendances
- Peut installer plusieurs versions d'une même dépendance
- Pas de désinstallation automatique des dépendances non utilisées

## Création de packages

- Structure de répertoires avec `__init__.py`
- Utilisation de `setuptools` pour la distribution

### Définition d'un package

Un package est un moyen d'organiser des modules Python connexes dans un répertoire. Il permet de structurer de grands projets en regroupant des modules liés.

### Structure de base d'un package

1. Créez un répertoire avec le nom de votre package
2. À l'intérieur, créez un fichier `__init__.py` (peut être vide)
3. Ajoutez vos modules Python (.py) dans ce répertoire

Exemple de structure :
```
mon_package/
    __init__.py
    module1.py
    module2.py
```

### Le fichier __init__.py

- Indique à Python que le répertoire doit être traité comme un package
- Peut être vide ou contenir du code d'initialisation
- Peut définir quels modules sont exportés lors de l'importation du package

### Création de sous-packages

Vous pouvez créer des sous-packages en ajoutant des sous-répertoires, chacun avec son propre `__init__.py`.

### Importation et utilisation

- Import du package entier : `import mon_package`
- Import d'un module spécifique : `from mon_package import module1`
- Import d'une fonction spécifique : `from mon_package.module1 import ma_fonction`

### Bonnes pratiques

1. Utilisez des noms descriptifs pour vos packages et modules
2. Évitez les conflits de noms avec des modules Python standards
3. Incluez une documentation dans le `__init__.py`
4. Utilisez des imports relatifs dans les sous-packages

### Distribution du package

1. Créez un fichier `setup.py` à la racine de votre projet
2. Utilisez `setuptools` pour définir les métadonnées et les dépendances
3. Créez un fichier `README.md` pour décrire votre package
4. Utilisez `pip` pour construire et distribuer votre package

### Exemple de setup.py basique

```python
from setuptools import setup, find_packages

setup(
    name="mon_package",
    version="0.1",
    packages=find_packages(),
    install_requires=[
        'dependance1',
        'dependance2',
    ],
)
```

### Publication sur PyPI

1. Créez un compte sur PyPI
2. Utilisez `twine` pour téléverser votre package :
   ```
   python setup.py sdist bdist_wheel
   twine upload dist/*
   ```

# Extraction et transformation de données avec l'extraction web en Python

## Introduction à l'extraction web

- L'extraction web (web scraping) permet de collecter automatiquement des données à partir de sites web
- Utilisée pour la veille concurrentielle, l'analyse de marché, la recherche, etc.
- Nécessite de respecter les conditions d'utilisation des sites web et les aspects légaux

## Outils pour l'extraction web en Python

1. **Requests** : bibliothèque pour envoyer des requêtes HTTP
   - Installation : `pip install requests`
   - Utilisation basique :
     ```python
     import requests
     response = requests.get('https://example.com')
     print(response.text)
     ```

2. **Beautiful Soup** : bibliothèque pour analyser le HTML et XML
   - Installation : `pip install beautifulsoup4`
   - Utilisation basique :
     ```python
     from bs4 import BeautifulSoup
     soup = BeautifulSoup(response.content, 'html.parser')
     ```

## Processus d'extraction web

1. Envoi d'une requête HTTP au site web
2. Réception de la réponse HTML
3. Analyse du HTML avec Beautiful Soup
4. Extraction des données souhaitées

## Exemple pratique

Extraction des titres d'articles d'un blog :

```python
import requests
from bs4 import BeautifulSoup

url = 'https://example-blog.com'
response = requests.get(url)
soup = BeautifulSoup(response.content, 'html.parser')

titles = soup.find_all('h2', class_='post-title')
for title in titles:
    print(title.text.strip())
```

## Bonnes pratiques

- Respectez les robots.txt des sites web
- Ajoutez des délais entre les requêtes pour ne pas surcharger les serveurs
- Identifiez-vous auprès du site web (user-agent)
- Utilisez des sessions pour gérer les cookies si nécessaire

## Limitations et considérations

- Certains sites web peuvent bloquer les robots d'extraction
- Les structures HTML peuvent changer, nécessitant une maintenance du code
- L'extraction à grande échelle peut nécessiter des techniques plus avancées (ex: proxies, parallélisation)

# Chargement de données avec Python

## Types de données couramment chargés

1. Fichiers texte (.txt)
2. Fichiers CSV (Comma-Separated Values)
3. Fichiers JSON (JavaScript Object Notation)
4. Fichiers Excel (.xlsx)
5. Bases de données SQL

## Lecture de fichiers texte

```python
with open('fichier.txt', 'r') as file:
    contenu = file.read()
```

## Chargement de données CSV

Utilisation du module `csv` :

```python
import csv

with open('donnees.csv', 'r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

Ou avec pandas pour des fonctionnalités plus avancées :

```python
import pandas as pd

df = pd.read_csv('donnees.csv')
```

## Chargement de données JSON

```python
import json

with open('donnees.json', 'r') as file:
    data = json.load(file)
```

## Lecture de fichiers Excel

Utilisation de pandas :

```python
import pandas as pd

df = pd.read_excel('donnees.xlsx', sheet_name='Feuille1')
```

## Connexion à une base de données SQL

Exemple avec SQLite :

```python
import sqlite3

conn = sqlite3.connect('ma_base.db')
cursor = conn.cursor()
cursor.execute("SELECT * FROM ma_table")
resultats = cursor.fetchall()
conn.close()
```


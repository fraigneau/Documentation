
## Types de variables

### Types primitifs

Java offre 8 types primitifs :

- `boolean` : true ou false
- `byte` : -128 à 127
- `char` : un caractère unique
- `double` : nombre à virgule flottante double précision
- `float` : nombre à virgule flottante simple précision
- `int` : entier de -2^31 à 2^31-1
- `long` : entier de -2^64 à 2^64-1
- `short` : entier de -32,768 à 32,767

### Types complexes

Les types complexes, basés sur le paradigme de programmation orientée objet, permettent de créer des ensembles de données personnalisés[1].

	### Déclaration et initialisation

La syntaxe de base pour déclarer une variable est :

```java
type nomVariable;
```

Pour initialiser une variable lors de sa déclaration :

```java
type nomVariable = valeur;
```

### Tableaux

Les tableaux permettent de stocker plusieurs valeurs du même type :

```java
int[] tableau = {5, 10, 15, 20};
```

On peut accéder aux éléments d'un tableau par leur index :

```java
tableau[0]; // Renvoie 5
```

### Mot-clé var

Depuis Java 10, le mot-clé `var` permet d'omettre le type lors de la déclaration d'une variable :

```java
var nombre = 5; // Le compilateur déduit que c'est un int
```

Il est recommandé d'utiliser `var` avec précaution et de donner des noms explicites aux variables pour maintenir la lisibilité du code[1].


## Introduction aux Fonctions

Une fonction en Java est une suite d'instructions organisée en un traitement, comprenant :

1. **Visibilité** : La portée de la fonction (ex. `public`).
2. **Caractéristique** : Options comme `static`, `final`, etc.
3. **Type de Retour** : Le type de donnée retourné (ou `void` pour aucune valeur).
4. **Nom** : Nom sémantique en camelCase.
5. **Paramètres** : Données en entrée.

### Exemple de Fonction Simple
```java
public static void affiche() {
    System.out.println("Une fonction en Java a été exécutée");
}
```
## Fonction conditionnelle 

### Instruction if-else

L'instruction `if-else` permet d'exécuter du code en fonction d'une condition :

```java
if (condition) {
    // Code exécuté si la condition est vraie
} else {
    // Code exécuté si la condition est fausse
}
```

On peut utiliser des opérateurs de comparaison comme `==`, `!=`, `>`, `<`, etc. Pour les chaînes de caractères, il faut utiliser la méthode `equals()`[1].

### Switch

La structure `switch` permet de vérifier plusieurs cas possibles :

```java
switch (expression) {
    case valeur1 -> instruction1;
    case valeur2 -> instruction2;
    default -> instructionParDefaut;
}
```

### Boucle while

La boucle `while` exécute un bloc de code tant qu'une condition est vraie :

```java
while (condition) {
    // Code à répéter
}
```

### Boucle do-while

La boucle `do-while` garantit l'exécution du code au moins une fois :

```java
do {
    // Code à répéter
} while (condition);
```

### Boucle for

La boucle `for` est utilisée pour un nombre connu d'itérations :

```java
for (initialisation; condition; incrémentation) {
    // Code à répéter
}
```

### Boucle for-each

La boucle `for-each` permet de parcourir facilement les éléments d'une collection :

```java
for (Type element : collection) {
    // Code à exécuter pour chaque élément
}
```

Ce chapitre d'OpenClassrooms introduit les concepts fondamentaux de la programmation orientée objet (POO) en Java. Voici un résumé des points clés :

## Programmation orientée objet

La POO permet de résoudre plusieurs problématiques de développement logiciel :
- Représenter le monde réel dans le programme
- Faciliter la modification du code sans effets de bord
- Permettre l'ajout de nouvelles fonctionnalités sans impacter l'existant

### Classes et objets

Une classe est un "plan" qui définit la structure d'un objet, comprenant :
- Des attributs (variables de classe)
- Des méthodes (fonctions de classe)

### Instanciation et constructeurs

L'instanciation crée un objet à partir d'une classe :

```java
Bloc unBloc = new Bloc();
```

Le constructeur est une méthode spéciale appelée lors de l'instanciation. On peut créer des constructeurs paramétrés pour initialiser les attributs.

### Encapsulation

L'encapsulation protège l'intégrité des objets en contrôlant l'accès à leurs attributs et méthodes :

- `public` : accessible de partout
- `private` : accessible uniquement dans la classe

Il est recommandé de déclarer les attributs en `private` et d'utiliser des getters et setters pour y accéder :

```java
public class Bloc {
    private String description;
    
    public String getDescription() {
        return this.description;
    }
    
    public void setDescription(String description) {
        this.description = description;
    }
}
```

## Héritage en programmation orientée objet

L'héritage permet à une classe fille d'hériter des attributs et méthodes d'une classe mère. Cela favorise la réutilisation du code et évite la duplication.

**Principaux points :**

- Utilisation du mot-clé `extends` pour définir l'héritage
- Visibilité `protected` pour permettre l'accès aux classes filles
- Mot-clé `super` pour accéder aux éléments de la classe mère
- Toutes les classes héritent implicitement de la classe `Object`

### Polymorphisme 

Le polymorphisme permet à un objet de se présenter sous différentes formes.

**Deux types de polymorphisme :**

1. Polymorphisme à l'exécution (redéfinition de méthodes)
2. Polymorphisme à la compilation (surcharge de méthodes)

### Abstraction

L'abstraction s'applique aux classes et aux méthodes :

- Une classe abstraite ne peut pas être instanciée directement
- Une méthode abstraite n'a pas d'implémentation dans la classe où elle est définie

### Implémentation pratique

Le cours propose des exercices pour appliquer ces concepts au projet Epicraft's Journey :

1. Modifier la classe `Bloc` pour la rendre abstraite
2. Créer une classe `Mur` héritant de `Bloc`
3. Créer une classe `Porte` héritant de `Bloc`

## Interfaces

Les interfaces permettent d'appliquer des contrats aux classes :

- Définies avec le mot-clé `interface`
- Peuvent contenir des constantes (variables `public`, `static` et `final`)
- Contiennent des signatures de méthodes sans implémentation
- Les classes implémentent les interfaces avec le mot-clé `implements`

L'interface `IBloc` est créée pour contraindre les blocs à implémenter une méthode `afficherDescription()`.

### Injection de dépendances

Cette technique permet de réduire le couplage entre les classes :

- La classe dépendante utilise une interface plutôt qu'une classe concrète
- La dépendance est fournie via le constructeur ou un mutateur
- Exemple : la classe `Rempart` dépend de l'interface `IBloc` au lieu de la classe `Bloc`

### Records

Introduits dans Java 16, les records simplifient la création de classes de données :

- Syntaxe concise : `public record Planete(String nom, double perimetre, int superficie) { }`
- Génère automatiquement constructeur, accesseurs, et méthodes utilitaires
- Sont finaux et immuables
- Peuvent implémenter des interfaces et définir des méthodes supplémentaires

### Énumérations (Enums)

Les enums sont utiles pour représenter un ensemble fixe de constantes :

```java
public enum Couleur {
    BLEU, VERT, GRIS, MARRON, NOIR
}
```

- Permettent une utilisation type-safe dans les switch statements
- Plus concises et pratiques que des constantes statiques

## Collections en Java

Les collections sont des objets permettant de gérer des ensembles d'éléments. Elles offrent une alternative plus flexible et puissante que les tableaux classiques.

### Types de collections

#### List
- Permet de manipuler des listes d'éléments
- Autorise les doublons
- Exemple d'implémentation : ArrayList

```java
List<Integer> quantiteBlocsUtilises = new ArrayList<>();
quantiteBlocsUtilises.add(1);
quantiteBlocsUtilises.add(3);
quantiteBlocsUtilises.add(1); // doublon autorisé
```

#### Set
- Gère des ensembles d'éléments uniques
- N'autorise pas les doublons
- Exemple d'implémentation : LinkedHashSet

```java
Set<String> motsCles = new LinkedHashSet<>();
motsCles.add("Cabane");
motsCles.add("Cabane"); // Ce doublon sera ignoré
motsCles.add("Muraille");
```

#### Map
- Manipule des associations clé-valeur
- Exemple d'implémentation : HashMap

```java
Map<Bloc, Integer> quantiteBloc = new HashMap<>();
quantiteBloc.put(new Mur(1,1,1,true), 4);
quantiteBloc.put(new Porte(1,1,1,false), 1);
```

### Méthodes communes

- `add()` : Ajoute un élément (List, Set)
- `put()` : Ajoute une paire clé-valeur (Map)
- `remove()` : Supprime un élément
- `get()` : Récupère un élément (par index pour List, par clé pour Map)
- `contains()` : Vérifie la présence d'un élément

### Application au projet Epicrafter's Journey

Pour implémenter la classe Kit, on peut utiliser :

- Une List pour gérer les blocs
- Un Set pour les mots-clés

```java
public class Kit {
    private List<Bloc> blocs;
    private Set<String> motsClés;

    public Kit() {
        this.blocs = new ArrayList<>();
        this.motsClés = new LinkedHashSet<>();
    }

    // Méthodes pour ajouter des blocs et des mots-clés
}
```

## Découverte des exceptions

Les exceptions sont des objets représentant des erreurs qui peuvent survenir lors de l'exécution du programme. La classe de base pour les exceptions est `java.lang.Exception`.

### Gestion des exceptions

Pour gérer les exceptions, on utilise les blocs `try` et `catch` :

```java
try {
    // Code susceptible de générer une exception
} catch (ExceptionType e) {
    // Code pour gérer l'exception
}
```

Cette structure permet d'anticiper les erreurs potentielles et d'y répondre de manière appropriée, améliorant ainsi l'expérience utilisateur[1].

### Levée d'exceptions

Les développeurs peuvent également déclencher leurs propres exceptions pour gérer des situations spécifiques :

```java
if (condition) {
    throw new IllegalArgumentException();
}
```

### Création d'exceptions personnalisées

Il est possible de créer des exceptions spécifiques en étendant la classe `Exception` :

```java
public class IllegalBlocException extends Exception {
    // Implémentation de l'exception personnalisée
}
```

### Déclaration d'exceptions

Certaines exceptions doivent être déclarées dans la signature de la méthode qui peut les lever :

```java
public void methode() throws IllegalBlocException {
    // Code pouvant lever IllegalBlocException
}
```

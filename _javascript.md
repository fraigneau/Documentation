## Déclaration de variables en JavaScript

### L'instruction let

- Syntaxe : `let nomVariable = valeur`
- Exemple : `let monAge = 42`
- La valeur peut être modifiée ultérieurement.

### L'instruction const

- Syntaxe : `const nomVariable = valeur`
- Exemple : `const monPrenom = "David"`
- La valeur ne peut pas être modifiée après déclaration.

### L'instruction console.log()

- Utilisée pour vérifier le contenu d'une variable.
- Syntaxe : `console.log(nomVariable)`

## Bonnes pratiques de codage

- Nommer les variables de manière descriptive et précise.
- Donner du sens aux noms des variables pour améliorer la lisibilité du code.

## Types de données de base

1. **string** : chaîne de caractères (texte)
2. **number** : chiffre
3. **boolean** : valeur vraie (true) ou fausse (false)

## Opérateurs pour modifier les variables

### Opérateurs d'affectation
Raccourci pour modifier une variable :
```javascript
placesDejaVendues += 10  // Équivalent à placesDejaVendues = placesDejaVendues + 10
```
Voici un résumé du chapitre sur la structuration des données avec les objets en JavaScript :

## Déclaration d'un objet

- Utilisation des accolades `{ }`
- Propriétés définies par paires nom:valeur
- Propriétés séparées par des virgules

Exemple :
```javascript
let monPersonnage = {
  nom: "Wayne",
  prenom: "Bruce",
  age: 35,
  couleurPreferee: "noir",
  hobbies: "sortir la nuit"
};
```

## Ajout d'une propriété à un objet

Syntaxe : `nomObjet.nouvelleProprieté = valeur`

Exemple :
```javascript
monPersonnage.vehiculePrefere = "Batmobile";
```

## Accès à une propriété d'un objet

Utilisation du point `.` pour accéder aux valeurs

Exemple :
```javascript
const nomDeMonPersonnage = monPersonnage.nom;
console.log(nomDeMonPersonnage);
```

## Découverte des tableaux

- Les tableaux permettent de regrouper plusieurs données similaires ou partageant la même thématique.
- Ils limitent le nombre de variables dans le code.

## Déclaration d'un tableau

- Utilisation des crochets `[ ]`
- Valeurs séparées par des virgules
- Exemple : `const maCollectionDeFilms = ["Titanic", "Jurassic Park", "Le Seigneur des Anneaux"]`

## Manipulation des tableaux

1. Accès aux éléments : 
   - Utilisation de l'index (commence à 0)
   - Exemple : `let premierFilmDuTableau = maCollectionDeFilms`

2. Compter les éléments :
   - Propriété `length`
   - Exemple : `const nombreDeFilms = maCollectionDeFilms.length`

3. Ajout d'éléments :
   - Méthode `push()`
   - Exemple : `mesFilms.push("Retour vers le futur")`

4. Suppression du dernier élément :
   - Méthode `pop()`
   - Exemple : `mesFilms.pop()`

## Copie de tableaux

- Copie par référence pour les tableaux (et objets)
- Pour une vraie copie indépendante : `let nouveauTableau = [...ancienTableau]`

## Structure conditionnelle if / else

Syntaxe de base :
```javascript
if (condition) {
    // Code exécuté si la condition est vraie
} else {
    // Code exécuté si la condition est fausse
}
```

## Types de tests

1. Avec des booléens :
   ```javascript
   let motTapeOk = true
   if (motTapeOk) {
       console.log("Bravo, vous avez correctement tapé le mot")
   }
   ```

2. Avec des opérateurs de comparaison :
   ```javascript
   if (motUtilisateur === motApplication) {
       console.log("Bravo !")
   }
   ```

## Structure conditionnelle switch/case

Utilisée pour gérer plusieurs réponses possibles :
```javascript
switch (motUtilisateur) {
    case motApplication:
        console.log("Bravo !")
        break
    case "Gredin":
    case "Mécréant":
        console.log("Restez correct !")
        break
    default:
        console.log("Vous avez fait une erreur de frappe.")
}
```

## Types de boucles

### Boucle for

- Utilisée quand on connaît à l'avance le nombre de répétitions.
- Syntaxe :
  ```javascript
  for (let compteur = 0; compteur < 3; compteur++) {
    // Code à répéter
  }
  ```
- Trois parties : initialisation, condition d'arrêt, incrémentation.

### Boucle while

- Utilisée quand le nombre de répétitions n'est pas connu à l'avance.
- Syntaxe :
  ```javascript
  let i = 0;
  while (i < 3) {
    // Code à répéter
    i++;
  }
  ```
- Continue tant que la condition est vraie.

## Rédaction d'une fonction

Syntaxe de base :
```javascript
function nomDeLaFonction(parametre1, parametre2) {
    // Code de la fonction
    return resultat;
}
```

## Introduction aux fonctions

- Les fonctions permettent d'organiser et de réutiliser le code, ce qui est essentiel à mesure que le projet grandit.
- Exemple d'utilisation d'une fonction : `motUtilisateur = prompt('Entrez un mot')`, où `prompt` est une fonction qui prend un paramètre et retourne un résultat.

## Rédaction d'une fonction

- Exemple de fonction pour générer un message de score :
  ```javascript
  function retournerMessageScore(score, nombreQuestions) {
      let message = 'Votre score est de ' + score + ' sur ' + nombreQuestions;
      return message;
  }
  ```

### Éléments clés d'une fonction

- Utilisation du mot-clé `function` suivi du nom de la fonction.
- Les paramètres sont définis entre parenthèses.
- Le code à exécuter est placé entre accolades.
- La fonction peut retourner une valeur avec le mot-clé `return`.

## Organisation du code

- Séparer le code en plusieurs fichiers améliore la lisibilité et la maintenance.
- Exemple d'inclusion de fichiers dans HTML :
  ```html
  <script src="config.js"></script>
  <script src="script.js"></script>
  ```

## Portée des variables

- **Variables globales** : Déclarées en dehors des fonctions, accessibles partout.
- **Variables locales** : Déclarées à l'intérieur d'une fonction, accessibles uniquement dans cette fonction.

### Exemple de portée
```javascript
let monNombre = 1; // variable globale

function afficheUnNombre() {
    let monNombreLocal = 2; // variable locale
    console.log(monNombre); // accessible
    console.log(monNombreLocal); // accessible
}

afficheUnNombre();
console.log(monNombre); // accessible
console.log(monNombreLocal); // erreur, non accessible
```

## Étapes pratiques

1. **Créer des fonctions** : Définir des fonctions comme `afficherResultat`, `choisirPhrasesOuMots`, etc.
2. **Séparer le code en fichiers** : Créer un fichier `config.js` pour les données et un fichier principal pour l'appel des fonctions.


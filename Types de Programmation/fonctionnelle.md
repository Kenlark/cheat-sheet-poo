# Programmation Fonctionnelle

La programmation fonctionnelle, c'est une approche où on utilise des **fonctions** pour **transformer des données**. Contrairement à la programmation impérative (où on donne des instructions étape par étape), en fonctionnelle, on évite de modifier l'état du programme et on se concentre sur **les transformations des données**.

## Concepts clés :

1. **Fonction pure** :

- Une fonction est pure si elle retourne toujours la même valeur pour les mêmes entrées et n'a pas d'effet secondaire (elle ne modifie rien à l'extérieur).

**Exemple simple de fonction pure** :

```java
public int additionner(int a, int b) {
    return a + b;  // Ne modifie rien d'autre, juste une transformation
}
```

2. **Immuabilité** :

- Les données ne changent jamais. Quand on veut modifier quelque chose, on crée une nouvelle version de cette donnée.

**Exemple avec une liste** :

```java
List<Integer> nombres = List.of(1, 2, 3);
List<Integer> nouveauxNombres = nombres.stream().map(x -> x * 2).collect(Collectors.toList());
// La liste 'nombres' reste inchangée, 'nouveauxNombres' contient [2, 4, 6]
```

**Exemple simple en Java** :

Doubler chaque nombre d'une liste, en utilisant une approche fonctionnelle. Voici un exemple avec les Streams (Java permet d’écrire du code fonctionnel avec ça).

```java
import java.util.List;
import java.util.stream.Collectors;

public class ExempleSimple {
    public static void main(String[] args) {
        // Liste d'exemples
        List<Integer> nombres = List.of(1, 2, 3, 4, 5);

        // Doubler chaque nombre de la liste avec un stream
        List<Integer> nombresDoubles = nombres.stream()      // Crée un stream des éléments
                                               .map(x -> x * 2) // Applique une fonction (ici, doubler)
                                               .collect(Collectors.toList()); // Collecte le résultat

        // Affiche la nouvelle liste
        System.out.println(nombresDoubles);  // [2, 4, 6, 8, 10]
    }
}
```

**Explication** :

- `map(x -> x * 2)` : C'est une fonction qui transforme chaque élément de la liste en son double.

- `stream()` permet de traiter les éléments de la liste de manière fonctionnelle, un par un.

- **Immuabilité** : La liste nombres reste inchangée. Une nouvelle liste nombresDoubles est créée.

**Résumé** :

- En programmation fonctionnelle, on utilise des fonctions pour transformer des données.

- Les données ne changent jamais, elles sont immuables.

- On évite de modifier l'état du programme ou des variables.

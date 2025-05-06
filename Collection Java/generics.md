## Generics

Les Génériques permettent de spécifier le type des éléments d'une collection pour :

- Éviter les erreurs de cast
- Rendre le code plus lisible et sûr

```java
List<String> noms = new ArrayList<>();
noms.add("Jean");  // OK
noms.add(42);      // ❌ Erreur à la compilation
```

### Syntaxe

```java
List<String> noms = new ArrayList<>();
Map<Integer, String> map = new HashMap<>();
```

### Exemple avec méthode générique

```java
public class Utilitaire {

    public static <T> void afficherListe(List<T> liste) {
        for (T element : liste) {
            System.out.println(element);
        }
    }

    public static void main(String[] args) {
        List<Integer> nombres = List.of(1, 2, 3);
        List<String> noms = List.of("Ana", "Léo");

        afficherListe(nombres); // affiche : 1, 2, 3
        afficherListe(noms);    // affiche : Ana, Léo
    }
}
```

_Ici, `<T>` indique que la méthode fonctionne avec tout type (String, Integer, etc.), et Java déduit le type automatiquement lors de l’appel._

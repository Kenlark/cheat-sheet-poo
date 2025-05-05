# Constructeur

Un **constructeur** est une **méthode spéciale** utilisée pour **initialiser** un objet lorsqu'il est créé. Le constructeur a le même nom que la classe et ne retourne rien (pas même `void`).

- **Définition** : Un constructeur est utilisé pour initialiser un objet lorsqu'il est créé.

- **Syntaxe** :

```java
public class Personne {
    private String nom;
    private int age;

    // Constructeur
    public Personne(String nom, int age) {
        this.nom = nom;
        this.age = age;
    }
}
```

## Exemple d'utilisation :

```java
public class Main {
    public static void main(String[] args) {
        // Instanciation avec le constructeur
        Personne p = new Personne("Alice", 30);
    }
}
```

- Ici, le constructeur `Personne(String nom, int age)` permet d'initialiser les attributs `nom` et `age` lors de l'instanciation.

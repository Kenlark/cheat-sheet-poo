# Encapsulation

L'**encapsulation** est un principe clé de la POO qui consiste à **protéger les données internes** d'une classe en les rendant privées et à permettre l'accès via des **méthodes publiques** (getters et setters). Cela protège l'intégrité des données en limitant l'accès direct.

- **Définition** : L'encapsulation protège les données internes d'une classe et les expose uniquement via des méthodes contrôlées.

## Exemple d'encapsulation :

```java
public class Personne {
    private String nom;
    private int age;

    // Getter et Setter (accès contrôlé)
    public String getNom() {
        return nom;
    }

    public void setNom(String nom) {
        if (nom != null && !nom.isEmpty()) {  // Validation
            this.nom = nom;
        }
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age > 0) {  // Validation
            this.age = age;
        }
    }
}
```

- **Avantages de l'encapsulation** : Cela permet de protéger les données et de garantir que les valeurs restent dans des limites valides, évitant ainsi des erreurs dans le programme.

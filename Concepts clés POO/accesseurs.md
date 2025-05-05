# Accesseurs

Les **accesseurs** sont des **méthodes** qui permettent de **lire ou modifier** les valeurs des attributs d'une classe.

Les accesseurs incluent :

- **Les getters** : permettent de lire la valeur d'un attribut.

- **Les setters** : permettent de modifier la valeur d'un attribut.

- **Définition** : Un getter permet d'obtenir une valeur, tandis qu'un setter permet de modifier une valeur.

## Exemple avec un getter et un setter :

```java
public class Personne {
    private String nom;

    // Getter
    public String getNom() {
        return nom;
    }

    // Setter
    public void setNom(String nom) {
        this.nom = nom;
    }
}
```

## Utilisation :

```java
public class Main {
    public static void main(String[] args) {
        Personne p = new Personne();

        // Utilisation du setter
        p.setNom("Alice");

        // Utilisation du getter
        System.out.println(p.getNom());  // Affiche : Alice
    }
}
```

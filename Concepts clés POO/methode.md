# Méthode

Une **méthode** est un comportement ou une fonction définie à l'intérieur d'une classe. Elle permet à un objet d'exécuter une action, comme **modifier son état** ou **afficher des informations**.

- **Définition** : Une méthode est une action que l'objet peut effectuer.

```java
public class Personne {
    private String nom;
    private int age;

    // Méthode qui affiche un message
    public void direBonjour() {
        System.out.println("Bonjour, je m'appelle " + nom + " et j'ai " + age + " ans.");
    }
}
```

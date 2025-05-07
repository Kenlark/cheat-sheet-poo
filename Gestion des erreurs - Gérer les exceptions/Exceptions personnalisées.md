# Exceptions personnalisées

Parfois, les exceptions de Java ne suffisent pas. On peut créer nos propres exceptions pour mieux décrire une erreur spécifique à l'application.

Étapes :

1. Créer une classe qui hérite de `Exception` (ou `RuntimeException`)
2. Appeler le constructeur de la classe mère avec un message

**Exemple, vérifier si un utilisateur est majeur** :

```java
// Étape 1 : Créer l'exception personnalisée
public class AgeInvalideException extends Exception {
    public AgeInvalideException(String message) {
        super(message);
    }
}
```

```java
// Étape 2 : Utiliser cette exception dans une méthode
public class Verificateur {
    public static void verifierAge(int age) throws AgeInvalideException {
        if (age < 18) {
            throw new AgeInvalideException("Âge insuffisant : accès refusé.");
        }
    }
}
```

```java
// Étape 3 : Gérer l'exception dans le main
public class Main {
    public static void main(String[] args) {
        try {
            Verificateur.verifierAge(16);
        } catch (AgeInvalideException e) {
            System.out.println("Erreur : " + e.getMessage());
        }
    }
}
```

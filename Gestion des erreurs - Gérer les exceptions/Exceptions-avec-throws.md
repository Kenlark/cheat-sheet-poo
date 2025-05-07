# Exceptions avec throws

Quand une méthode peut provoquer une erreur mais ne veut pas la gérer elle-même, elle utilise le mot-clé `throws` pour déléguer la gestion de l’exception à celui qui l'appelle.

**Syntaxe** : :

```java
public void nomDeLaMéthode() throws TypeException {
    // Code qui peut lancer une exception
}
```

**Exemple** :

```java
public class Maths {
    public static int division(int a, int b) throws ArithmeticException {
        return a / b;
    }
}
```

```java
public class Main {
    public static void main(String[] args) {
        try {
            int resultat = Maths.division(10, 0);
            System.out.println("Résultat : " + resultat);
        } catch (ArithmeticException e) {
            System.out.println("Erreur : " + e.getMessage());
        }
    }
}
```

> `try-catch` : l’erreur est gérée immédiatement.

> `throws` : signale que l'erreur peut arriver, et laisses l'appelant décider quoi faire.

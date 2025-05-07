# Try/catch/finally

- `Try` : bloc où l'erreur peut se produire
- `Catch` : capture et gère l'exception
- `Finally` : toujours exécuté, qu'il y ait exception ou non (utile pour libérer des ressources)

**Exemple** :

```java

public class Division {
    public static int diviser(int a, int b) {
        if (b == 0) {
            throw new ArithmeticException("Division par zéro interdite !");
        }
        return a / b;
    }
}


public class ExempleTryCatch {
    public static void main(String[] args) {
        try {
            int resultat = Division.diviser(10, 0);
            System.out.println("Résultat: " + resultat);
        } catch (ArithmeticException e) {
            System.out.println("Erreur : " + e.getMessage());
        } finally {
            System.out.println("Bloc finally exécuté.");
        }
    }
}
```

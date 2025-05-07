# Utilisation des exceptions

Quand une opération peut échouer, **Java** lance une exception (`throw new Exception()`), que l'on peut ensuite capturer.

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
```

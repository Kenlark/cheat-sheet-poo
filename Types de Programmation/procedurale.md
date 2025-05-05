# Programmation Procédurale

La programmation procédurale est un sous-type de la programmation impérative.

**Définition** :

La **programmation procédurale** organise le code en procédures (ou **fonctions** ou **sous-programmes**). Ce style reste impératif, mais **structure mieux** les instructions en les regroupant sous forme de blocs réutilisables.

## Caractéristiques de la programmation procédurale :

- Basée sur des fonctions/procédures qui effectuent des tâches spécifiques.

- Facilite la réutilisation et la lisibilité du code.

- Suit toujours une exécution séquentielle, avec des conditions, des boucles et des variables globales ou locales.

- Ne repose pas sur des objets ou des classes (contrairement à la programmation orientée objet).

- **Exemple en Java (style procédural)** :

```java
public class ExempleProcedural {
    public static void main(String[] args) {
        int resultat = addition(5, 10);
        System.out.println("Résultat : " + resultat);
    }

    public static int addition(int a, int b) {
        return a + b;
    }
}
```

**Analyse** :

- `addition()` est une procédure (ou fonction) clairement définie.

- Le code est organisé et lisible, mais **sans objets** ou **classes métier**.

**En résumé** :

- **Procédural** = **impératif + structuration en fonctions.**

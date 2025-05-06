# Notions d'interface

Une interface est un contrat pur : elle définit un ensemble de méthodes sans implémentation (jusqu’à Java 7).

- En Java 8+, on peut ajouter :

  - des méthodes default (avec implémentation)

  - des méthodes static

  - des private methods internes (Java 9+)

## Objectifs

- Spécifier un comportement qu’une classe s’engage à respecter.

- Permettre une forme d’héritage multiple.

- Désolidariser les implémentations : on programme contre des interfaces, pas des classes concrètes.

**Exemple** :

```java
interface Volant {
    void voler();
}

class Oiseau implements Volant {
    public void voler() {
        System.out.println("Je vole avec des ailes.");
    }
}
```

## Héritage multiple via interfaces

```java
interface Nageur {
    void nager();
}

interface Chanteur {
    void chanter();
}

class Canard implements Nageur, Chanteur {
    public void nager() {
        System.out.println("Je nage sur l'eau.");
    }

    public void chanter() {
        System.out.println("Coin coin !");
    }
}
```

**Exemple avancé** :

```java
interface Connectable {
    void connecter();

    default void ping() {
        System.out.println("Ping en cours...");
    }
}
```

# Principes SOLID en Programmation Orientée Objet

Les principes SOLID sont cinq règles de conception qui facilitent la maintenance, la compréhension et l’évolutivité du code objet. Ces principes ont été formalisés par Robert C. Martin (Uncle Bob).

## Acronyme SOLID

| **Lettre** | **Principe**                    | **Traduction française**               |
| ---------- | ------------------------------- | -------------------------------------- |
| **S**      | Single Responsibility Principle | Principe de responsabilité unique      |
| **O**      | Open/Closed Principle           | Principe ouvert/fermé                  |
| **L**      | Liskov Substitution Principle   | Principe de substitution de Liskov     |
| **I**      | Interface Segregation Principle | Principe de ségrégation des interfaces |
| **D**      | Dependency Inversion Principle  | Principe d'inversion des dépendances   |

## S - Single Responsibility Principle (SRP)

> Une classe ne doit avoir qu'une seule responsabilité et donc une seule raison de changer.

✅ **Bon exemple** :

```java
public class Invoice {
    private double amount;

    public Invoice(double amount) {
        this.amount = amount;
    }

    public double calculateTax() {
        return amount * 0.2;
    }
}

public class InvoicePrinter {
    public void print(Invoice invoice) {
        System.out.println("Total with tax: " + invoice.calculateTax());
    }
}
```

> La classe `Invoice` calcule, `InvoicePrinter` affiche. Une responsabilité par classe.

❌ **Mauvais exemple** :

```java
public class Invoice {
    private double amount;

    public Invoice(double amount) {
        this.amount = amount;
    }

    public double calculateTax() {
        return amount * 0.2;
    }

    public void print() {
        System.out.println("Total with tax: " + calculateTax());
    }
}
```

> Ici, la classe `Invoice` a deux responsabilités : gestion des données et affichage.

## O — Open/Closed Principle (OCP)

> Une classe doit être ouverte à l’extension mais fermée à la modification.

✅ **Exemple avec `abstract class`** :

```java
public abstract class Shape {
    public abstract double area();
}

public class Circle extends Shape {
    private double radius;
    public Circle(double radius) { this.radius = radius; }
    public double area() { return Math.PI * radius * radius; }
}

public class Square extends Shape {
    private double side;
    public Square(double side) { this.side = side; }
    public double area() { return side * side; }
}

public class AreaCalculator {
    public double totalArea(List<Shape> shapes) {
        return shapes.stream().mapToDouble(Shape::area).sum();
    }
}
```

> La classe `AreaCalculator` n’a pas besoin d’être modifiée quand on ajoute de nouvelles formes.

## L — Liskov Substitution Principle (LSP)

> Une classe dérivée doit pouvoir remplacer sa classe de base sans altérer le comportement du programme.

✅ **Bon exemple** :

```java
public class Bird {
    public void fly() {
        System.out.println("Flying...");
    }
}

public class Sparrow extends Bird {}

public class BirdWatcher {
    public void watch(Bird bird) {
        bird.fly();
    }
}
```

❌ **Mauvais exemple** :

```java
public class Bird {
    public void fly() {
        System.out.println("Flying...");
    }
}

public class Ostrich extends Bird {
    @Override
    public void fly() {
        throw new UnsupportedOperationException("Ostrich can't fly");
    }
}
```

> `Ostrich` viole LSP car elle ne respecte pas les attentes de la classe de base.

## I — Interface Segregation Principle (ISP)

> Il vaut mieux plusieurs interfaces spécifiques qu'une interface générale.

✅ **Bon exemple** :

```java
public interface Workable {
    void work();
}

public interface Eatable {
    void eat();
}

public class Human implements Workable, Eatable {
    public void work() { System.out.println("Human working..."); }
    public void eat() { System.out.println("Human eating..."); }
}

public class Robot implements Workable {
    public void work() { System.out.println("Robot working..."); }
}
```

❌ **Mauvais exemple** :

```java
public interface Worker {
    void work();
    void eat();
}

public class Robot implements Worker {
    public void work() { System.out.println("Robot working..."); }
    public void eat() { throw new UnsupportedOperationException(); }
}
```

> `Robot` n’a pas besoin de manger, donc il ne devrait pas implémenter `eat()`.

## D — Dependency Inversion Principle (DIP)

> Les modules de haut niveau ne doivent pas dépendre de modules de bas niveau. Tous deux doivent dépendre d’abstractions.

✅ **Bon exemple** :

```java
public interface Database {
    void connect();
}

public class MySQLDatabase implements Database {
    public void connect() {
        System.out.println("Connected to MySQL");
    }
}

public class Application {
    private Database db;

    public Application(Database db) {
        this.db = db;
    }

    public void start() {
        db.connect();
    }
}
```

> Ici, `Application` dépend de l’interface `Database`, pas d’une implémentation spécifique.

❌ **Mauvais exemple** :

```java
public class MySQLDatabase {
    public void connect() {
        System.out.println("Connected to MySQL");
    }
}

public class Application {
    private MySQLDatabase db = new MySQLDatabase();
    public void start() {
        db.connect();
    }
}
```

> `Application` dépend directement de `MySQLDatabase`.

✅ Conclusion

Les principes **SOLID** permettent de :

- Réduire le couplage.
- Améliorer la maintenance du code.
- Faciliter les tests unitaires.
- Faire évoluer le système sans casse.

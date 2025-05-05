# Programmation orientée objet (POO)

**Définition** :

La **programmation orientée objet** est un paradigme qui organise le code autour **d'objets** : des entités qui regroupent **données** (attributs) et **comportements** (méthodes).

## Concepts fondamentaux de la POO :

| Concept           | Description                                                       |
| ----------------- | ----------------------------------------------------------------- |
| **Classe**        | Modèle (ou plan) pour créer des objets.                           |
| **Objet**         | Instance concrète d’une classe.                                   |
| **Encapsulation** | Cacher l’état interne d’un objet et le protéger via des méthodes. |
| **Héritage**      | Une classe peut hériter des propriétés/comportements d’une autre. |
| **Polymorphisme** | Même interface, comportements différents selon les objets.        |

**Exemple simple en Java** :

```java
// Classe
public class Personne {
    private String nom;
    private int age;

    public Personne(String nom, int age) {
        this.nom = nom;
        this.age = age;
    }

    public void afficherInfos() {
        System.out.println("Nom : " + nom);
        System.out.println("Âge : " + age);
        System.out.println("Bonjour " + nom + ", vous avez " + age + " ans.");
    }
}

// Programme principal
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez votre nom : ");
        String nom = scanner.nextLine();

        System.out.print("Entrez votre âge : ");
        int age = scanner.nextInt();

        Personne p = new Personne(nom, age);
        p.afficherInfos();

        scanner.close();
    }
}
```

| **Aspect**      | **Procédural**                | **Orienté Objet**                        |
| --------------- | ----------------------------- | ---------------------------------------- |
| Organisation    | Fonctions et données séparées | Fonctions (méthodes) et données ensemble |
| Réutilisabilité | Moins facile                  | Meilleure via héritage/polymorphisme     |
| Structure       | Fonctionnelle, linéaire       | Basée sur des objets, plus modulaire     |
| Exemple         | `addition(a, b)`              | `objet.addition()`                       |

**Avantages de la POO** :

- Code plus modulaire et réutilisable.

- Meilleure organisation pour des gros projets.

- Facilite la maintenance et l’extension du code.

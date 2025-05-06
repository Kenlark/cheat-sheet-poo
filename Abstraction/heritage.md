## Bilan sur l’Héritage

### 🔹 Définition

L’héritage est un mécanisme de la programmation orientée objet (POO) permettant à une classe (dite **classe fille**) de **reprendre les caractéristiques** (attributs + méthodes) d’une autre classe (dite **classe parente** ou **super-classe**).

> Permet la **réutilisation**, la **généralisation** et l’**extension** de comportements.

### Types d’Héritage

- **Simple** : une classe hérite d’une seule classe.
- **Multiple** (non supporté directement en Java, mais possible en C++ ou via interfaces en Java).
- **Hiérarchique** : plusieurs classes héritent d’une même super-classe.
- **Multiniveau** : héritage en chaîne (classeA → classeB → classeC).

### Exemple concret en Java

```java
class Animal {
    String nom;

    void manger() {
        System.out.println("Je mange.");
    }
}

class Chien extends Animal {
    void aboyer() {
        System.out.println("Wouf !");
    }
}

// Utilisation
Chien c = new Chien();
c.manger();   // hérité
c.aboyer();   // spécifique à Chien
```

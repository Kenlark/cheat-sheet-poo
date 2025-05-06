## 3. Notion de Classes Abstraites

### Définition

Une **classe abstraite** est une classe **incomplète** qui sert de **modèle de base**.  
Elle peut contenir :

- des **méthodes abstraites** (sans corps)
- des **méthodes concrètes**
- des **attributs**

Elle **ne peut pas être instanciée**.

### Objectifs

- **Imposer une structure** à toutes les classes qui en héritent.
- Fournir une **implémentation partielle** commune.
- Favoriser le **polymorphisme** (traiter différents objets via leur type abstrait).

### Syntaxe en Java

```java
abstract class Animal {
    abstract void crier();     // à implémenter par les enfants
    void respirer() {
        System.out.println("Je respire.");
    }
}
```

```java
class Chien extends Animal {
    @Override
    void crier() {
        System.out.println("Wouf !");
    }
}
```

```java
 Animal monChien = new Chien();
        monChien.crier();     // Affiche: Wouf !
        monChien.respirer();  // Affiche: Je respire.
```

- @Override est une annotation Java utilisée pour indiquer qu'une méthode redéfinit (override) une méthode héritée d'une classe parente ou d'une interface.

**Son rôle** :

- Avertir le compilateur : « cette méthode doit exister dans la super-classe ou interface ».

- Empêcher les erreurs de frappe ou de signature silencieuses.

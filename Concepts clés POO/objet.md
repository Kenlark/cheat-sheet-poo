# Objet

Un **objet** est une instance d'une classe. Lorsqu'on crée un objet à partir d'une classe, on utilise ce modèle pour créer une entité réelle en mémoire.

- **Définition** : Un objet est une instance d'une classe, qui a des valeurs spécifiques pour ses attributs et peut exécuter des méthodes.

```java
public class Main {
    public static void main(String[] args) {
        // Création d'un objet (instanciation)
        Voiture maVoiture = new Voiture();

        // Utilisation de la méthode de l'objet
        maVoiture.demarrer();  // Affiche : "La voiture démarre"
    }
}
```

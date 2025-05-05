# Programmation Impérative

La programmation impérative est un paradigme (manière de penser et d'organiser le code) où l'on décrit comment un programme doit effectuer ses tâches, en enchaînant des instructions qui modifient l'état du programme.

## Caractéristiques principales :

1. **Séquence d'instructions** : Le code s'exécute étape par étape, comme une recette.
2. **Variables et affectation** : On utilise des variables pour stocker des données et on peut les modifier avec des instructions.
3. **Structures de contrôle** : Utilisation de boucles (for, while), de conditions (if, else), etc.
4. **Effets de bord** : Les fonctions/instructions peuvent modifier l’état global (par exemple, changer une variable ou afficher à l’écran).

**Exemple en Java** :

```java
public class SommeImperative {
    public static void main(String[] args) {
        int somme = 0;

        for (int i = 1; i <= 10; i++) {
            somme = somme + i; // ou somme += i;
        }

        System.out.println("La somme de 1 à 10 est : " + somme);
    }
}
```

**Analyse** :

- `int somme = 0`; : on déclare et initialise une variable (état).

- `for (...)` : une structure de contrôle pour répéter une action.

- `somme = somme + i;` : instruction impérative qui change l'état du programme.

- `System.out.println(...)` : effet de bord (affichage à l'écran).

Tout cela correspond bien au style impératif : le code dit exactement _comment_ faire le calcul étape par étape.

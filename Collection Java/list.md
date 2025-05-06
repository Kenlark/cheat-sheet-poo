## List (ArrayList, LinkedList)

### Caractéristiques

- **Ordre respecté**
- **Doublons autorisés**
- Accès par **indice** (`get(int index)`)

### ArrayList

- Basée sur un tableau dynamique
- Accès rapide par index (temps constant)
- Insertion/suppression lente en milieu de liste

```java
List<String> noms = new ArrayList<>();
noms.add("Alice");
noms.add("Bob");
System.out.println(noms.get(1)); // Bob
```

### LinkedList

- Liste doublement chaînée
- Insertion/suppression rapide au début/milieu
- Accès lent par index

```java
 List<String> chaines = new LinkedList<>();
        chaines.add("a");
        chaines.add("b");

        System.out.println("Premier élément : " + chaines.getFirst()); // Affiche "a"

        chaines.removeFirst(); // Enlève "a"

        System.out.println("Nouveau premier élément : " + chaines.getFirst()); // Affiche "b"
```

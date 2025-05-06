## Set (HashSet, TreeSet)

### Caractéristiques

- Pas de doublons
- Pas d'accès par index
- Utilisé pour les valeurs uniques

### HashSet

- Basé sur une table de hachage
- Pas d'ordre garanti
- Très rapide (0(1)) `add`, `contains`, etc.

```java
Set<String> emails = new HashSet<>();
emails.add("a@example.com");
emails.add("a@example.com"); // ignoré

System.out.println(emails);
```

### TreeSet

- Basé sur un arbre binaire (trié)
- Tri naturel (ou via `Comparator`)
- Plus lent que HashSet

```java
Set<Integer> scores = new TreeSet<>();
scores.add(42);
scores.add(7);
System.out.println(scores); // [7, 42]
```

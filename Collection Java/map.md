## Map (HashMap, TreeMap)

### Caractéristiques

- Stocke des paires clé/valeur
- Clés uniques
- Valeurs peuvent être dupliquées
- Pas une `Collection`, mais dans le framework Collections

### HashMap

- Clés non triées, ordre non garanti
- Rapide (0(1)) pour `put`, `get`, `remove`

```java
Map<String, Integer> ages = new HashMap<>();
ages.put("Alice", 25);
ages.put("Bob", 30);
System.out.println("before " + ages.get("Alice")); // 25
ages.remove("Alice");
System.out.println(ages.get("After" + "Alice")); // null
```

### TreeMap

- Clés triées (ordre naturel ou `Comparator`)
- Plus lent

```java
Map<Integer, String> codes = new TreeMap<>();
codes.put(2, "B");
codes.put(1, "A");
codes.remove(1);
System.out.println(codes); //  {2=B}
```

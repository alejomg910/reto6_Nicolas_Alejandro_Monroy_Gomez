# reto6_Nicolas_Alejandro_Monroy_Gomez

## Reto 6
Para este reto 6 hay que desarrollar estos 6 puntos en un notebook de python, el cual estará adjuntado en este repo. Los 3 primeros puntos deben tener diagramas de flujo y además, el código debe ir debidamente documentado.


1. Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.
``` mermaid
flowchart TD
 subgraph extra_block[" "]
    direction TB
        n9["&lt;bloque_sig&gt;"]
  end
    n1["Inicio"] --> n2["n = 1"]
    n2 --> n3["n &lt;= 100?"]
    n3 -- V --> n4["n ^ 2"]
    n4 --> n5["n = n + 1"]
    n5 --> n3
    n3 -- F --> n9
    n10["&lt;bloque_prev&gt;"] --> n1

    n9@{ shape: rounded}
    n10@{ shape: rounded}
    style extra_block stroke:none
```


2.  Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.
```mermaid
---
config:
  layout: fixed
---
flowchart TD
 subgraph extra_block[" "]
    direction TB
        n9["&lt;bloque_sigui&gt;"]
  end
 subgraph s1[" "]
        n17["&lt;bloque_sigui&gt;"]
  end
    n1["Inicio"] --> n2["m = 1"]
    n2 --> n3["m &lt;= 499"]
    n3 -- V --> n4["print ((2 * m) + 1)"]
    n4 --> n5["m = m + 1"]
    n5 --> n3
    n3 -- F --> n9
    n10["&lt;bloque_prev&gt;"] --> n1
    n11["&lt;bloque_prev&gt;"] --> n12["inicio"]
    n12 --> n13["n = 1"]
    n13 --> n14["n &lt;= 500"]
    n14 --> n15["print (2 * n)"] & n17
    n15 --> n16["n = n + 1"]
    n16 -- F --> n14
    n9@{ shape: rounded}
    n3@{ shape: diam}
    n10@{ shape: rounded}
    n11@{ shape: rounded}
    n14@{ shape: diam}
    style extra_block stroke:none
    style s1 stroke:none

```

3.  Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado.
```mermaid
flowchart TD
    n1["&lt;bloque_previo&gt;"] --> n2["Ingresa un numero entero:"]
    n2 --> n3["n &gt; 2"]
    n3 --> n4["print (n - 1)"] & n6["&lt;bloque_sigui&gt;"]
    n4 --> n5["n = n -1"]
    n5 --> n3

    n1@{ shape: rounded}
    n3@{ shape: diam}
    n6@{ shape: rounded}

```
4. Imprimir el factorial de un número natural n dado.
5. Implementar un programa que ingrese un número de 2 a 50 y muestre sus divisores.
6. Implementar el algoritmo que muestre los números primos del 1 al 100. **Nota:** use funciones

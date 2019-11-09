## Tercera parte
Aclaración: Para esta tercer parte de la práctica, no está permitido usar los siguientes paquetes:
- "strings"

### Primer tanda
Para esta primer tanda vamos a tratar de ejercitar el cerebro y acostumbrarlo a usar nuestra nueva estructura de control, el ciclo `for`. Vamos a realizar algunas tareas bastante comunes y recurrentes en el mundo informático como acumular valores, contar cantidades, procesar strings, transformar caracteres, encontrar ocurrencias, entre otras. Como bien se aclara en el comienzo de esta **tercer parte**, no usar la librería de "strings".

#### 1. Dado un array de 5 enteros imprimir el tercer elemento

#### 2. Dado un array de 5 enteros imprimirlos todos en pantalla de la siguiente forma
- `"el elemento <i> es <n>"` -> reemplazando `<i>` por el índice y `<n>` por el numero asociado (por cada elemento)

#### 3. Dado un array de 5 enteros imprimirlos igual que en el ejercicio anterior pero en el orden inverso

#### 4. Dado un array de 5 enteros imprimir el resultado de sumarlos todos

#### 5. Dado un array de 5 enteros imprimir el resultado de multiplicarlos todos

#### 6. Dado un array de 5 enteros imprimir el mayor y el menor

#### 7. Dado un array de 5 enteros, solicitar el ingreso de un entero e imprimir todos los números del array que sean múltiplos del valor ingresado

#### 8. Dado un array de 5 letras, solicitar el ingreso de un número entero que representará el número de elemento que desea ver e imprimir
- `"el elemento <n> es <c>"` -> si el numero ingresado es válido (reemplazando `<n>` por el número ingresado y `<c>` por la letra asociada)
- `"está más allá de mis límites"` -> si el número ingresado es inválido

#### 9. Solicitar el ingreso de un string e imprimir la cantidad de caracteres que lo componen

#### 10. Solicitar el ingreso de un string e imprimir cada letra que lo compone separada por un guión

#### 11. Solicitar el ingreso de un string y un char e imprimir
- `"<s> contiene <c>"` -> si el string ingresado contiene al char ingresado
- `"<s> no contiene ningun <c>"` -> si el string ingresado no contiene al char ingresado

(Reemplazando `<s>` por el string y `<c>` por el char)

#### 12. Solicitar el ingreso de un string y un char e imprimir
- `"el string <s> contiene <n> veces el char <c>"`

(Reemplazando `<s>` por el string, `<c>` por el char y `<n>` por la cantidad de ocurrencias de `<c>` en `<s>`)

#### 13. Solicitar el ingreso de un string y un char e imprimir
- `"encontrado en <i>"` -> si se encontró el char en el string (mostrando el índice de la primer ocurrencia)
- `"no encontrado"` -> si no se encontró el char en el string

#### 14. Solicitar el ingreso de un string y un char e imprimir
- `"encontrado en [<i>,<i>,<i>,etc]"` -> si se encontró el char en el string (mostrando todos los índices de las ocurrencias encontradas)
- `"no encontrado"` -> si no se encontró el char en el string

#### 15. Solicitar el ingreso de un string e imprimir el mismo string reemplazando todas las `a` por `A`

#### 16. Solicitar el ingreso de un string e imprimirlo en mayúsculas

#### 17. Solicitar el ingreso de un string e imprimirlo en minúsculas

#### 18. Solicitar el ingreso de un string e imprimir si representa  un número válido

#### 19. Solicitar el ingreso de un string y un número entero que representará un índice en el string e imprimir
- `"el string a partir de <i> es <s>"` -> si el numero ingresado es un indice válido 
- `"fuera de rango"` -> si el numero ingresado es un indice invalido

(Reemplazando `<i>` por el numero y `<s>` por el string a partir del índice `<i>` ingresado)

#### 20. Solicitar el ingreso de un string y dos números enteros que representará un índice de comienzo y de fin en el string e imprimir
- `"el string a partir de <i1> y hasta <i2> es <s>"` -> si los numeros ingresados son válidos 
- `"fuera de rango"` -> si al menos uno de los numeros ingresados es un indice invalido

(Reemplazando `<i1>`  e `<i2>` por los indices y `<s>` por el string a partir del índice `<i1>` y hasta `<i2>`)

#### 21. Solicitar el ingreso de dos strings e imprimir
- `"son iguales"` -> si representan el mismo string
- `"son parecidos"` -> si difieren en no mas de 2 letras
- `"son distintos"` -> si difieren en más de 2 letras

### Segunda tanda
En esta tanda vamos a tratar de sacar ese artista que llevamos dentro. Para es importante que respetes los formatos planteados. No agregar espacios, enters, tabs, etc. a menos que así se visualice. Demás está decir que cada ejercicio está pensado para ser _pintado_ usando ciclos `for` (anidados o no) por lo que tener un `fmt.Print(...)` con todo el dibujo no es válido. A dibujar!

#### 1. Dibujar la siguiente figura en consola
```
***** *****
```

#### 2. Dibujar la siguiente figura en consola
```
**********
**********
**********
**********
```

#### 3. Dibujar la siguiente figura en consola
```
**********
*        *
**********
```

#### 4. Dibujar la siguiente figura en consola
```
**********
*        *
**********
*        *
**********
*        *
**********
```

#### 5. Dibujar la siguiente figura en consola
```
*    
**   
***  
**** 
*****
```

#### 6. Dibujar la siguiente figura en consola
```
*****
**** 
***  
**   
*    
```

#### 7. Dibujar la siguiente figura en consola
```
    *
   **
  ***
 ****
*****
```

#### 8. Dibujar la siguiente figura en consola
```
*****
 ****
  ***
   **
    *
```

#### 9. Dibujar la siguiente figura en consola
```
    *    
   ***   
  *****  
 ******* 
*********
 ******* 
  *****  
   ***   
    *    
```

#### 10. Encontrar el patrón y dibujar la siguiente figura en consola
```
*.*.*.*.*.
**.**.**.*
***.***.**
****.****.
*****.****
******.***
*******.**
********.*
*********.
**********
```

#### 11. Dibujar el siguiente eje de coordenadas
```
     |     
     |     
     |     
     |     
     |     
-----|-----
     |     
     |     
     |     
     |     
     |     
```

#### 12. Dibujar la siguiente función lineal en consola (para valientes)
>f(x) = x

Considerando que cada paso en x es 1 y cada paso en y es 1
```
     |    *
     |   * 
     |  *  
     | *   
     |*    
-----*-----
    *|     
   * |     
  *  |     
 *   |     
*    |     
```

#### 13. Dibujar la siguiente función en consola (para muy valientes)
>f(x) = sen(x)

Considerando que cada paso en x es Pi/4 y cada paso en y es 1
```
          |          
          |          
    *     | *       *
--*---*---*---*---*--
*       * |     *    
          |          
          |          
```

### Tercer tanda
Aclaración: Donde se pida solicitar el ingreso de arrays (independiente del tipo solicitado) se deja al programador definir el tamaño del mismo al momento de compilación salvo que se indique lo contrario.

#### 1. Solicitar el ingreso de un array de dos números reales e imprimir el mayor

#### 2. Solicitar el ingreso de un array de dos números reales e imprimirlos en orden de mayor a menor

#### 3. Solicitar el ingreso de un array de tres números reales e imprimir el mayor

#### 4. Solicitar el ingreso de un array de tres números reales e imprimirlos en orden de mayor a menor

#### 5. Solicitar el ingreso de un array de números reales (los que se quieran) e imprimir el mayor de todos ellos

#### 6. Solicitar el ingreso de un array de números reales (los que se quieran) e imprimirlos en orden de mayor a menor (solo para valientes)

#### 7. Dado un array de números reales, imprimirlos en orden de mayor a menor cortando prematuramente una vez ordenado el array (dependiendo de como resuelvan el ejercicio anterior este ejercicio está repetido o no) (solo para muy valientes)

#### 8. Solicitar el ingreso de dos arrays de números enteros de igual tamaño e imprimir si ambos arrays contienen los mismos elementos (sin importar el orden). Asumir que no hay repetidos
Ej: 

[1, 2, 3, 4] [2, 3, 1, 4] -> contienen los mismos elementos

[-1, 2, 3, 4] [2, -1, 3, 6] -> no contienen los mismos elementos

#### 9. Solicitar el ingreso de dos strings e imprimir
- `"<s1> contiene al string <s2>"` -> si el primer string contiene al segundo
- `"<s1> no contiene al string <s2>"` -> si el segundo string no contiene al segundo

#### 10. Solicitar el ingreso de tres strings e imprimir el resultado de hallar el segundo string en el primer string y reemplazarlo por el tercer string
Ej: 
- palito ito ote -> imprime `palote`
- confusion fu tor -> imprime `contorsion`
- delgadez dele to -> imprime `delgadez` (no se encontró el string a reemplazar)

#### 11. Solicitar el ingreso de un string y un array de strings e imprimir
- `"<s1> contiene al menos un string del array"` -> si el string contiene al menos un string del array
- `"<s1> no contiene ningun string del array"` -> si el string no contiene ningún string del array

#### 12. Solicitar el ingreso de un string e imprimir
- `"<string> es palíndromo"` -> si el string ingresado es palíndromo
- `"<string> no es palíndromo"` -> si el string ingresado no es palíndromo

### Cuarta tanda
En esta cuarta tanda vamos a ejercitar un concepto interesante en el mundo de los ciclos y arrays. Matrices o arrays multidimensionales! 
Cuando hablemos de filas y columnas nos vamos a referir a 
- fila -> el primer indice
- columna -> el segundo indice

#### 1. Dada una matriz de 3 x 3 de números enteros, imprimir el elemento 2 - 2

#### 2. Dada una matriz de 3 x 3 de números enteros, imprimir toda la matriz de la siguiente forma
```
     c1 c2 c3  
    ---------- 
f1 | n1 n2 n3 |
f2 | n4 n5 n6 |
f3 | n7 n8 n9 |
    ---------- 
```
#### 3. Dada una matriz de 3 x 3 de números enteros, imprimir el mayor de toda la matriz

#### 4. Dada una matriz de 3 x 3 de números enteros, imprimir el menor de cada fila

#### 5. Dada una matriz de 3 x 3 de número enteros, imprimir el menor de cada columna

#### 6. Dada una matriz de 3 x 3 de número enteros, imprimir si representa un cuadrante válido según las siguientes reglas
- la sumatoria de toda la matriz no debe exceder el valor `50`
- la sumatoria de cada fila no debe exceder el valor `30`
- la sumatoria de cada columna no debe ser menor al valor `10`
- ningún valor de la matriz debe exceder el valor `10`
- ningún valor de la matriz debe ser menor al valor `1`

#### 7. Dada una matriz de 3 x 3 de número enteros, imprimir si representa un cuadrante válido para el SUDOKU según las siguientes reglas
- los números de cada casillero deben estar entre el `1` y el `9`
- no deben repetirse números en ningún casillero de la matriz

#### 8. Dada una matriz de 9 x 9 números enteros, imprimir la matriz de la siguiente forma 
```
+ - - - + - - - + - - - +
| n n n | n n n | n n n |
| n n n | n n n | n n n |
| n n n | n n n | n n n |
+ - - - + - - - + - - - +
| n n n | n n n | n n n |
| n n n | n n n | n n n |
| n n n | n n n | n n n |
+ - - - + - - - + - - - +
| n n n | n n n | n n n |
| n n n | n n n | n n n |
| n n n | n n n | n n n |
+ - - - + - - - + - - - +
```
#### e indicar si representa una solución válida para el SUDOKU según las siguientes reglas
- las filas deben contener solo números del `1` al `9`
- las filas no deben contener números repetidos
- las columnas deben contener solo números del `1` al `9`
- las columnas no debe contener números repetidos
- cada cuadrante de 3 x 3 debe contener solo números del `1` al `9`
- cada cuadrante de 3 x 3 no debe contener números repetidos

#### 9. Dado un array de 5 x 5 booleanos determinar cual será el camino (solo para valientes) para llegar de un punto a otro de la matriz teniendo en cuenta que 
- la matriz representa un laberinto
- el laberinto puede no tener salida
- solo existe un posible camino (no hay bifurcaciones)
- uno comienza en la posición `0,0` y debe llegar a la `4,4`
- uno puede moverse de a un casillero horizontalmente (izquierda o derecha) o verticalmente (arriba o abajo)
- una posición `true` representa un camino libre por el que se puede ir
- una posición `false` representa un camino bloqueado por el que no se puede ir

imprimir:
- `el camino es: n1,m1 -> n2,m2 -> n3,m3 -> n4,m4 -> etc`
- `no existe un camino para llegar`

#### Para pensar:
- Cambiaría algo del ejercicio anterior si la matriz fuera de 10 x 10?
- Qué pasaría si la restricción de `"solo existe un posible camino (no hay bifurcaciones)"` no estuviera? Podría resolver el ejercicio con las herramientas de las que dispone (sin depender de la dimensión de la matriz)?
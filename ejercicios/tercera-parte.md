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
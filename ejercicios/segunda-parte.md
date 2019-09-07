## Segunda Parte
Aclaración: Acá sí el programa tiene que pedir al usuario ciertos datos. Dichos datos serán aclarados en cada punto.

#### 1. Solicitar el ingreso de 2 números enteros e imprimir el mayor.

#### 2. Solicitar el ingreso de 2 números enteros e imprimirlos en orden de mayor a menor

#### 3. Solicitar el ingreso de 3 números enteros e imprimir el mayor

#### 4. Solicitar el ingreso de 3 números enteros e imprimirlos en orden de mayor a menor

#### 5. Solicitar el ingreso de 4 números enteros e imprimir el mayor

#### 6. Solicitar el ingreso de 4 números enteros e imprimirlos en orden de mayor a menor (solo para valientes)

#### 7. Solicitar el ingreso de 1 número entero e imprimir
- `"par"` -> si es par
- `"impar"` -> si es impar
- `"ni par ni impar"` -> si es 0

*recordar que un numero es par si es divisible por 2

#### 8. Solicitar el ingreso de 2 números enteros e imprimir
- `"estan bastante distanciados"` -> si la diferencia entre ambos es mayor o igual a 130
- `"estan cerca"` -> si la diferencia entre ambos es mayor o igual a 30 pero menor a 130
- `"estan re cerquita"` -> si la diferencia entre ambos es mayor o igual a 1 pero menor a 30
- `"son iguales"` -> si la diferencia es 0

#### 9. Solicitar el ingreso de un número entero que representará un dia de la semana e imprimir
- `"domingo"` -> si es 0
- `"lunes"` -> si es 1
- `"martes"` -> si es 2
- `"miércoles"` -> si es 3
- `"martes"` -> si es 4
- `"jueves"` -> si es 5
- `"viernes"` -> si es 6
- `"sábado"` -> si es 7
- `"error"` -> si no es ninguno de los anteriores

#### 10. Solicitar el ingreso de un número entero e imprimir el resultado de multiplicarlo por 2 y sumarle 10
Notar que lo que se pide simula una función lineal del tipo: 
> f(x) = 2x + 10

#### 11. Solicitar el ingreso de un número entero e imprimir el resultado de elevarlo al cuadrado, sumarle 5 veces el numero y restarle 4
Notar que lo que se pide simula una función cuadrática del tipo: 
> f(x) = x^2 + 5x - 4

#### 12. Solicitar el ingreso de 3 números reales que representan los coeficientes principales de una función cuadrática e imprimir 
- Cuando existan las raíces y sean distintas
 ```
 Las raices de la función f(x) = <a>x^2 + <b>x + <c> son:
 x1 = <raiz1>
 x2 = <raiz2>
 ```
 - Cuando existan las raíces y sean iguales
  ```
 "Las raices de la función f(x) = <a>x^2 + <b>x + <c> son:
 x1 = x2 = <raiz>
 ```
 - Cuando no existan raíces
  ```
 La función f(x) = <a>x^2 + <b>x + <c> no tiene raíces reales
 ```
 En todos los casos hay que reemplazar a, b y c con los valores que haya ingresado el usuario y raiz/raiz1/raiz2 con el valor de la/las raíces calculadas
 
*Recordar que para el cálculo de las raíces se utiliza la fórmula resolvente y que el discriminante es particularmente útil en este caso. 

#### 13. Solicitar el ingreso de 3 números reales que representarán los lados de un triángulo e imprimir
- `"es equilatero"` -> si todos sus lados son iguales
- `"es isosceles"` -> si dos de sus lados son iguales y uno desigual
- `"es escaleno"` -> si todos sus lados son distintos

#### 14. Solicitar el ingreso de 1 número real que representará el radio de una esfera e imprimir
- `"la circunferencia es <circ>, la superficie es <sup>, el volumen es <vol>"` -> si el radio es positivo
- `"con radio 0, todo es 0"` -> si el radio es 0
- `"ya nada tiene sentido"` -> si el radio es negativo

#### 15.  Solicitar el ingreso de 5 números reales e imprimir
- `"el resultado es <res>"` -> obtenido de dividir cada número por el siguiente (acumulando el resultado)
- `"no voy a caer"` -> si hay alguna operación que no puede hacerse

#### 16.  Solicitar el ingreso de 2 strings que representarán un usuario y contraseña para ingresar a un sistema e imprimir
- `"usuario incorrecto"` -> si el usuario ingresado es incorrecto
- `"password incorrecto"` -> si el usuario ingresado es correcto pero la contraseña es incorrecta
- `"acceso otorgado"` -> si el usuario y password ingresados son correctos
- 
#### 17. Basado en el ejercicio anterior, si el acceso es otorgado (después de mostrar dicho mensaje), preguntar al usuario si desea cambiar la contraseña. Si responde afirmativamente, solicitar el ingreso del nuevo password 2 veces e imprimir
- `"password cambiado exitosamente"` -> si la nueva contraseña ingresada coincide con la confirmación
- `"error al cambiar el password. Los passwords no coinciden"` -> si la nueva contraseña y su confirmación no coinciden

#### 18. Solicitar el ingreso de un string que representará un mes del año e imprimir 
- `"1"` -> si ingresó `enero`
- `"2"` -> si ingresó `febrero`
- `"3"` -> si ingresó `marzo`
- `"4"` -> si ingresó `abril`
- `"5"` -> si ingresó `mayo`
- `"6"` -> si ingresó `junio`
- `"7"` -> si ingresó `julio`
- `"8"` -> si ingresó `agosto`
- `"9"` -> si ingresó `septiembre`
- `"10"` -> si ingresó `octubre`
- `"11"` -> si ingresó `noviembre`
- `"12"` -> si ingresó  `diciembre`
- `"error"` -> si ingresó cualquier otra cosa

#### 19. Basado en el ejercicio anterior, ahora imprimir
- `"estamos en el mes corriente"` -> si ingreso el nombre del mes actual al momento de correr el programa
- `"no es el mes corriente"` -> si ingresó otro mes
- `"ni siquiera es un mes"` -> si ingresó cualquier otra cosa
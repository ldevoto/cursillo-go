## Segunda Parte
Aclaración: Acá sí el programa tiene que pedir al usuario ciertos datos. Dichos datos serán aclarados en cada punto.

#### 1. Solicitar el ingreso de 2 números enteros e imprimir el mayor.

#### 2. Solicitar el ingreso de 2 números enteros e imprimirlos en orden de menor a mayor

#### 3. Solicitar el ingreso de 3 números enteros e imprimir el mayor

#### 4. Solicitar el ingreso de 3 números enteros e imprimirlos en orden de menor a mayor

#### 5. Solicitar el ingreso de 4 números enteros e imprimir el mayor

#### 6. Solicitar el ingreso de 4 números enteros e imprimirlos en orden de menor a mayor (solo para valientes)

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

#### 10. Solicitar el ingreso de un número entero e imprimir el resultado de elevarlo al cuadrado, sumarle 5 veces el numero y restarle 4
Notar que lo que se pide simula una función del tipo: 
> f(x) = x^2 + 5x - 4

#### 11. Solicitar el ingreso de 3 números reales que representan los coeficientes principales de una función cuadrática e imprimir 
- Cuando existan las raíces y sean distintas
 ```
 Las raices de la función f(x) = ax^2 + bx + c son:
 x1 = <raiz1>
 x2 = <raiz2>
 ```
 - Cuando existan las raíces y sean iguales
  ```
 "Las raices de la función f(x) = ax^2 + bx + c son:
 x1 = x2 = <raiz>
 ```
 - Cuando no existan raíces
  ```
 La función f(x) = ax^2 + bx + c no tiene raíces reales
 ```
 En todos los casos hay que reemplazar a, b y c con los valores que haya ingresado el usuario y raiz/raiz1/raiz2 con el valor de la/las raíces calculadas
 
*Recordar que para el cálculo de las raíces se utiliza la fórmula resolvente y que el discriminante es particularmente útil en este caso. 

#### 12. Solicitar el ingreso de 3 números reales que representarán los lados de un triángulo e imprimir
- `"es equilatero"` -> si todos sus lados son iguales
- `"es isosceles"` -> si dos de sus lados son iguales y uno desigual
- `"es escaleno"` -> si todos sus lados son distintos

#### 13. Solicitar el ingreso de 1 número real que representará el radio de una esfera e imprimir
- `"la circunferencia es <circ>, la superficie es <sup>, el volumen es <vol>"` -> si el radio es positivo
- `"con radio 0, todo es 0"` -> si el radio es 0
- `"no voy a pisar el palito"` -> si el radio es negativo

#### 14.  Solicitar el ingreso de 2 strings que representarán un usuario y contraseña para ingresar a un sistema e imprimir
- `"usuario incorrecto"` -> si el usuario ingresado es incorrecto
- `"password incorrecto"` -> si el usuario ingresado es correcto pero la contraseña es incorrecta
- `"acceso otorgado"` -> si el usuario y password ingresados son correctos
- 
#### 15. Basado en el ejercicio anterior, si el acceso es otorgado (después de mostrar dicho mensaje), preguntar al usuario si desea cambiar la contraseña. Si responde afirmativamente, solicitar el ingreso del nuevo password 2 veces e imprimir
- `"password cambiado exitosamente"` -> si la nueva contraseña ingresada coincide con la confirmación
- `"error al cambiar el password. Los passwords no coinciden"` -> si la nueva contraseña y su confirmación no coinciden
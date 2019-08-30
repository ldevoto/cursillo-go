## Segunda Parte

#### 1. Solicitar el ingreso de 2 números enteros e imprimir el mayor.
```go
package main

import "fmt"

func main() {
  var number1 int
  var number2 int
  
  fmt.Println("Ingrese dos números enteros")
  fmt.Scanf("%d %d", &number1, &number2)
  if number1 > number2 {
    fmt.Println("el mayor es el", number1)
  } else {
    fmt.Println("el mayor es el", number2)
  }
}
```

#### 2. Solicitar el ingreso de 2 números enteros e imprimirlos en orden de mayor a menor
```go
package main

import "fmt"

func main() {
  var number1 int
  var number2 int
  
  fmt.Println("Ingrese dos números enteros")
  fmt.Scanf("%d %d", &number1, &number2)
  if number1 > number2 {
    fmt.Println(number1, number2)
  } else {
    fmt.Println(number2, number1)
  }
}
```

#### 3. Solicitar el ingreso de 3 números enteros e imprimir el mayor
```go
package main

import "fmt"

func main() {
  var number1 int
  var number2 int
  var number3 int
  var max int
  
  fmt.Println("Ingrese tres números enteros")
  fmt.Scanf("%d %d %d", &number1, &number2, &number3)
  if number1 > number2 {
    max = number1
  } else {
    max = number2
  }
  if number3 > max {
    max = number3
  }
  fmt.Println("el mayor es el", max)
}
```

#### 4. Solicitar el ingreso de 3 números enteros e imprimirlos en orden de mayor a menor
```go
package main

import "fmt"

func main() {
  var number1 int
  var number2 int
  var number3 int
  
  fmt.Println("Ingrese tres números enteros")
  fmt.Scanf("%d %d %d", &number1, &number2, &number3)
  if number1 > number2 {
    if number2 > number3 {
      fmt.Println(number1, number2, number3)
    } else if number1 > number3 {
      fmt.Println(number1, number3, number2)
    } else {
      fmt.Println(number3, number1, number2)
    }
  } else {
    if number1 > number3 {
      fmt.Println(number2, number1, number3)
    } else if number2 > number3 {
      fmt.Println(number2, number3, number1)
    } else {
      fmt.Println(number3, number2, number1)
    }
  }
}
```

#### 5. Solicitar el ingreso de 4 números enteros e imprimir el mayor
```go
package main

import "fmt"

func main() {
  var number1 int
  var number2 int
  var number3 int
  var number4 int
  var max int
  
  fmt.Println("Ingrese cuatro números enteros")
  fmt.Scanf("%d %d %d %d", &number1, &number2, &number3, &number4)
  if number1 > number2 {
    max = number1
  } else {
    max = number2
  }
  if number3 > max {
    max = number3
  }
  if number4 > max {
    max = number4
  }
  fmt.Println("el mayor es el", max)
}
```

#### 6. Solicitar el ingreso de 4 números enteros e imprimirlos en orden de mayor a menor (solo para valientes)
```go
package main

import "fmt"

func main() {
  var number1 int
  var number2 int
  var number3 int
  var number4 int
  var max int
  var middleMax int
  var middleMin int
  var min int
  
  fmt.Println("Ingrese cuatro números enteros")
  fmt.Scanf("%d %d %d %d", &number1, &number2, &number3, &number4)
  
  if number1 > number2 {
    max = number1
    middleMax = number2
  } else {
    max = number2
    middleMax = number1
  }
  
  if number3 > max {
    middleMin = middleMax
    middleMax = max
    max = number3
  } else if number3 > middleMax {
    middleMin = middleMax
    middleMax = number3
  }
  
  if number4 > max {
    min = middleMin
    middleMin = middleMax
    middleMax = max
    max = number4
  } else if number4 > middleMax {
    min = middleMin
    middleMin = middleMax
    middleMax = number4
  } else if number4 > middleMin {
    min = middleMin
    middleMin = number4
  } else {
    min = number4
  }
  
  fmt.Println(max, middleMax, middleMin, min)
}
```

#### 7. Solicitar el ingreso de 1 número entero e imprimir
- `"par"` -> si es par
- `"impar"` -> si es impar
- `"ni par ni impar"` -> si es 0

*recordar que un numero es par si es divisible por 2
```go
package main

import "fmt"

func main() {
  var number int
  
  fmt.Println("Ingrese un numero entero")
  fmt.Scanf("%d", &number)
  if number == 0 {
    fmt.Println("ni par ni impar")
  } else if number % 2 == 0 {
    fmt.Println("par")
  } else {
    fmt.Println("impar")
  }
}
```

#### 8. Solicitar el ingreso de 2 números enteros e imprimir
- `"estan bastante distanciados"` -> si la diferencia entre ambos es mayor o igual a 130
- `"estan cerca"` -> si la diferencia entre ambos es mayor o igual a 30 pero menor a 130
- `"estan re cerquita"` -> si la diferencia entre ambos es mayor o igual a 1 pero menor a 30
- `"son iguales"` -> si la diferencia es 0
```go
package main

import "fmt"

func main() {
  var number1 int
  var number2 int
  var difference int
  
  fmt.Println("Ingrese dos números enteros")
  fmt.Scanf("%d %d", &number1, &number2)
  difference = number1 - number2
  if (difference < 0) {
    difference = difference * -1
  }
  if difference >= 130 {
    fmt.Println("estan bastante distanciados")
  } else if difference >= 30 {
    fmt.Println("estan cerca")
  } else if difference >= 1 {
    fmt.Println("estan re cerquita")
  } else {
    fmt.Println("son iguales")
  }
}
```

#### 9. Solicitar el ingreso de un número entero que representará un dia de la semana e imprimir
- `"domingo"` -> si es 0
- `"lunes"` -> si es 1
- `"martes"` -> si es 2
- `"miércoles"` -> si es 3
- `"jueves"` -> si es 4
- `"viernes"` -> si es 5
- `"sábado"` -> si es 6
- `"error"` -> si no es ninguno de los anteriores
```go
package main

import "fmt"

func main() {
  var dayOfWeek int
  
  fmt.Println("Ingrese un número que representará un día de la semana")
  fmt.Scanf("%d", &dayOfWeek)
  switch dayOfWeek {
    case 0:
      fmt.Println("domingo.")
    case 1:
      fmt.Println("lunes")
    case 2:
      fmt.Println("martes")
    case 3:
      fmt.Println("miercoles")
    case 4:
      fmt.Println("jueves")
    case 5:
      fmt.Println("viernes")
    case 6:
      fmt.Println("sábado")
    default:
      fmt.Println("error")
  }
}
```

#### 10. Solicitar el ingreso de un número entero e imprimir el resultado de multiplicarlo por 2 y sumarle 10
Notar que lo que se pide simula una función lineal del tipo: 
> f(x) = 2x + 10

#### 10. Solicitar el ingreso de un número entero e imprimir el resultado de elevarlo al cuadrado, sumarle 5 veces el numero y restarle 4
Notar que lo que se pide simula una función cuadrática del tipo: 
> f(x) = x^2 + 5x - 4

#### 11. Solicitar el ingreso de 3 números reales que representan los coeficientes principales de una función cuadrática e imprimir 
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

#### 12. Solicitar el ingreso de 3 números reales que representarán los lados de un triángulo e imprimir
- `"es equilatero"` -> si todos sus lados son iguales
- `"es isosceles"` -> si dos de sus lados son iguales y uno desigual
- `"es escaleno"` -> si todos sus lados son distintos

#### 13. Solicitar el ingreso de 1 número real que representará el radio de una esfera e imprimir
- `"la circunferencia es <circ>, la superficie es <sup>, el volumen es <vol>"` -> si el radio es positivo
- `"con radio 0, todo es 0"` -> si el radio es 0
- `"ya nada tiene sentido"` -> si el radio es negativo

#### 14.  Solicitar el ingreso de 5 números reales e imprimir
- `"el resultado es <res>"` -> obtenido de dividir cada número por el siguiente (acumulando el resultado)
- `"no voy a caer"` -> si hay alguna operación que no puede hacerse

#### 15.  Solicitar el ingreso de 2 strings que representarán un usuario y contraseña para ingresar a un sistema e imprimir
- `"usuario incorrecto"` -> si el usuario ingresado es incorrecto
- `"password incorrecto"` -> si el usuario ingresado es correcto pero la contraseña es incorrecta
- `"acceso otorgado"` -> si el usuario y password ingresados son correctos
- 
#### 16. Basado en el ejercicio anterior, si el acceso es otorgado (después de mostrar dicho mensaje), preguntar al usuario si desea cambiar la contraseña. Si responde afirmativamente, solicitar el ingreso del nuevo password 2 veces e imprimir
- `"password cambiado exitosamente"` -> si la nueva contraseña ingresada coincide con la confirmación
- `"error al cambiar el password. Los passwords no coinciden"` -> si la nueva contraseña y su confirmación no coinciden

#### 17. Solicitar el ingreso de un string que representará un mes del año e imprimir 
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

#### 18. Basado en el ejercicio anterior, ahora imprimir
- `"estamos en el mes corriente"` -> si ingreso el nombre del mes actual al momento de correr el programa
- `"no es el mes corriente"` -> si ingresó otro mes
- `"ni siquiera es un mes"` -> si ingresó cualquier otra cosa
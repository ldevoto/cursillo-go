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
```go
package main

import "fmt"

func main() {
	var x int
	fmt.Print("Ingrese un número entero que será aplicado como 'x' a la función f(x) = 2 * x + 10: ")
	fmt.Scan(&x)
	fmt.Printf("f(%d) = 2 * %d + 10 = %d\n", x, x, 2*x + 10)
}
```

#### 11. Solicitar el ingreso de un número entero e imprimir el resultado de elevarlo al cuadrado, sumarle 5 veces el numero y restarle 4
Notar que lo que se pide simula una función cuadrática del tipo: 
> f(x) = x^2 + 5x - 4
```go
package main

import "fmt"

func main() {
	var x int
	fmt.Print("Ingrese un número entero que será aplicado como 'x' a la función f(x) = x ^ 2 + 5 * x - 4: ")
	fmt.Scan(&x)
	fmt.Printf("f(%d) = %d ^ 2 + 5 * %d - 4 = %d\n", x, x, x, x*x +  5*x -  4)
}
```

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
```go
package main

import "fmt"
import "math"

func main() {
	var a float64
	var b float64
	var c float64
	var x1 float64
	var x2 float64
	var discriminant float64
	
	fmt.Print("Ingrese 3 numeros reales que serán los coeficientes a, b y c de una función cuandrática: ")
	fmt.Scan(&a, &b, &c)

	if a != 0 {
		discriminant = math.Pow(b, 2) - 4 * a * c
		if discriminant > 0 {
			x1 = -b + math.Sqrt(discriminant)/(2*a)
			x2 = -b - math.Sqrt(discriminant)/(2*a)
			fmt.Printf("Las raices de la función f(x) = %.2fx^2 + %.2fx + %.2f son:\n", a, b, c)
			fmt.Printf("x1 = %.2f\nx2 = %.2f\n", x1, x2)
		} else if discriminant == 0 {
			x1 = -b
			fmt.Printf("Las raices de la función f(x) = %.2fx^2 + %.2fx + %.2f son:\n", a, b, c)
			fmt.Printf("x1 = x2 = %.2f\n", x1)
		} else {
			fmt.Printf("La función f(x) = %.2fx^2 + %.2fx + %.2f no tiene raíces reales\n", a, b, c)
		}
	} else {
		fmt.Println("Casi casi eh, no se puede dividir por 0. La función que trataste de ingresar no es cuadrática!")
	}
}
```

#### 13. Solicitar el ingreso de 3 números reales que representarán los lados de un triángulo e imprimir
- `"es equilatero"` -> si todos sus lados son iguales
- `"es isosceles"` -> si dos de sus lados son iguales y uno desigual
- `"es escaleno"` -> si todos sus lados son distintos
```go
package main

import "fmt"

func main() {
	var a float64
	var b float64
	var c float64
	
	fmt.Print("Ingrese tres números reales que representarán los lados de un triángulo: ")
	fmt.Scan(&a, &b, &c)

	if a == b && b == c {
		fmt.Println("es equilátero")
	} else if a != b && a != c && b != c {
		fmt.Println("es escaleno")
	} else {
		fmt.Println("es isósceles")
	}
}
```

#### 14. Solicitar el ingreso de 1 número real que representará el radio de una esfera e imprimir
- `"la circunferencia es <circ>, la superficie es <sup>, el volumen es <vol>"` -> si el radio es positivo
- `"con radio 0, todo es 0"` -> si el radio es 0
- `"ya nada tiene sentido"` -> si el radio es negativo
```go
package main

import "fmt"
import "math"

func main() {
	var r float64
	var circunference float64
	var area float64
	var volume float64
	
	fmt.Print("Ingrese un número real que representará el radio de una esfera: ")
	fmt.Scan(&r)

	if r > 0 {
		circunference = 2 * math.Pi * r
		area = 4 * math.Pi * math.Pow(r, 2)
		volume = (4 / 3) * math.Pi * math.Pow(r, 3)
		fmt.Printf("la circunferencia es %.2f, la superficie es %.2f y el volumen es %.2f\n", circunference, area, volume)
	} else if r == 0 {
		fmt.Println("con radio 0, todo es 0")
	} else {
		fmt.Println("ya nada tiene sentido")
	}
}
```

#### 15.  Solicitar el ingreso de 5 números reales e imprimir
- `"el resultado es <res>"` -> obtenido de dividir cada número por el siguiente (acumulando el resultado)
- `"no voy a caer"` -> si hay alguna operación que no puede hacerse
```go
package main

import "fmt"

func main() {
	var num1 float64
	var num2 float64
	var num3 float64
	var num4 float64
	var num5 float64
	var result float64
	
	fmt.Print("Ingrese 5 números reales: ")
	fmt.Scan(&num1, &num2, &num3, &num4, &num5)

	if num2 == 0 || num3 == 0 || num4 == 0 || num5 == 0 {
		fmt.Println("no voy a caer")
	} else {
		result = (((num1 / num2) / num3) / num4) / num5
		fmt.Printf("el resultado es %.4f\n", result)
	}
}
```

#### 16.  Solicitar el ingreso de 2 strings que representarán un usuario y contraseña para ingresar a un sistema e imprimir
- `"usuario incorrecto"` -> si el usuario ingresado es incorrecto
- `"password incorrecto"` -> si el usuario ingresado es correcto pero la contraseña es incorrecta
- `"acceso otorgado"` -> si el usuario y password ingresados son correctos
```go
package main

import "fmt"

func main() {
	const USER string = "Jose"
	const PASSWORD string = "roco"
	
	var user string
	var password string

	fmt.Print("Ingrese usuario: ")
	fmt.Scan(&user)
	fmt.Print("Ingrese contraseña: ")
	fmt.Scan(&password)

	if user != USER {
		fmt.Println("usuario incorrecto")
	} else {
		if password != PASSWORD {
			fmt.Println("password incorrecto")
		} else {
			fmt.Println("acceso otorgado")
		}
	}
}
```

#### 17. Basado en el ejercicio anterior, si el acceso es otorgado (después de mostrar dicho mensaje), preguntar al usuario si desea cambiar la contraseña. Si responde afirmativamente, solicitar el ingreso del nuevo password 2 veces e imprimir
- `"password cambiado exitosamente"` -> si la nueva contraseña ingresada coincide con la confirmación
- `"error al cambiar el password. Los passwords no coinciden"` -> si la nueva contraseña y su confirmación no coinciden
```go
package main

import "fmt"

func main() {
	const USER string = "Jose"
	const PASSWORD string = "roco"
	
	var user string
	var password string
	var answer string
	var newPassword1 string
	var newPassword2 string

	fmt.Print("Ingrese usuario: ")
	fmt.Scan(&user)
	fmt.Print("Ingrese contraseña: ")
	fmt.Scan(&password)

	if user != USER {
		fmt.Println("usuario incorrecto")
	} else {
		if password != PASSWORD {
			fmt.Println("password incorrecto")
		} else {
			fmt.Println("acceso otorgado")
			fmt.Print("Desea cambiar la contraseña (y/n)? :")
			fmt.Scan(&answer)
			if answer == "y" {
				fmt.Print("Ingrese su nueva contraseña: ")
				fmt.Scan(&newPassword1)
				fmt.Print("Repita su nueva contraseña: ")
				fmt.Scan(&newPassword2)
				
				if newPassword1 != newPassword2 {
					fmt.Println("error al cambiar el password. Los passwords no coinciden")
				} else {
					fmt.Println("password cambiado exitosamente")
				}
			}
		}
	}
}
```

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
```go
package main

import "fmt"

func main() {
	var month string

	fmt.Print("Ingrese el nombre de un mes: ")
	fmt.Scan(&month)
	
	switch month {
	case "enero":
		fmt.Println("1")
	case "febrero":
		fmt.Println("2")
	case "marzo":
		fmt.Println("3")
	case "abril":
		fmt.Println("4")
	case "mayo":
		fmt.Println("5")
	case "junio":
		fmt.Println("6")
	case "julio":
		fmt.Println("7")
	case "agosto":
		fmt.Println("8")
	case "septiembre":
		fmt.Println("9")
	case "octubre":
		fmt.Println("10")
	case "noviembre":
		fmt.Println("11")
	case "diciembre":
		fmt.Println("12")
	default:
		fmt.Println("error")
	}
}
```

#### 19. Basado en el ejercicio anterior, ahora imprimir
- `"estamos en el mes corriente"` -> si ingreso el nombre del mes actual al momento de correr el programa
- `"no es el mes corriente"` -> si ingresó otro mes
- `"ni siquiera es un mes"` -> si ingresó cualquier otra cosa
```go
package main

import "fmt"
import "time"

func main() {
	var month string
	var givenMonth time.Month
	var actualMonth time.Month
	var validMonth bool = true

	fmt.Print("Ingrese el nombre de un mes: ")
	fmt.Scan(&month)

	switch month {
	case "enero":
		givenMonth = time.January
	case "febrero":
		givenMonth = time.February
	case "marzo":
		givenMonth = time.March
	case "abril":
		givenMonth = time.April
	case "mayo":
		givenMonth = time.May
	case "junio":
		givenMonth = time.June
	case "julio":
		givenMonth = time.July
	case "agosto":
		givenMonth = time.August
	case "septiembre":
		givenMonth = time.September
	case "octubre":
		givenMonth = time.October
	case "noviembre":
		givenMonth = time.November
	case "diciembre":
		givenMonth = time.December
	default:
		validMonth = false
	}
	
	if validMonth {
		actualMonth = time.Now().Month()
		if actualMonth == givenMonth {
			fmt.Println("estamos en el mes corriente")
		} else {
			fmt.Println("no es el mes corriente")
		}
	} else {
		fmt.Println("Ni siquiera es un mes")
	}
}
```
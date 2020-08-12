## Tercera parte
En esta tercera parte vamos a tratar de ejercitar el cerebro y acostumbrarlo a usar nuestra nueva estructura de control, el ciclo `for`. Vamos a realizar algunas tareas bastante comunes y recurrentes en el mundo informático como acumular valores, contar cantidades, procesar strings, transformar caracteres, encontrar ocurrencias, entre otras.
Aclaración: Para esta tercer parte de la práctica, no está permitido usar los siguientes paquetes:
- "strings"

### Primera tanda
En esta tanda vamos a tratar de sacar ese artista que llevamos dentro. Para es importante que respetes los formatos planteados. No agregar espacios, enters, tabs, etc. a menos que así se visualice. Demás está decir que cada ejercicio está pensado para ser _pintado_ usando ciclos `for` (anidados o no) por lo que tener un `fmt.Print(...)` con todo el dibujo no es válido al igual que tener muchos `fmt.Print(...)` uno debajo del otro. La clave está en encontrar el patrón. A dibujar!

#### 1. Dibujar la siguiente figura en consola
```
***** *****
```
```go
package main

import "fmt"

func main() {
	const quantity = 11
	var i int
	
	for i = 0; i < quantity; i++ {
		if i != quantity / 2 {
			fmt.Print("*")
		} else {
			fmt.Print(" ")
		}
	}
	fmt.Println()
}
```

#### 2. Dibujar la siguiente figura en consola
```
**********
**********
**********
**********
```
```go
package main

import "fmt"

func main() {
	const rowQuantity = 4
	const columnQuantity = 10
	var i int
	var j int
	
	for i = 0; i < rowQuantity; i++ {
		for j = 0; j < columnQuantity; j++ {
			fmt.Print("*")
		}
		fmt.Println()
	}
}
```

#### 3. Dibujar la siguiente figura en consola
```
**********
*        *
**********
```
```go
package main

import "fmt"

func main() {
	const rowQuantity = 3
	const columnQuantity = 10
	var i int
	var j int
	
	for i = 0; i < rowQuantity; i++ {
		if i % 2 == 0 {
			for j = 0; j < columnQuantity; j++ {
				fmt.Print("*")
			}
			fmt.Println()
		} else {
			fmt.Print("*")
			for j = 0; j < columnQuantity - 2; j++ {
				fmt.Print(" ")
			}
			fmt.Print("*\n")
		}
	}
	fmt.Println()
}
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
```go
package main

import "fmt"

func main() {
	const rowQuantity = 7
	const columnQuantity = 10
	var i int
	var j int
	
	for i = 0; i < rowQuantity; i++ {
		if i % 2 == 0 {
			for j = 0; j < columnQuantity; j++ {
				fmt.Print("*")
			}
			fmt.Println()
		} else {
			fmt.Print("*")
			for j = 0; j < columnQuantity - 2; j++ {
				fmt.Print(" ")
			}
			fmt.Print("*\n")
		}
	}
	fmt.Println()
}
```

#### 5. Dibujar la siguiente figura en consola
```
*    
**   
***  
**** 
*****
```
```go
package main

import "fmt"

func main() {
	const rowQuantity = 5
	const columnQuantity = rowQuantity
	var i int
	var j int
	
	for i = 0; i < rowQuantity; i++ {
		for j = 0; j < columnQuantity; j++ {
			if j <= i {
				fmt.Print("*")
			} else {
				fmt.Print(" ")
			}
		}
		fmt.Println()
	}
}
```

#### 6. Dibujar la siguiente figura en consola
```
*****
**** 
***  
**   
*    
```
```go
package main

import "fmt"

func main() {
	const rowQuantity = 5
	const columnQuantity = rowQuantity
	var i int
	var j int
	
	for i = 0; i < rowQuantity; i++ {
		for j = 0; j < columnQuantity; j++ {
			if j < rowQuantity - i {
				fmt.Print("*")
			} else {
				fmt.Print(" ")
			}
		}
		fmt.Println()
	}
}
```

#### 7. Dibujar la siguiente figura en consola
```
    *
   **
  ***
 ****
*****
```
```go
package main

import "fmt"

func main() {
	const rowQuantity = 5
	const columnQuantity = rowQuantity
	var i int
	var j int
	
	for i = 0; i < rowQuantity; i++ {
		for j = 0; j < columnQuantity; j++ {
			if j < rowQuantity - 1 - i {
				fmt.Print(" ")
			} else {
				fmt.Print("*")
			}
		}
		fmt.Println()
	}
}
```

#### 8. Dibujar la siguiente figura en consola
```
*****
 ****
  ***
   **
    *
```
```go
package main

import "fmt"

func main() {
	const rowQuantity = 5
	const columnQuantity = rowQuantity
	var i int
	var j int
	
	for i = 0; i < rowQuantity; i++ {
		for j = 0; j < columnQuantity; j++ {
			if j < i {
				fmt.Print(" ")
			} else {
				fmt.Print("*")
			}
		}
		fmt.Println()
	}
}
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
```go
package main

import "fmt"

func main() {
	const rowQuantity = 9
	const columnQuantity = rowQuantity
	const middleColumn = columnQuantity / 2
	var i int
	var j int
	
	for i = 0; i < rowQuantity; i++ {
		for j = 0; j < columnQuantity; j++ {
			if i <= rowQuantity / 2 {
				if j >= middleColumn - i && j <= middleColumn + i {
					fmt.Print("*")
				} else {
					fmt.Print(" ")
				}
			} else {
				if j >= middleColumn - i && j <= middleColumn + i {
					fmt.Print("*")
				} else {
					fmt.Print(" ")
				}
			}
		}
		fmt.Println()
	}
}
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
```go
package main

import "fmt"

func main() {
	const rowQuantity = 10
	const columnQuantity = 10
	var i int
	var j int
	
	for i = 0; i < rowQuantity; i++ {
		for j = 1; j <= columnQuantity; j++ {
			if j % (i + 2) == 0 {
				fmt.Print(".")
			} else {
				fmt.Print("*")
			}
		}
		fmt.Println()
	}
}
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
```go
package main

import "fmt"

func main() {
	const minX int = -5
	const maxX int = 5
	const minY int = -5
	const maxY int = 5
	var x int
	var y int
	
	for y = maxY; y >= minY; y-- {
		for x = minX; x <= maxX; x++ {
			if x == 0 {
				fmt.Print("|")
			} else if y == 0 {
				fmt.Print("-")
			} else {
				fmt.Print(" ")
			}
		}
		fmt.Println()
	}
}
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
```go
package main

import "fmt"

func main() {
	const minX int = -5
	const maxX int = 5
	const minY int = -5
	const maxY int = 5
	var x int
	var y int
	
	for y = maxY; y >= minY; y-- {
		for x = minX; x <= maxX; x++ {
			if x == y {
				fmt.Print("*")
			} else if x == 0 {
				fmt.Print("|")
			} else if y == 0 {
				fmt.Print("-")
			} else {
				fmt.Print(" ")
			}
		}
		fmt.Println()
	}
}
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
```go
package main

import "fmt"
import "math"

func main() {
	const minX int = -10
	const maxX int = 10
	const minY int = -3
	const maxY int = 3
	var sinX float64
	var x int
	var y int
	
	for y = maxY; y >= minY; y-- {
		for x = minX; x <= maxX; x++ {
			sinX = math.Sin(float64(x) * math.Pi /  4) // hay que calcular el seno de x considerando que 1x -> Pi / 4
			if float64(y) > sinX - 0.0001 && float64(y) < sinX + 0.0001 { // si este fuera un == contra sinX nos perderíamos valores porque hay veces que el sinX == 0.0000000000000001 (y no es == 0)
				fmt.Print("*")
			} else if x == 0 {
				fmt.Print("|")
			} else if y == 0 {
				fmt.Print("-")
			} else {
				fmt.Print(" ")
			}
		}
		fmt.Println()
	}
}
```

### Segunda tanda
Abandonamos el dibujo en esta segunda tanda pero seguimos con los `for`. Vamos a estar jugando ahora con las condiciones de corte, repeticiones, confirmaciones y algunas cositas más.

#### 1. Imprimir una cuenta regresiva de 100 a 0 en saltos de a 3
```go
package main

import "fmt"

func main() {
	var i int

	for i = 100; i >= 0; i -= 3 {
		fmt.Println(i)
	}
}
```

#### 2. Solicitar el ingreso de dos números enteros e imprimir todo el rango de números que se encuentre entre ellos (hacerlo de menor a mayor)
```go
package main

import "fmt"

func main() {
	var i int
	var number1 int
	var number2 int
	var start int
	var end int

	fmt.Print("Ingrese dos números enteros: ")
	fmt.Scan(&number1, &number2)

	start = number1
	end = number2

	if number1 > number2 {
		start = number2
		end = number1
	}

	for i = start; i <= end; i++ {
		fmt.Println(i)
	}
}
```

#### 3. Solicitar el ingreso de dos números enteros e imprimir cuántos números múltiplos de 11 existen entre ellos
```go
package main

import "fmt"

func main() {
	var i int
	var number1 int
	var number2 int
	var start int
	var end int
	var count int

	fmt.Print("Ingrese dos números enteros: ")
	fmt.Scan(&number1, &number2)

	start = number1
	end = number2

	if number1 > number2 {
		start = number2
		end = number1
	}

	for i = start; i <= end; i++ {
		if i%11 == 0 {
			count++
		}
	}

	fmt.Printf("Existen %d múltiplos de 11\n", count)
}
```

#### 4. Solicitar el ingreso de un número entero e imprimir cuáles y cuántos divisores positivos tiene. Adicionalmente indicar si el número es primo
- Ej: 
```
> Ingrese un número entero: 21
> Divisores: 1, 3, 7, 21
> Tiene 5 divisores
> 21 no es primo
```
Recordatorio: Un número es primo si y solo si tiene unicamente 2 divisores: 1 y el mismo número (en rigor de verdad, la definición de primo contempla divisores negativos pero no nos interesa para este caso). Por ejemplo el número 5 es primo ya que los únicos divisores que tiene son 1 y 5.
```go
package main

import "fmt"

func main() {
	var i int
	var number int
	var divisors int

	fmt.Print("Ingrese un número entero: ")
	fmt.Scan(&number)

	fmt.Print("Divisores: ")
	for i = 1; i <= number; i++ {
		if number%i == 0 {
			fmt.Printf("%d, ", i)
			divisors++
		}
	}

	fmt.Printf("\nTiene %d divisores\n", divisors)
	if divisors == 2 {
		fmt.Printf("%d es primo\n", number)
	} else {
		fmt.Printf("%d no es primo\n", number)
	}
}
```

#### 5. Imprimir la tabla de multiplicar del 9 de la siguiente forma
```
9 x 1 = 9
9 x 2 = 18
9 x 3 = 27
...
9 x 10 = 90
```
```go
package main

import "fmt"

func main() {
	var i int
	const NUMBER int = 9

	for i = 1; i <= 10; i++ {
		fmt.Printf("%d x %d = %d\n", NUMBER, i, i*NUMBER)
	}
}
```

#### 6. Imprimir la tabla de multiplicar de cada uno de los números del 1 al 10 de la siguiente forma
```
Tabla del 1
1 x 1 = 1
1 x 2 = 2
...

Tabla del 2
2 x 1 = 2
2 x 2 = 4
...

Tabla del 10
10 x 1 = 10
10 x 2 = 10
...
10 x 10 = 100
```
```go
package main

import "fmt"

func main() {
	var i int
	var j int

	for i = 1; i <= 10; i++ {
		fmt.Printf("\nTabla del %d\n", i)
		for j = 1; j <= 10; j++ {
			fmt.Printf("%d x %d = %d\n", i, j, i*j)
		}
	}
}
```

#### 7. Emular una calculadora de la siguiente forma:
- Preguntar que operación desea realizar el usuario
    - `"+"` -> Suma ambos números
    - `"-"` -> Resta el segundo número al primero
    - `"*"` -> Multiplica ambos números
    - `"/"` -> Divide el primer número por el segundo
    - `"^"` -> Eleva el primer número al segundo
- Solicitar los números reales a operar
- Imprimir el resultado
- Preguntar al usuario si desea realizar otra operación
    - si indica que `"si"` -> reinciar la calculadora
    - si indica que `"no"` -> salir
    - si ingresa cualquier otra cosa -> repreguntar
```go
package main

import (
	"fmt"
	"math"
)

func main() {
	const PLUS string = "+"
	const MINUS string = "-"
	const TIMES string = "*"
	const DIVISION string = "/"
	const POWER string = "^"
	const YES string = "si"
	const NO string = "no"
	var operation string
	var answer string
	var number1 float32
	var number2 float32

	for answer != NO {
		fmt.Print("Ingrese que operacion desea realizar: ")
		fmt.Scan(&operation)

		fmt.Print("Ingrese los operandos: ")
		fmt.Scan(&number1, &number2)

		switch operation {
		case PLUS:
			fmt.Printf("%.2f + %.2f = %.2f\n", number1, number2, number1+number2)
		case MINUS:
			fmt.Printf("%.2f - %.2f = %.2f\n", number1, number2, number1-number2)
		case TIMES:
			fmt.Printf("%.2f x %.2f = %.2f\n", number1, number2, number1*number2)
		case DIVISION:
			if number2 == 0 {
				fmt.Println("No se puede realizar la operación")
			} else {
				fmt.Printf("%.2f / %.2f = %.2f\n", number1, number2, number1/number2)
			}
		case POWER:
			fmt.Printf("%.2f ^ %.2f = %.2f\n", number1, number2, math.Pow(float64(number1), float64(number2)))
		default:
			fmt.Printf("Operación erronea\n")
		}

		answer = ""
		for answer != NO && answer != YES {
			fmt.Print("Desea realizar otra operación? ")
			fmt.Scan(&answer)
		}
	}
}
```

#### 8. Realizar un programa que será utilizado por profesores universitarios para llevar el estado de una cursada dada que cumpla con los siguientes requisitos:
- Preguntar de que cursada se trata
- Pedir el ingreso de cuántas notas se van a procesar por alumno
- Por cada alumno, solicitar el ingreso de las notas y mostrar el promedio
- El sistema debe preguntar luego de cada alumno si todavía hay alguno pendiente y en caso de no haber más finalizar.
- Finalmente indicar de cuántos alumnos está compuesto el curso y cuál es el promedio general

Ej: 
```
Ingrese el nombre de la cursada: Matemática AR1B
Cuántas notas hay por alumno?: 3
Quedan alumnos por procesar (si/no)?: si
Ingrese nombre de alumno: Sol
Ingrese nota 1: 8
Ingrese nota 2: 10
Ingrese nota 3: 4
El promedio de Sol es 7.33
Quedan alumnos por procesar (si/no)?: si
Ingrese nombre de alumno: Axel
Ingrese nota 1: 2
Ingrese nota 2: 4
Ingrese nota 3: 4
El promedio de Axel es 3.33
Quedan alumnos por procesar (si/no)?: no
El curso Matemática AR1B está compuesto por 2 alumnos. El promedio general es: 5.33
```
```go
package main

import "fmt"

func main() {
	const YES string = "si"
	const NO string = "no"
	var courseName string
	var marksQuantity int
	var studentName string
	var studentMark float32
	var studentSum float32
	var studentQuantity int
	var courseSum float32
	var answer string
	var i int

	fmt.Print("Ingrese el nombre de la cursada: ")
	fmt.Scan(&courseName)
	for marksQuantity <= 0 {
		fmt.Print("Cuántas notas hay por alumno?: ")
		fmt.Scan(&marksQuantity)
	}

	studentQuantity = 0
	for answer != NO {
		fmt.Print("Quedan alumnos por procesar (si/no)?: ")
		fmt.Scan(&answer)
		if answer == YES {
			studentQuantity++
			studentSum = 0
			fmt.Print("Ingrese nombre del alumno: ")
			fmt.Scan(&studentName)
			for i = 0; i < marksQuantity; i++ {
				fmt.Printf("Ingrese nota %d: ", i+1)
				fmt.Scan(&studentMark)
				studentSum += studentMark
			}
			courseSum += studentSum
			fmt.Printf("El promedio de %s es %.2f\n", studentName, studentSum/float32(marksQuantity))
		}
	}
	fmt.Printf("El curso %s está compuesto por %d alumnos. El promedio general es: %.2f\n", courseName, studentQuantity, courseSum/float32(studentQuantity*marksQuantity))
}
```

### Tercer tanda
En esta Tercer tanda vamos a estar trabajando con arrays y slices. Como bien se aclara en el comienzo de esta **tercer parte**, no usar la librería de "strings".

#### 1. Dado un array de 5 enteros imprimir el tercer elemento
```go
package main

import "fmt"

func main() {
	var array [5]int = [5]int{10, 20, 30, 40, 50}
	fmt.Printf("el tercer elemento es %d\n", array[2])
}
```

#### 2. Dado un array de 5 enteros imprimirlos todos en pantalla de la siguiente forma
- `"el elemento <i> es <n>"` -> reemplazando `<i>` por el índice y `<n>` por el numero asociado (por cada elemento)
```go
package main

import "fmt"

func main() {
	var array [5]int = [5]int{10, 20, 30, 40, 50}
	var i int
	
	for i = 0; i < len(array); i++ {
		fmt.Printf("el elemento %d es %d\n", i, array[i])
	}
}
```

#### 3. Dado un array de 5 enteros imprimirlos igual que en el ejercicio anterior pero en el orden inverso
```go
package main

import "fmt"

func main() {
	var array [5]int = [5]int{10, 20, 30, 40, 50}
	var i int
	
	for i = len(array) - 1; i >= 0; i-- {
		fmt.Printf("el elemento %d es %d\n", i, array[i])
	}
}
```

#### 4. Dado un array de 5 enteros imprimir el resultado de sumarlos todos
```go
package main

import "fmt"

func main() {
	var array [5]int = [5]int{10, 20, 30, 40, 50}
	var i int
	var sum int
	
	for i = 0; i < len(array); i++ {
		sum += array[i]
	}
	fmt.Printf("la suma es %d\n", sum)
}
```

#### 5. Dado un array de 5 enteros imprimir el resultado de multiplicarlos todos
```go
package main

import "fmt"

func main() {
	var array [5]int = [5]int{10, 20, 30, 40, 50}
	var i int
	var mul int = 1
	
	for i = 0; i < len(array); i++ {
		mul *= array[i]
	}
	fmt.Printf("la multiplicacion es %d\n", mul)
}
```

#### 6. Dado un array de 5 enteros imprimir el mayor y el menor
```go
package main

import "fmt"

func main() {
	var array [5]int = [5]int{10, 20, 30, 40, 50}
	var i int
	var max int = array[0]
	var min int = array[0]
	
	for i = 1; i < len(array); i++ {
		if array[i] > max {
			max = array[i]
		}
		if array[i] < min {
			min = array[i]
		}
	}
	fmt.Printf("el maximo es %d\n", max)
	fmt.Printf("el minimo es %d\n", min)
}
```

#### 7. Dado un array de 5 enteros, solicitar el ingreso de un entero e imprimir todos los números del array que sean múltiplos del valor ingresado
```go
package main

import "fmt"

func main() {
	var array [5]int = [5]int{10, 20, 30, 40, 50}
	var i int
	var number int

	fmt.Print("ingrese un numero entero: ")
	fmt.Scan(&number)
	
	if number == 0 {
		fmt.Println("ninguno es multiplo de 0")
	} else {
		for i = 0; i < len(array); i++ {
			if array[i] % number == 0 {
				fmt.Printf("%d es multiplo de %d\n", array[i], number)
			}
		}
	}
}
```

#### 8. Dado un array de 5 letras, solicitar el ingreso de un número entero que representará el número de elemento que desea ver e imprimir
- `"el elemento <n> es <c>"` -> si el numero ingresado es válido (reemplazando `<n>` por el número ingresado y `<c>` por la letra asociada)
- `"está más allá de mis límites"` -> si el número ingresado es inválido
```go
package main

import "fmt"

func main() {
	var array [5]byte = [5]byte{'a', 'e', 'i', 'o', 'u'}
	var index int

	fmt.Print("ingrese el indice de la letra que desea ver: ")
	fmt.Scan(&index)
	
	if index < 0 || index >= len(array) {
		fmt.Println("está más allá de mis límites")
	} else {
		fmt.Printf("el elemento %d es %c\n", index, array[index])
	}
}
```

#### 9. Solicitar el ingreso de un string e imprimir la cantidad de caracteres que lo componen
```go
package main

import "fmt"

func main() {
	var aString string
	var i int
	var count int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString) // me permite poder ingresar string vacios
	
	// esto es intencional. Ver que la funcion len se le puede aplicar a un string al igual que a un array
	for i = 0; i < len(aString); i++ {
		count++
	}

	fmt.Printf("tiene %d caracteres\n", count)
}
```

#### 10. Solicitar el ingreso de un string e imprimir cada letra que lo compone separada por un guión
```go
package main

import "fmt"

func main() {
	var aString string
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	
	if len(aString) > 0 {
		fmt.Printf("%c", aString[0])
	}
	for i = 1; i < len(aString); i++ {
		fmt.Printf("-%c", aString[i])
	}
	fmt.Println()
}
```

#### 11. Solicitar el ingreso de un string y un char e imprimir
- `"<s> contiene <c>"` -> si el string ingresado contiene al char ingresado
- `"<s> no contiene ningun <c>"` -> si el string ingresado no contiene al char ingresado

(Reemplazando `<s>` por el string y `<c>` por el char)
```go
package main

import "fmt"

func main() {
	var aString string
	var searchedChar byte
	var contains bool
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	fmt.Print("ingrese un char a buscar: ")
	fmt.Scanf("%c\n", &searchedChar) // esto permite poder leer correctamente el char de teclado
	
	for i = 0; i < len(aString); i++ {
		if aString[i] == searchedChar {
			contains = true
			break
		}
	}
	if contains {
		fmt.Printf("%s contiene %c\n", aString, searchedChar)
	} else {
		fmt.Printf("%s no contiene ningun %c\n", aString, searchedChar)
	}
}
```

#### 12. Solicitar el ingreso de un string y un char e imprimir
- `"el string <s> contiene <n> veces el char <c>"`

(Reemplazando `<s>` por el string, `<c>` por el char y `<n>` por la cantidad de ocurrencias de `<c>` en `<s>`)
```go
package main

import "fmt"

func main() {
	var aString string
	var searchedChar byte
	var count int
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	fmt.Print("ingrese un char a buscar: ")
	fmt.Scanf("%c\n", &searchedChar)
	
	for i = 0; i < len(aString); i++ {
		if aString[i] == searchedChar {
			count++
		}
	}
	fmt.Printf("el string %s contiene %d veces el char %c\n", aString, count, searchedChar)
}
```

#### 13. Solicitar el ingreso de un string y un char e imprimir
- `"encontrado en <i>"` -> si se encontró el char en el string (mostrando el índice de la primer ocurrencia)
- `"no encontrado"` -> si no se encontró el char en el string
```go
package main

import "fmt"

func main() {
	var aString string
	var searchedChar byte
	var foundIndex int
	var charFound bool
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	fmt.Print("ingrese un char a buscar: ")
	fmt.Scanf("%c\n", &searchedChar)
	
	for i = 0; i < len(aString); i++ {
		if aString[i] == searchedChar {
			charFound = true
			foundIndex = i
			break
		}
	}
	if charFound {
		fmt.Printf("encontrado en %d\n", foundIndex)
	} else {
		fmt.Println("no encontrado")
	}
}
```

#### 14. Solicitar el ingreso de un string y un char e imprimir
- `"encontrado en [<i>,<i>,<i>,etc]"` -> si se encontró el char en el string (mostrando todos los índices de las ocurrencias encontradas)
- `"no encontrado"` -> si no se encontró el char en el string
```go
package main

import "fmt"

func main() {
	var aString string
	var searchedChar byte
	var foundIndexes []int
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	fmt.Print("ingrese un char a buscar: ")
	fmt.Scanf("%c\n", &searchedChar)
	
	for i = 0; i < len(aString); i++ {
		if aString[i] == searchedChar {
			foundIndexes = append(foundIndexes, i)
		}
	}
	if len(foundIndexes) > 0 {
		fmt.Printf("encontrado en %v\n", foundIndexes)
	} else {
		fmt.Println("no encontrado")
	}
}
```

#### 15. Solicitar el ingreso de un string e imprimir el mismo string reemplazando todas las `a` por `A`
```go
package main

import "fmt"

func main() {
	var aString string
	var convertedString []byte
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	
	for i = 0; i < len(aString); i++ {
		if aString[i] == 'a' {
			convertedString = append(convertedString, 'A')
		} else {
			convertedString = append(convertedString, aString[i])
		}
	}
	fmt.Printf("%s\n", convertedString) // hay que imprimirlo así dado que no fue declarado como string
}
```

#### 16. Solicitar el ingreso de un string e imprimirlo en mayúsculas
```go
package main

import "fmt"

func main() {
	var aString string
	var convertedString []byte
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	
	for i = 0; i < len(aString); i++ {
		if aString[i] >= 'a' && aString[i] <= 'z' {
			convertedString = append(convertedString, aString[i] & 0xDF) // la magia del operador AND a nivel de bits (notar que es el mismo simbolo que el AND lógico pero no es doble)
		} else {
			convertedString = append(convertedString, aString[i])
		}
	}
	fmt.Printf("%s\n", convertedString)
}
```

#### 17. Solicitar el ingreso de un string e imprimirlo en minúsculas
```go
package main

import "fmt"

func main() {
	var aString string
	var convertedString []byte
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	
	for i = 0; i < len(aString); i++ {
		if aString[i] >= 'A' && aString[i] <= 'Z' {
			convertedString = append(convertedString, aString[i] | 0x20) // de nuevo un operador OR a nivel de bits (analogo al operador OR lógico pero no es doble)
		} else {
			convertedString = append(convertedString, aString[i])
		}
	}
	fmt.Printf("%s\n", convertedString)
}
```

#### 18. Solicitar el ingreso de un string e imprimir si representa  un número válido
```go
package main

import "fmt"

func main() {
	var aString string
	var validNumber bool = true
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	
	for i = 0; i < len(aString); i++ {
		if aString[i] < '0' || aString[i] > '9' {
			validNumber = false
			break
		}
	}
	
	if validNumber {
		fmt.Printf("%s representa un numero valido\n", aString)
	} else {
		fmt.Printf("%s no es un numero valido\n", aString)
	}
}
```

#### 19. Solicitar el ingreso de un string y un número entero que representará un índice en el string e imprimir
- `"el string a partir de <i> es <s>"` -> si el numero ingresado es un indice válido 
- `"fuera de rango"` -> si el numero ingresado es un indice invalido

(Reemplazando `<i>` por el numero y `<s>` por el string a partir del índice `<i>` ingresado)
```go
package main

import "fmt"

func main() {
	var aString string
	var subIndex int
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	fmt.Print("ingrese un numero: ")
	fmt.Scanln(&subIndex)

	if subIndex < 0 || subIndex >= len(aString) {
		fmt.Println("fuera de rango")
	} else {
		fmt.Printf("el string a partir de %d es ", subIndex)
		for i = subIndex; i < len(aString); i++ {
			fmt.Printf("%c", aString[i])
		}
		fmt.Println()
	}
}
```

#### 20. Solicitar el ingreso de un string y dos números enteros que representará un índice de comienzo y de fin en el string e imprimir
- `"el string a partir de <i1> y hasta <i2> es <s>"` -> si los numeros ingresados son válidos 
- `"fuera de rango"` -> si al menos uno de los numeros ingresados es un indice invalido

(Reemplazando `<i1>`  e `<i2>` por los indices y `<s>` por el string a partir del índice `<i1>` y hasta `<i2>`)
```go
package main

import "fmt"

func main() {
	var aString string
	var startIndex int
	var endIndex int
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scanln(&aString)
	fmt.Print("ingrese el indice de inicio: ")
	fmt.Scanln(&startIndex)
	fmt.Print("ingrese el indice de fin: ")
	fmt.Scanln(&endIndex)

	if startIndex < 0 || startIndex > endIndex || endIndex >= len(aString) {
		fmt.Println("fuera de rango")
	} else {
		fmt.Printf("el string a partir de %d y hasta %d es ", startIndex, endIndex)
		for i = startIndex; i <= endIndex; i++ {
			fmt.Printf("%c", aString[i])
		}
		fmt.Println()
	}
}
```

#### 21. Solicitar el ingreso de dos strings e imprimir
- `"son iguales"` -> si representan el mismo string
- `"son parecidos"` -> si difieren en no mas de 2 letras
- `"son distintos"` -> si difieren en más de 2 letras
```go
package main

import "fmt"

func main() {
	var string1 string
	var string2 string
	var differences int
	var minLength int
	var i int

	fmt.Print("ingrese dos strings: ")
	fmt.Scanln(&string1, &string2)

	if len(string1) < len(string2) {
		minLength = len(string1)
		differences = len(string2) - len(string1)
	} else {
		minLength = len(string2)
		differences = len(string1) - len(string2)
	}
	for i = 0; i < minLength; i++ {
		if string1[i] != string2[i] {
			differences++
		}
	}
	if differences == 0 {
		fmt.Println("son iguales")
	} else if differences <= 2 {
		fmt.Println("son parecidos")
	} else {
		fmt.Println("son distintos")
	}
}
```

### Cuarta tanda
Aclaración: Donde se pida solicitar el ingreso de arrays (independiente del tipo solicitado) se deja al programador definir el tamaño del mismo al momento de compilación salvo que se indique lo contrario.

#### 1. Solicitar el ingreso de un array de dos números reales e imprimir el mayor
```go
package main

import "fmt"

func main() {
	var array [2]int
	var max int
	var i int

	for i = 0; i < len(array); i++ {
		fmt.Printf("Ingrese el elemento %d: ", array[i])
		fmt.Scan(&array[i])
	}

	if array[0] > array[1] {
		max = array[0]
	} else {
		max = array[1]
	}
	
	fmt.Printf("el mayor es: %d\n", max)
}
```

#### 2. Solicitar el ingreso de un array de dos números reales e imprimirlos en orden de mayor a menor
```go
package main

import "fmt"

func main() {
	var array [2]int
	var aux int
	var i int

	for i = 0; i < len(array); i++ {
		fmt.Printf("Ingrese el elemento %d: ", array[i])
		fmt.Scan(&array[i])
	}

	if array[0] < array[1] {
		aux = array[0]
		array[0] = array[1]
		array[1] = aux
	}
	fmt.Println(array)
}
```

#### 3. Solicitar el ingreso de un array de tres números reales e imprimir el mayor
```go
package main

import "fmt"

func main() {
	var array [3]int
	var max int
	var i int

	for i = 0; i < len(array); i++ {
		fmt.Printf("Ingrese el elemento %d: ", array[i])
		fmt.Scan(&array[i])
	}
	
	max = array[0]
	if array[1] > max {
		max = array[1]
	}
	if array[2] > max {
		max = array[2]
	}
	
	fmt.Printf("el mayor es: %d\n", max)
}
```

#### 4. Solicitar el ingreso de un array de tres números reales e imprimirlos en orden de mayor a menor
```go
package main

import "fmt"

func main() {
	var array [3]int
	var aux int
	var i int

	for i = 0; i < len(array); i++ {
		fmt.Printf("Ingrese el elemento %d: ", array[i])
		fmt.Scan(&array[i])
	}
	
	if array[1] > array[0] {
		aux = array[0]
		array[0] = array[1]
		array[1] = aux
	}

	if array[2] > array[1] {
		if array[2] > array[0] {
			aux = array[2]
			array[2] = array[1]
			array[1] = array[0]
			array[0] = aux
		} else {
			aux = array[2]
			array[2] = array[1]
			array[1] = aux
		}
	}
	
	fmt.Println(array)
}
```

#### 5. Solicitar el ingreso de un array de números reales (los que se quieran) e imprimir el mayor de todos ellos
```go
package main

import "fmt"

func main() {
	const cantidad int = 5
	var array [cantidad]int
	var max int
	var i int

	for i = 0; i < len(array); i++ {
		fmt.Printf("Ingrese el elemento %d: ", array[i])
		fmt.Scan(&array[i])
	}
	
	max = array[0]
	for i = 1; i < len(array); i++ {
		if array[i] > max {
			max = array[i]
		}
	}
	
	fmt.Printf("el mayor es: %d\n", max)
}
```

#### 6. Solicitar el ingreso de un array de números reales (los que se quieran) e imprimirlos en orden de mayor a menor (solo para valientes)
```go
package main

import "fmt"

func main() {
	const cantidad int = 5
	var array [cantidad]int
	var aux int
	var i int
	var j int

	for i = 0; i < len(array); i++ {
		fmt.Printf("Ingrese el elemento %d: ", array[i])
		fmt.Scan(&array[i])
	}
	
	for i = 0; i < len(array); i++ {
		for j = 0; j < len(array); j++ {
			if array[i] > array[j] {
				aux = array[i]
				array[i] = array[j]
				array[j] = aux
			} 
		}
	}
	
	fmt.Println(array)
}
```

#### 7. Dado un array de números reales, imprimirlos en orden de mayor a menor cortando prematuramente una vez ordenado el array (dependiendo de como resuelvan el ejercicio anterior este ejercicio está repetido o no) (solo para muy valientes)
```go
package main

import "fmt"

func main() {
	var array [5]int = [5]int{1, 32, 4, 42, 123}
	var aux int
	var isOrdered bool
	var i int
	var j int
	
	// este algoritmo de ordenamiento es llamado burbujeo
	for i = 0; i < len(array); i++ {
		isOrdered = true
		for j = 0; j < len(array) - 1; j++ {
			if array[j + 1] > array[j]  {
				isOrdered = false
				aux = array[j + 1]
				array[j + 1] = array[j]
				array[j] = aux
			}
		}
		if isOrdered {
			break
		}
	}
	
	fmt.Println(array)
}
```

#### 8. Solicitar el ingreso de dos arrays de números enteros de igual tamaño e imprimir si ambos arrays contienen los mismos elementos (sin importar el orden). Asumir que no hay repetidos
Ej: 

[1, 2, 3, 4] [2, 3, 1, 4] -> contienen los mismos elementos

[-1, 2, 3, 4] [2, -1, 3, 6] -> no contienen los mismos elementos
```go
package main

import "fmt"

func main() {
	const length int = 5
	var firstArray [length]int
	var secondArray [length]int
	var elementFound bool
	var i int
	var j int

	fmt.Printf("Ingrese el primer array de %d elementos: ", length)
	for i = 0; i < len(firstArray); i++ {
		fmt.Scan(&firstArray[i])
	}
	fmt.Printf("Ingrese el segundo array de %d elementos: ", length)
	for i = 0; i < len(secondArray); i++ {
		fmt.Scan(&secondArray[i])
	}

	for i = 0; i < len(firstArray); i++ {
		elementFound = false
		for j = 0; j < len(secondArray); j++ {
			if firstArray[i] == secondArray[j] {
				elementFound = true
				break
			}
		}
		if !elementFound {
			break
		}
	}
	
	if elementFound {
		fmt.Println("Ambos arrays contienen los mismos elementos")
	} else {
		fmt.Println("Ambos arrays no contienen los mismos elementos")
	}
}
```

#### 9. Solicitar el ingreso de dos strings e imprimir
- `"<s1> contiene al string <s2>"` -> si el primer string contiene al segundo
- `"<s1> no contiene al string <s2>"` -> si el segundo string no contiene al segundo
```go
package main

import "fmt"

func main() {
	var aString string
	var searchedString string
	var found bool
	var i int
	var j int

	fmt.Print("Ingrese el primer string: ")
	fmt.Scan(&aString)
	fmt.Print("Ingrese el string a buscar: ")
	fmt.Scan(&searchedString)

	for i = 0; i < len(aString); i++ {
		found = true
		for j = 0; j < len(searchedString); j++ {
			if aString[i + j] != searchedString[j] {
				found = false
				break
			}
		}
		if found {
			break
		}
	}
	
	if found {
		fmt.Println("Se encontró el string")
	} else {
		fmt.Println("No se encontró el string")
	}
}
```

#### 10. Solicitar el ingreso de tres strings e imprimir el resultado de hallar el segundo string en el primer string y reemplazarlo por el tercer string
Ej: 
- palito ito ote -> imprime `palote`
- confusion fu tor -> imprime `contorsion`
- delgadez dele to -> imprime `delgadez` (no se encontró el string a reemplazar)
```go
package main

import "fmt"

func main() {
	var aString string
	var searchedString string
	var replaceString string
	var replacedString []byte
	var found bool
	var i int
	var j int

	fmt.Print("Ingrese tres strings: ")
	fmt.Scan(&aString, &searchedString, &replaceString)

	for i = 0; i < len(aString); i++ {
		found = true
		for j = 0; j < len(searchedString); j++ {
			if aString[i + j] != searchedString[j] {
				found = false
				break
			}
		}
		if !found {
			replacedString = append(replacedString, aString[i])
		} else {
			for j = 0; j < len(replaceString); j++ {
				replacedString = append(replacedString, replaceString[j])
			}
			for j = i + len(searchedString); j < len(aString); j++ {
				replacedString = append(replacedString, aString[j])
			}
			break
		}
	}
	fmt.Printf("%s\n", replacedString)
}
```

#### 11. Solicitar el ingreso de un string y un array de strings e imprimir
- `"<s1> contiene al menos un string del array"` -> si el string contiene al menos un string del array
- `"<s1> no contiene ningun string del array"` -> si el string no contiene ningún string del array
```go
package main

import "fmt"

func main() {
	var aString string
	var searchedStrings [5]string
	var searchedString string
	var found bool
	var i int
	var j int
	var k int

	fmt.Print("Ingrese el string: ")
	fmt.Scan(&aString)
	fmt.Printf("Ingrese los %d strings a buscar: ", len(searchedStrings))
	for i = 0; i < len(searchedStrings); i++ {
		fmt.Scan(&searchedStrings[i])
	}
	
	for i = 0; i < len(searchedStrings); i++ {
		searchedString = searchedStrings[i]
		for j = 0; j < len(aString); j++ {
			found = true
			for k = 0; k < len(searchedString); k++ {
				if aString[j + k] != searchedString[k] {
					found = false
					break
				}
			}
			if found {
				break
			}
		}
		if found {
			break
		}
	}
	
	if found {
		fmt.Println("Se encontró el string")
	} else {
		fmt.Println("No se encontró el string")
	}
}
```

#### 12. Solicitar el ingreso de un string e imprimir
- `"<string> es palíndromo"` -> si el string ingresado es palíndromo
- `"<string> no es palíndromo"` -> si el string ingresado no es palíndromo
```go
package main

import "fmt"

func main() {
	var aString string
	var isPalindrome bool
	var i int

	fmt.Print("ingrese un string: ")
	fmt.Scan(&aString)

	isPalindrome = true
	for i = 0; i < len(aString)/2; i++ {
		if aString[i] != aString[len(aString)-i-1] {
			isPalindrome = false
			break
		}
	}

	if isPalindrome {
		fmt.Printf("%s es palíndromo\n", aString)
	} else {
		fmt.Printf("%s no es palíndromo\n", aString)
	}
}
```

### Cuarta tanda
En esta cuarta tanda vamos a ejercitar un concepto no menor en el mundo de los ciclos y arrays. Estamos hablando de arrays multidimensionales o ,mejor conocidos como, matrices. Cuando hablemos de filas y columnas nos vamos a referir a 
- fila -> el primer indice
- columna -> el segundo indice

#### 1. Dada una matriz de 3 x 3 de números enteros, imprimir el elemento 2 - 2
```go
package main

import "fmt"

func main() {
	var matrix [3][3]int = [3][3]int{[3]int{1,2,3}, [3]int{4,5,6}, [3]int{7,8,9}}

	fmt.Printf("el elemento 2 - 2 es %d\n", matrix[1][1])
}
```

#### 2. Dada una matriz de 3 x 3 de números enteros, imprimir toda la matriz de la siguiente forma
```
     c1 c2 c3  
    ---------- 
f1 | n1 n2 n3 |
f2 | n4 n5 n6 |
f3 | n7 n8 n9 |
    ---------- 
```
```go
package main

import "fmt"

func main() {
	var matrix [3][3]int = [3][3]int{[3]int{1,2,3}, [3]int{4,5,6}, [3]int{7,8,9}}
	var i int
	var j int

	fmt.Print("     c1 c2 c3\n")
	fmt.Print("    ----------\n")
	for i = 0; i < len(matrix); i++ {
		fmt.Printf("f%d | ", i + 1)
		for j = 0; j < len(matrix[i]); j++ {
			fmt.Printf("%2d ", matrix[i][j])
		}
		fmt.Println("|")
	}
	fmt.Print("    ----------\n")
}
```
#### 3. Dada una matriz de 3 x 3 de números enteros, imprimir el mayor de toda la matriz
```go
package main

import "fmt"
import "math"

func main() {
	var matrix [3][3]int = [3][3]int{[3]int{10,3,12}, [3]int{3,5,4}, [3]int{3,15,1}}
	var max int = math.MinInt64
	var i int
	var j int

	for i = 0; i < len(matrix); i++ {
		for j = 0; j < len(matrix[i]); j++ {
			if matrix[i][j] > max {
				max = matrix[i][j]
			}
		}
	}
	fmt.Printf("el máximo es: %d\n", max)
}
```

#### 4. Dada una matriz de 3 x 3 de números enteros, imprimir el menor de cada fila
```go
package main

import "fmt"
import "math"

func main() {
	var matrix [3][3]int = [3][3]int{[3]int{10,3,12}, [3]int{6,5,4}, [3]int{3,15,1}}
	var min int
	var i int
	var j int

	for i = 0; i < len(matrix); i++ {
		min = math.MaxInt64
		for j = 0; j < len(matrix[i]); j++ {
			if matrix[i][j] < min {
				min = matrix[i][j]
			}
		}
		fmt.Printf("el mínimo en la fila %d es: %d\n", i, min)
	}
}
```

#### 5. Dada una matriz de 3 x 3 de número enteros, imprimir el menor de cada columna
```go
package main

import "fmt"
import "math"

func main() {
	var matrix [3][3]int = [3][3]int{[3]int{10,30,12}, [3]int{6,5,4}, [3]int{3,15,1}}
	var min int
	var i int
	var j int

	for i = 0; i < len(matrix); i++ {
		min = math.MaxInt64
		for j = 0; j < len(matrix[i]); j++ {
			if matrix[j][i] < min { // esto se puede hacer si y solo si estamos seguros que la matriz es cuadrada
				min = matrix[j][i]
			}
		}
		fmt.Printf("el mínimo en la columna %d es: %d\n", i, min)
	}
}
```

#### 6. Dada una matriz de 3 x 3 de número enteros, imprimir si representa un cuadrante válido según las siguientes reglas
- la sumatoria de toda la matriz no debe exceder el valor `50`
- la sumatoria de cada fila no debe exceder el valor `30`
- la sumatoria de cada columna no debe ser menor al valor `10`
- ningún valor de la matriz debe exceder el valor `10`
- ningún valor de la matriz debe ser menor al valor `1`
```go
package main

import "fmt"

func main() {
	var matrix [3][3]int = [3][3]int{[3]int{4,3,3}, [3]int{3,4,3}, [3]int{3,3,4}}
	var isValid bool
	var matrixSum int = 0
	var rowSum int = 0
	var columnSum int = 0
	const maxMatrixValue int = 50
	const maxRowValue int = 30
	const minColumnValue int = 10
	const maxElementValue int = 10
	const minElementValue int = 1
	var i int
	var j int

	isValid = true
	for i = 0; i < len(matrix); i++ {
		rowSum = 0
		columnSum = 0
		for j = 0; j < len(matrix[i]); j++ {
			if matrix[i][j] > maxElementValue || matrix[i][j] < minElementValue {
				isValid = false
				break
			}
			matrixSum += matrix[i][j]
			rowSum += matrix[i][j]
			columnSum += matrix[j][i] // de nuevo esto solo se puede hacer si y solo si es una matriz cuadrada
		}
		if isValid {
			if rowSum > maxRowValue {
				isValid = false
				break
			}
			if columnSum < minColumnValue {
				isValid = false
				break
			}
		} else {
			break
		}	
	}
	
	if isValid && matrixSum > maxMatrixValue {
		isValid = false
	}
	
	if isValid {
		fmt.Println("es un cuadrante válido")
	} else {
		fmt.Println("es un cuadrante inválido")
	}
}
```

#### 7. Dada una matriz de 3 x 3 de número enteros, imprimir si representa un cuadrante válido para el SUDOKU según las siguientes reglas
- los números de cada casillero deben estar entre el `1` y el `9`
- no deben repetirse números en ningún casillero de la matriz
```go
package main

import "fmt"

func main() {
	var matrix [3][3]int = [3][3]int{[3]int{4,3,3}, [3]int{3,4,3}, [3]int{3,3,4}}
	var elementsOcurrences [9]int
	var isValid bool
	const minElementValue int = 1
	const maxElementValue int = 9
	var i int
	var j int

	isValid = true
	for i = 0; i < len(matrix); i++ {
		for j = 0; j < len(matrix); j++ {
			if matrix[i][j] > maxElementValue || matrix[i][j] < minElementValue {
				isValid = false
				break
			}
			elementsOcurrences[matrix[i][j] - 1]++
			if elementsOcurrences[matrix[i][j] - 1] > 1 {
				isValid = false
				break
			}
		}
		if !isValid {
			break
		}
	}
	
	if isValid {
		fmt.Println("es un cuadrante válido")
	} else {
		fmt.Println("es un cuadrante inválido")
	}
}
```

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
```go
package main

import "fmt"

func main() {
	var sudoku [9][9]int = [9][9]int{
		[9]int{1, 2, 3, 4, 5, 6, 7, 8, 9},
		[9]int{7, 8, 9, 1, 2, 3, 4, 5, 6},
		[9]int{4, 5, 6, 7, 8, 9, 1, 2, 3},
		[9]int{9, 1, 2, 3, 4, 5, 6, 7, 8},
		[9]int{6, 7, 8, 9, 1, 2, 3, 4, 5},
		[9]int{3, 4, 5, 6, 7, 8, 9, 1, 2},
		[9]int{8, 9, 1, 2, 3, 4, 5, 6, 7},
		[9]int{5, 6, 7, 8, 9, 1, 2, 3, 4},
		[9]int{2, 3, 4, 5, 6, 7, 8, 9, 1},
	}
	var i int
	var j int
	const line = "+ - - - + - - - + - - - +"

	for i = 0; i < len(sudoku); i++ {
		if i%3 == 0 {
			fmt.Printf("%s\n", line)
		}
		for j = 0; j < len(sudoku[i]); j++ {
			if j%3 == 0 {
				fmt.Printf("| %d ", sudoku[i][j])
			} else {
				fmt.Printf("%d ", sudoku[i][j])
			}
		}
		fmt.Println("|")
	}
	fmt.Printf("%s\n", line)

	var rowOcurrences [9]int
	var columnOcurrences [9]int
	var boxOcurrences [3][9]int
	const minValue int = 1
	const maxValue int = 9
	var element int
	var invertElement int
	var isValid bool

	isValid = true
	for i = 0; i < len(sudoku); i++ {
		rowOcurrences = [9]int{}
		columnOcurrences = [9]int{}
		if i%3 == 0 {
			boxOcurrences = [3][9]int{}
		}
		for j = 0; j < len(sudoku[i]); j++ {
			element = sudoku[i][j]
			invertElement = sudoku[j][i]
			if element > maxValue || element < minValue {
				isValid = false
				break
			}
			if invertElement > maxValue || invertElement < minValue {
				isValid = false
				break
			}
			rowOcurrences[element-1]++
			columnOcurrences[invertElement-1]++
			boxOcurrences[j/3][element-1]++
			if rowOcurrences[element-1] > 1 {
				isValid = false
				break
			}
			if columnOcurrences[invertElement-1] > 1 {
				isValid = false
				break
			}
			if boxOcurrences[j/3][element-1] > 1 {
				fmt.Print(boxOcurrences)
				isValid = false
				break
			}
		}
		if !isValid {
			break
		}
	}

	if isValid {
		fmt.Println("Es una solución válida para el SUDOKU")
	} else {
		fmt.Println("No es una solución válida para el SUDOKU")
	}
}
```

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
```go
package main

import "fmt"

func main() {
	const dimension int = 5
	var maze [dimension][dimension]bool = [dimension][dimension]bool{
		[dimension]bool{true,true,true,true,true}, 
		[dimension]bool{false,false,false,false,true}, 
		[dimension]bool{false,false,true,true,true}, 
		[dimension]bool{false,false,true,false,false},
		[dimension]bool{false,false,true,true,true},
	}
	var path []string = []string{}
	var blocked bool = false
	var arrived bool = false
	const NONE byte = 0
	const UP byte = 1
	const DOWN byte = 2
	const LEFT byte = 3
	const RIGHT byte = 4
	var lastMove byte = NONE
	var i int = 0
	var j int = 0

	if maze[i][j] {
		path = append(path, fmt.Sprintf("%d,%d", i, j))
	} else {
		blocked = true
	}

	for !arrived && !blocked {
		if i == dimension - 1 && j == dimension - 1 {
			arrived = true
			continue
		}
		
		if lastMove != LEFT && j + 1 < dimension && maze[i][j + 1] {
			lastMove = RIGHT
			j++
		} else if lastMove != UP && i + 1 < dimension && maze[i + 1][j] {
			lastMove = DOWN
			i++
		} else if lastMove != RIGHT && j > 0 && maze[i][j - 1] {
			lastMove = LEFT
			j--
		} else if lastMove != DOWN && i > 0 && maze[i - 1][j] {
			lastMove = UP
			i--
		} else {
			blocked = true
		}
		
		if !blocked {
			path = append(path, fmt.Sprintf("%d,%d", i, j))
		}
	}
	
	if blocked {
		fmt.Println("no existe un camino para llegar")
	} else if arrived {
		fmt.Print("el camino es: ")
		for i = 0; i < len(path) - 1; i++ {
			fmt.Printf("%s -> ", path[i])
		}
		fmt.Printf("%s\n", path[i])
	} else {
		fmt.Println("Error en la lógica. Ni se bloqueó, ni llegó.")
	}
}
```
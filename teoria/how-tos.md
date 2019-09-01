# How To's and What 's

## Como luce la estructura base de un programa en GO?
```go
package main

import "fmt"

func main() {
	fmt.Println("Hola Mundo!")
}
```

## Como declaro una variable?
```go
var number int = 1000
```

## Cómo cambio el valor de una variable?
```go
var number int = 1000
...
number = 2000
```

## Cómo declaro una constante?
```go
const number int = 1000
```

## Cómo cambio el valor de una constante?
Una constante no puede cambiar su valor a lo largo del programa, como el nombre lo indica es `constante`

## Cómo escribo/imprimo a pantalla?
Para imprimir a pantalla es necesario importar el paquete `"fmt"` y utilizar cualquiera de las funciones de impresión que define
```go
import "fmt"

func main() {
	...
	fmt.Print("Hola Mundo!")
	fmt.Println("Hola Mundo!")
	fmt.Printf("%s", "Hola Mundo!")
	...
}
```
De que va cada una?
```go
fmt.Print(valorAImprimir, otroValor, otro, etc..)
```
Imprime lo que se le pase por parámetro a la consola. Imprime todo tipo de dato y la cantidad que se quiera. Recibe de `1` a `n` parámetros.
```go
fmt.Println(valorAImprimir, otroValor, otro, etc..)
```
Funciona igual que `Print()` solo que agrega un salto de linea (`\n`) al final de la impresión
```go
fmt.Printf(formato, valorAImprimir, otroValor, otro, etc..)
```
Esta es la más compleja de todas pero a la vez la más maleable de todas. Espera como primer parámetro `string` que representará el formato de impresión y de ahí en adelante, los valores a imprimir. El `string` de formato puede ser simplemente una cadena de texto común y corriente o puede tener algunos caracteres especiales que serán reemplazados en el `string` final por los valores pasados posteriormente. Veamos un ejemplo:
Supongamos que queremos imprimir el siguiente texto
```
Mi nombre es Jose y tengo 20 años
```
y contamos con dos variables `nombre` y `anios` en nuestro programa. Si quisiéramos hacerlo con nuestra función `Print()` quedaría algo así
```go
fmt.Print("Mi nombre es ", nombre, " y tengo ", anios, " años")
```
Cómo verán no es difícil en si pero hay varias cosas de las que nos tenemos que hacer cargo y no olvidar como por ejemplo de los espacios entre el texto y las variables, de que los números se van a imprimir de una cierta forma y no podemos cambiar como lo hacen, etc..
Para tener un mayor control de la salida que queremos, podemos hacer uso de la función `Printf()`. Veamos como quedaría con esta función:
```go
fmt.Printf("Mi nombre es %s y tengo %d años", nombre, anios)
```
Si le prestaron atención habrán notado que aparecieron un `%s` y un `%d` en el `string` que le pasamos y que nuestras variables `nombre` y `anios` ahora las enviamos al final, es decir, le estamos pasando 3 parámetros, `formato`, `nombre` y `anios`. El concepto detrás de esto es:
- `%s` será reemplazado por el primer parámetro pasado que debe ser de tipo `string`
- `%d` será reemplazado por el segundo parámetro pasado que debe ser de tipo `int`

Esto nos permite tener mucho más control sobre la impresión final de salida pudiendo interpolar datos entre nuestro string sin tener que hacerlo a mano. Y no solo sirve para esto, también puede usarse para imprimir los datos con un formato específico. Por ejemplo si imprimiéramos un `float32` con `Print()` lo que veríamos sería esto
```go
var flotante float32 = 123.12356789
fmt.Print(flotante)
> "123.123566"
```
Y si lo hiciéramos con `Printf()` podríamos cambiar la cantidad de decimales con la que imprimirlo por ejemplo
```go
var flotante float32 = 123.12356789
fmt.Printf("%.2f", flotante)

> "123.12"
```
Así podemos ver que `Printf()` nos permite realizar impresiones más complejas con la dificultad extra de saber que formato usar. Los formatos más comunes son:
- `%s` Imprime un `string`
- `%d` Imprime un `int`
- `%f` Imprime un `float`
- `%t` Imprime un `bool`

Y sus variantes con tamaños mínimos de impresión (muy útil para hacer tablas)
- `%<width>s` Imprime un `string` con un mínimo de `width`
- `%<width>d` Imprime un `int` con un mínimo de `width`
- `%<width>.<precision>f` Imprime un `float` con un mínimo de `width` y con una precisión de `precision`
- `%<width>t` Imprime un `bool` con un mínimo de `width`

Y una yapa
- `%T` Imprime el tipo de dato

Algunos ejemplos
- Strings
```go
fmt.Printf("%s", "hola")

> "hola"
```
```go
fmt.Printf("%10s", "hola")

> "      hola" //largo 10 alineado a derecha
```
```go
fmt.Printf("%-10s", "hola")

> "hola      " //largo 10 alineado a izquierda
```
- Decimales
```go
fmt.Printf("%d", 1)

> "1"
```
```go
fmt.Printf("%5d", 1)

> "    1" //largo 5 alineado a derecha
```
```go
fmt.Printf("%-5d", 1)

> "1    " //largo 5 alineado a izquierda
```
- Flotantes
```go
fmt.Printf("%f", 1.232)

> "1.232"
```
```go
fmt.Printf("%11f", 1.232)

> "      1.232" //largo 11 alineado a derecha
```
```go
fmt.Printf("%.1f", 1.232)

> "1.2" // presicion 1 decimal
```
```go
fmt.Printf("%11.1f", 1.232)

> "        1.2" //largo 11 alineado a derecha con precision 1 decimal
```
```go
fmt.Printf("%-11.1f", 1.232)

> "1.2        " //largo 11 alineado a izquierda con precision 1 decimal
```
- Booleanos
```go
fmt.Printf("%t", true)

> "true"
```
```go
fmt.Printf("%10t", true)

> "      true" // largo 10 alineado a derecha
```
```go
fmt.Printf("%-10t", true)

> "true      " // largo 10 alineado a izquierda
```
- Mezclando lo que conocemos podemos lograr algo como esto:
```go
fmt.Printf("%-10s | %-10s | %8s | %4s \n", "Nombre", "Apellido", "DNI", "Edad")
fmt.Printf("%-10s | %-10s | %8s | %4d \n", "Jose", "Deniro", "24765394", 65)
fmt.Printf("%-10s | %-10s | %8s | %4d \n", "Mabel", "Stun", "29471323", 45)
fmt.Printf("%-10s | %-10s | %8s | %4d \n", "Federico", "Avalos", "30291423", 29)

> "Nombre     | Apellido   |      DNI | Edad"
> "Jose       | Deniro     | 24765394 |   65"
> "Mabel      | Stun       | 29471323 |   45"
> "Federico   | Avalos     | 30291423 |   29"
```

## Como leo del teclado?
Para leer de teclado es necesario importar el paquete `"fmt"` y utilizar cualquiera de las funciones de lectura que define
```go
import "fmt"

func main() {
	var unEntero int
	var unString string
	
	fmt.Scan(&unEntero)
	fmt.Scanln(&unString)
	fmt.Scanf("%d %s", &unEntero, &unString)
	...
}
```
La forma de leer del teclado (o sea de standard input o entrada estándar) es mediante nuestro querido amigo, el paquete `"fmt"`. `"fmt"` nos provee funciones para leer de teclado análogas a las funciones para imprimir:
```go
fmt.Scan(&valorALeer, &otroValor, &otro, etc...)
fmt.Scanln(&valorALeer, &otroValor, &otro, etc...)
fmt.Scanf(formato, &valorALeer, &otroValor, &otro, etc...)
```
De que va cada una?
```go
fmt.Scan(&valorALeer, &otroValor, &otro, etc...)
```
Esta función sencillamente lee de teclado tantos valores como variables se le hayan pasado. El tipo de dato leído tiene que coincidir con el tipo de dato de la variable. Los datos ingresados pueden estar separados tanto por espacios como por enters (nueva linea o `\n`).

```go
fmt.Scanln(&valorALeer, &otroValor, &otro, etc...)
```
Esta funciona igual que la anterior salvo que un enter (nueva linea o `\n`) es reconocido como final de entrada. Es decir, si usamos este tipo de lectura para leer 5 números, los 5 números tendrán que ser ingresados en una sola linea separadas por espacios.

```go
fmt.Scanf(formato, &valorALeer, &otroValor, &otro, etc...)
```
Funciona igual que las anteriores solo que los tipos de datos leído y el formato son especificados en el `string` de formato (ver Cómo escribo/imprimo a pantalla? para más detalle en el manejo del formato). En otras palabras, podemos crear nuestro propio formato de entrada separado por espacios, comas, guiones, etc.. lo que necesitemos.

Ahora hay varias cosas que pasamos por alto. Por lo menos tres:
1. Qué es ese `&` (andpersand) que va delante del nombre de las variables?
2. Qué pasa si el usuario ingresa mal un valor?
3. Siempre tengo que declarar una variable para poder leer un valor?

Vamos a responder de a una. La primera:
1. Qué es ese `&` (andpersand) que va delante del nombre de las variables?

Ese `&` es un operador unario (es decir, que solo necesita de un operando) que aplicado a un nombre de variable, nos devuelve la dirección en memoria de dicha variable. Suena a chino básico? no hay problema, la idea que subyace en esto es darle la capacidad a `Scanf()` de poder modificar nuestra variable. Por el momento lo vamos a dejar acá y más adelante lo veremos en detalle. Basta con saber que a `Scanf()` hay que pasarle nuestras variables con el `&` delante, es decir, hay que pasarle la dirección de nuestras variables.

2. Qué pasa si el usuario ingresa mal un valor?

Bueno, esto es un problema recurrente en cualquier programa que hagamos. El usuario siempre intentará jugar con él y probar cosas raras, por ejemplo, ingresar una letra cuando le pedimos que ingrese un numero. Ahora, cómo validamos la integridad de lo que nos ingresó en nuestro sistema? La respuesta es: **por el momento no vamos a hacerlo**. Hacerlo supone hablar y explayarse más en lo que se conoce como el manejo de errores en una aplicación o programa y todavía no es el momento. Lo que sí vamos a hacer es asumir que el usuario siempre nos ingresará el tipo de dato pedido aunque tal vez no sea correcto. Ejemplo: Pedimos que ingrese su edad, para eso leemos un entero del teclado. El usuario ingresa el número y nosotros solo validaremos que ese número sea válido, osea, que sea positivo y no mayor a 150 (por dar un ejemplo). O si le pidiéramos al usuario ingresar una respuesta de `si` o `no`, asumiremos que el usuario nos ingresa un `string` pero validaremos que el `string` es un `si` o un `no`.

3. Siempre tengo que declarar una variable para poder leer un valor del teclado?

La respuesta es sí. Necesitamos poder almacenar el valor leído en alguna variable por lo que es necesario previamente declarar una.

Veamos algunos ejemplos:
```go
var numero int
fmt.Print("Ingrese un número: ")
fmt.Scan(&numero)

fmt.Println("El número ingresado fue ", numero)

> "Ingrese un número: " 3 //numero ingresado por el usuario
> "El número ingresado fue 3"
```
```go
var numero1 int
var numero2 int
fmt.Print("Ingrese dos números: ")
fmt.Scan(&numero1, &numero2)

fmt.Println("La suma es ", numero1 + numero2)

> "Ingrese dos números: " 3 65 //Numeros separados por espacios ingresados por el usuario
> "La suma es 68"
```
```go
var numero1 int
var numero2 int
fmt.Print("Ingrese dos números: ")
fmt.Scan(&numero1, &numero2)

fmt.Println("La suma es ", numero1 + numero2)

> "Ingrese dos números: " 3 
> 65 // numeros separados por enters ingresados por el usuario
> "La suma es 68"
```
```go
var numero1 int
var numero2 int
fmt.Print("Ingrese dos números: ")
fmt.Scanln(&numero1, &numero2)

fmt.Println("La resta es ", numero1 - numero2)

> "Ingrese dos números: " 23 4 // numeros separados por espacios ingresados por el usuario
> "La resta es 19"
```
```go
var numero1 int
var numero2 int
fmt.Print("Ingrese dos números: ")
fmt.Scanln(&numero1, &numero2)

fmt.Println("La resta es ", numero1 - numero2)

> "Ingrese dos números: " 23 
> 4 // ERROR: numeros separados por enters ingresados por el usuario 
> "La resta es 19"
```

```go
var numero1 int
var numero2 int
fmt.Print("Ingrese dos números separados por un guión: ")
fmt.Scanf("%d-%d", &numero1, &numero2)

fmt.Println("La multiplicación es ", numero1 * numero2)

> "Ingrese dos números separados por un guión: " 20-3 // numeros separados por guión ingresados por el usuario
> "La multiplicación es 60"
```
```go
var unString string
fmt.Print("Ingrese su nombre: ")
fmt.Scanf("%s", &unString)

fmt.Printf("Hola ", unString, ", que gusto verte!")

> "Ingrese su nombre: " Leandro
> "Hola Leandro, que gusto verte"
```
Una última aclaración, notar como siempre antes de un `Scan()`, `Scanln()`, `Scanf()` hay un `Print()`, `Println()`, `Printf()`. Esto se debe a que es necesario indicarle al usuario qué es lo que queremos que haga. Si no pusiéramos esos prints, el usuario no sabría qué hacer, simplemente la pantalla se quedaría en negro y esperando el ingreso de datos que nunca van a ocurrir u ocurrirán por accidente.

## Cómo escribo un if?
La sintaxis más sencilla para escribir un `if` es la siguiente:
```go
if <expresion> {
	<codigo>
}
```
Donde:
- `<expresion>` es cualquier expresión válida que devuelva un `bool`. Puede ser tan sencilla como simplemente una variables `booleana` o tan compleja como una serie de `&&` y `||` con llamados a funciones o lo que fuere.
- `<codigo>` es cualquier bloque de código valido para GO que será ejecutado si y solo si la `<expresion>` es `true`

Ej: 
```go
var numero int
fmt.Print("Ingrese un numero: ")
fmt.Scan(&numero)

if numero > 45 {
	// Este bloque de codigo será ejecutado solo si numero es mayor a 45
	fmt.Print("El numero ingresado es mayor a 45")
}
```

También existe una variante más completa que permite ejecutar diferente código dependiendo si la expresión fue `true` o `false`
```go
if <expresion> {
	<codigoSiVerdadero>
} else {
	<codigoSiFalso>
}
```
Donde:
- `<expresion>` es cualquier expresión válida que devuelva un `bool`.
- `<codigoSiVerdadero>` es cualquier bloque de código valido para GO que será ejecutado si y solo si la `<expresion>` es `true`
- `<codigoSiFalso>` es cualquier bloque de código valido para GO que será ejecutado si y solo si la `<expresion>` es `false`

Ej:
```go
var edad int
fmt.Print("Ingrese su edad: ")
fmt.Scan(&edad)

if edad < 0 || edad > 150 {
	// Este bloque de código solo será ejecutado si la edad ingresada es menor a 0 o mayor a 150
	fmt.Print("La edad ingresada no parece ser muy confiable")
} else {
	// Y este bloque de código será ejecutado solo si edad está entre 0 y 150
	fmt.Printf("Me alegra saber que tienes %d años", edad)
}
```

Por último existe una forma de reflejar el caso de no solo 2 condiciones, sino más, tantas como se quieran. La idea detrás de esto es sencillamente proveer una forma elegante de escribir varios ifs anidados. Pensemos en el siguiente ejemplo. Quiero pedirle al usuario su edad y poder decirle en que etapa de su vida está. Si es un niño, un adolescente, un joven, un adulto o un anciano. Para eso pensemos como sería con lo que sabemos:
```go
var edad int
fmt.Print("Ingrese su edad: ")
fmt.Scan(&edad)

if edad < 15 {
	fmt.Print("niño")
} else {
	if edad < 25 {
		fmt.Print("adolescente")
	} else {
		if edad < 37 {
			fmt.Print("joven")
		} else {
			if edad < 65 {
				fmt.Print("adulto")
			} else {
				fmt.Print("anciano")
			}
		}
	}
}
```
El programa anterior funciona y no hay ningún inconveniente con él. Salvo, salvo, salvo que se nos complica un poco la lectura. La lógica detrás de el es correcta:
- `[-inf, 15)` -> es un niño
- `[15, 25)` -> es un adolescente
- `[25, 37)` -> es un joven
- `[37, 65)` -> es un adulto
- `[65, +inf)` -> es un anciano

Pero la forma de escribirlo es un poco confuso 
```go
if edad < 15 {
	// si edad < 15
} else {
	// sino, si edad >= 15
	if edad < 25 {
		// si edad < 25
	} else {
		// sino, si edad >= 25
		if edad < 37 {
			// si edad < 37
		} else {
			// sino, si edad >= 37
			...
		}
	}
}
```

En GO existe una forma mas concisa de escribir esta lógica y es la siguiente:
```go
if edad < 15 {
} else if edad < 25 {
} else if edad < 37 {
} ...
```
La estructura se llama `else if`. Si rehacemos el ejercicio utilizando esta nueva forma veremos que queda mucho mas claro y ordenado:
```go
var edad int
fmt.Print("Ingrese su edad: ")
fmt.Scan(&edad)

if edad < 15 {
	fmt.Print("niño")
} else if edad < 25 {
	fmt.Print("adolescente")
} else if edad < 37 {
	fmt.Print("joven")
} else if edad < 65 {
	fmt.Print("adulto")
} else {
	fmt.Print("anciano")
}
```
Se ve a simple vista la comodidad de uno con respecto al otro. De todas formas, queda a gusto del quién lee el usar una forma u otra.

## Qué operadores existen en GO?
Existen varios tipos de operadores en GO:

 1. Aritméticos
 2. De Comparación
 3. Lógicos

Veamos
1. Aritméticos
El valor que devuelven estos operadores depende de los operandos. Si se usa el operador con dos enteros, devolverá un entero, dos decimales devolverá un decimal

| Operador | Nombre | Aplica a | Explicación | Tipo
|--|--|--|--|--|
| + | suma | `int` `float` `string` | Suma dos elementos | Binario
| - | resta | `int` `float` | Resta dos números | Binario
| * | multiplicación | `int` `float` | Multiplica dos números | Binario
| / | división | `int` `float` | Divide dos números | Binario
| % | resto de la división | `int` | Divide dos números enteros y devuelve el resto | Binario
| ++ | suma 1 | `int` `float` | Es un equivalente a `x = x + 1` | Unario
| -- | resta 1 | `int` `float` | Es un equivalente a `x = x - 1` | Unario

2. De Comparación
El valor que devuelven estos operadores es siempre un `bool` independientemente del tipo de los operandos

| Operador | Nombre | Aplica a | Explicación | Tipo |
|--|--|--|--|--|
| == | igualdad | Todos | Devuelve si dos elementos son iguales | Binario
| != | desigualdad | Todos | Devuelve si dos elementos no son iguales | Binario
| < | menor | `int` `float` `string` | Devuelve si un elemento es menor que otro | Binario
| <= | menor o igual | `int` `float` `string` | Devuelve si un elemento es menor o igual que otro | Binario
| > | mayor | `int` `float` `string` | Devuelve si un elemento es mayor que otro | Binario
| >= | mayor o igual | `int` `float` `string` | Devuelve si un elemento es mayor o igual que otro | Binario

3. Lógicos
El valor que devuelven estos operadores son siempre `bool` y se aplican siempre a expresiones `bool`

| Operador | Nombre | Aplica a | Explicación | Tipo |
|--|--|--|--|--|
| && | y (and) | `bool` | Devuelve `true` si los dos operandos son `true` | Binario |
| \|\| | o (or) | `bool` | Devuelve `true` si al menos uno de los dos operandos es `true` | Binario |
| ! | no (not) | `bool` | Niega el valor de verdad del operando | Unario|


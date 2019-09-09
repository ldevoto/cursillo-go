## Primera parte 

#### 1. Imprimir en pantalla "Hola Mundo!"
```go
package main

import "fmt"

func main() {
	fmt.Println("Hola Mundo!")
}
```

#### 2. Definir una variable y cambiarle el valor
```go
package main

import "fmt"

func main() {
	var variable int = 10
	variable = 123
	fmt.Print(variable)
}
```

#### 3. Definir una constante y cambiarle el valor
```go
package main

import "fmt"

func main() {
	const constant int = 10
	constant = 123 //Error: cannot assign to constante
	fmt.Print(constant)
}
```

#### 4. Imprimir en pantalla las siguientes constantes:
```go
const soyUnByte byte = 12
const soyUnEntero int = 123123
const soyUnFloat float32 = 32123.432312
const soyUnString string = "un string"
const soyUnBool bool = true
```
```go
package main

import "fmt"

func main() {
	const soyUnByte byte = 12
	const soyUnEntero int = 123123
	const soyUnFloat float32 = 32123.432312
	const soyUnString string = "un string"
	const soyUnBool bool = true
	fmt.Println(soyUnByte)
	fmt.Println(soyUnEntero)
	fmt.Println(soyUnFloat)
	fmt.Println(soyUnString)
	fmt.Println(soyUnBool)
}
```

#### 5. Dado un numero entero, imprimir
-  `"es mayor a 50"` -> si es mayor a 50
-  `"es menor a 50"` -> si es menor a 50
-  `"es igual a 50` -> si es igual a 50
```go
package main

import "fmt"

func main() {
	const number int = 12
	if number > 50 {
		fmt.Println("es mayor a 50")
	} else if number < 50 {
		fmt.Println("es menor a 50")
	} else {
		fmt.Println("es igual a 50")
	}
}
```

#### 6. Cambiar el programa anterior para que el valor buscado sea variable. Es decir, una vez lo quiero correr con 50, después con 231, después con 1, etc.
-  `"es mayor a x"` -> si es mayor a x
-  `"es menor a x"` -> si es menor a x
-  `"es igual a x` -> si es igual a x
```go
package main

import "fmt"

func main() {
	const number int = 12
	const searchedNumber int = 23
	if number > searchedNumber {
		fmt.Println("es mayor a", searchedNumber)
	} else if number < searchedNumber {
		fmt.Println("es menor a", searchedNumber)
	} else {
		fmt.Println("es igual a", searchedNumber)
	}
}
```

#### 7. Dado un string, imprimir 
- `"es un saludo"` -> si el string es `"hola"` o `"chau"`
- `"no se que es"` -> si el string es cualquier otra cosa
```go
package main

import "fmt"

func main() {
	const aString string = "asdf"
	if aString == "hola" || aString == "chau" {
		fmt.Println("es un saludo")
	} else {
		fmt.Println("no se que es")
	}
}
```

#### 8. Dado dos booleanos, imprimir
- `"es totalmente cierto"` -> si ambos son `true`
- `"es totalmente falso"` -> si ambos son `false`
- `"no se que decirte, estoy confundido.."` -> si uno es `false` y el otro `true`
```go
package main

import "fmt"

func main() {
	const firstBool bool = true
	const secondBool bool = false
	if firstBool && secondBool {
		fmt.Println("es totalmente cierto")
	} else if !firstBool && !secondBool {
		fmt.Println("es totalmente falso")
	} else {
		fmt.Println("no se que decirte, estoy confundido..")
	}
}
```

#### 9. Dado un string, imprimir el largo.
- `"10"` -> si era `"Hola Mundo"`
- `"6"` -> si era `"jajaja"`
- `"0"` -> si era `""`
- etc..
```go
package main

import "fmt"

func main() {
	const aString string = "Hola Mundo"
	fmt.Println(len(aString))
}
```

#### 10. Dado dos string, imprimirlos en orden alfabético
```go
package main

import "fmt"

func main() {
	const firstString string = "anything"
	const secondString string = "something"
	if firstString > secondString {
		fmt.Println(secondString, " ", firstString)
	} else {
		fmt.Println(firstString, " ", secondString)
	}
}
```

#### 11. Dado un char, imprimir el número que lo representa
```go
package main

import "fmt"

func main() {
	const char byte = 'H'
	fmt.Printf("%d", char)
}
```

#### 12. Dado un número, imprimir el char que representa
```go
package main

import "fmt"

func main() {
	const num byte = 47
	fmt.Printf("%c", num)
}
```

#### 13. Dado dos chars, imprimir ambos ordenados de menor a mayor
```go
package main

import "fmt"

func main() {
	const firstChar byte = 'a'
	const secondChar byte = 'A'
	if firstChar > secondChar {
		fmt.Printf("%c %c", secondChar, firstChar)
	} else {
		fmt.Printf("%c %c", firstChar, secondChar)
	}
}
```
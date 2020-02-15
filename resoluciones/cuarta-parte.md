## Cuarta parte
Aclaración: En esta cuarta parte vamos a estar trabajando con funciones. Muy posiblemente noten que hay ejercicios que ya hicieron completa o parcialmente. Pueden tomar lo ya hecho para completarlos o bien realizarlos desde cero. E incluso pueden usar funciones programadas en ejercicios anteriores de esta misma parte.
No es necesario ningún paquete externo ni adicional salvo el ya usado `fmt`

No se pide armar el programa completo aunque se recomienda hacerlo como ayuda para probar el funcionamiento.

### Primera Tanda

#### 1. Construir una función que imprima en pantalla `Hola Mundo!`
```go
package main

import "fmt"

func main() {
	printGreeting()
}

func printGreeting() {
	fmt.Println("Hola Mundo!")
}
```

#### 2. Construir una función que dado un string imprima en pantalla dicho string.
```go
package main

import "fmt"

func main() {
	printString("Hola Mundo!")
}

func printString(aString string) {
	fmt.Println(aString)
}
```

#### 3. Construir una función que devuelva un string `Hola Mundo!`.
```go
package main

import "fmt"

func main() {
	fmt.Println(getString())
}

func getString() string {
	return "Hola Mundo!"
}
```

#### 4. Contruir una función que dado un string imprima en pantalla el string subrayado con guiones `-` (solo las palabras) (nombrarla `printTitle`).
Ej: 
```go
printTitle("Programar es divertido!")

> Programar es divertido!
> --------- -- ----------
```
```go
package main

import "fmt"

func main() {
	printTitle("Programar es divertido!")
}

func printTitle(title string) {
	var i int
	fmt.Println(title)
	for i = 0; i < len(title); i++ {
		if title[i] == ' ' {
			fmt.Print(" ")
		} else {
			fmt.Print("-")
		}
	}
	fmt.Println()
}
```

#### 5. Construir una función que dado dos números enteros devuelva la suma.
```go
package main

import "fmt"

func main() {
	fmt.Println(sum(4, 2))
}

func sum(num1 int, num2 int) int {
	return num1 + num2
}
```

#### 6. Construir una función que dado un string devuelva el string dado en color verde. (nombrarla `inGreen`)
Pista: buscar en google `console color escape codes`
```go
package main

import "fmt"

func main() {
	fmt.Println(inGreen("todo esto se imprimirá en verde"))
}

func inGreen(aString string) string {
	const reset string = "\u001b[0m"
	const green string = "\u001b[32m"
	return green + aString + reset
}
```

#### 7. Construir una función que dado un string devuelva el string dado en color rojo. (nombrarla `inRed`)
```go
package main

import "fmt"

func main() {
	fmt.Println(inRed("todo esto se imprimirá en rojo"))
}

func inRed(aString string) string {
	const reset string = "\u001b[0m"
	const red string = "\u001b[31m"
	return red + aString + reset
}
```

#### 8. Construir una función que dado un string devuelva el string dado en color amarillo. (nombrarla `inYellow`)
```go
package main

import "fmt"

func main() {
	fmt.Println(inYellow("todo esto se imprimirá en amarillo"))
}

func inYellow(aString string) string {
	const reset string = "\u001b[0m"
	const yellow string = "\u001b[33m"
	return yellow + aString + reset
}
```

#### 9. Construir una función que dado un string imprima en pantalla el string dado en color verde. (nombrarla `printInGreen`)
```go
package main

import "fmt"

func main() {
	printInGreen("todo esto se imprimirá en verde")
}

func printInGreen(aString string) {
	fmt.Println(inGreen(aString))
}

// Funcion anteriormente hecha
func inGreen(aString string) string {
	const reset string = "\u001b[0m"
	const green string = "\u001b[32m"
	return green + aString + reset
}
```

#### 10. Construir una función que dado un string imprima en pantalla el string dado en color rojo. (nombrarla `printInRed`)
```go
package main

import "fmt"

func main() {
	printInRed("todo esto se imprimirá en rojo")
}

func printInRed(aString string) {
	fmt.Println(inRed(aString))
}

// Funcion anteriormente hecha
func inRed(aString string) string {
	const reset string = "\u001b[0m"
	const red string = "\u001b[31m"
	return red + aString + reset
}
```

#### 11. Construir una función que dado un string imprima en pantalla el string dado en color amarillo. (nombrarla `printInYellow`)
```go
package main

import "fmt"

func main() {
	printInYellow("todo esto se imprimirá en amarillo")
}

func printInYellow(aString string) {
	fmt.Println(inYellow(aString))
}

// Funcion anteriormente hecha
func inYellow(aString string) string {
	const reset string = "\u001b[0m"
	const yellow string = "\u001b[33m"
	return yellow + aString + reset
}
```

#### 12. Construir una función que imprima en pantalla los 256 posibles colores de la siguiente forma (nombrarla `printAllColors`):
```
  0   1   2   3   4   5   6   7   8   9  10  11  12  13  14  15 
 16  17  18  19  20  21  22  23  24  25  26  27  28  29  30  31 
 32  33  34  35  36  37  38  39  40  41  42  43  44  45  46  47 
 48  49  50  51  52  53  54  55  56  57  58  59  60  61  62  63 
 64  65  66  67  68  69  70  71  72  73  74  75  76  77  78  79 
 80  81  82  83  84  85  86  87  88  89  90  91  92  93  94  95 
 96  97  98  99 100 101 102 103 104 105 106 107 108 109 110 111 
112 113 114 115 116 117 118 119 120 121 122 123 124 125 126 127 
128 129 130 131 132 133 134 135 136 137 138 139 140 141 142 143 
144 145 146 147 148 149 150 151 152 153 154 155 156 157 158 159 
160 161 162 163 164 165 166 167 168 169 170 171 172 173 174 175 
176 177 178 179 180 181 182 183 184 185 186 187 188 189 190 191 
192 193 194 195 196 197 198 199 200 201 202 203 204 205 206 207 
208 209 210 211 212 213 214 215 216 217 218 219 220 221 222 223 
224 225 226 227 228 229 230 231 232 233 234 235 236 237 238 239 
240 241 242 243 244 245 246 247 248 249 250 251 252 253 254 255

Donde cada número debe verse de un color distinto.
```
```go
package main

import "fmt"

func main() {
	printAllCollors()
}

func printAllCollors() {
	const reset string = "\u001b[0m"
	var i int
	for i = 0; i < 256; i++ {
		if i%16 == 0 {
			fmt.Println()
		}
		fmt.Printf("%s ", fmt.Sprintf("\u001b[38;5;%dm%3d", i, i))
	}
	fmt.Println(reset)
}
```

#### 13. Construir una función que dado un string devuelva el mismo string pero sin espacios por delante. (nombrarla `leftTrim`)
```go
package main

import "fmt"

func main() {
	fmt.Println(leftTrim("  los espacios ya no están"))
}

func leftTrim(aString string) string {
	var i int
	var trimmedString []byte
	for i = 0; i < len(aString); i++ {
		if aString[i] != ' ' {
			break
		}
	}
	for ; i < len(aString); i++ {
		trimmedString = append(trimmedString, aString[i])
	}
	return string(trimmedString)
}
```

#### 14. Construir una función que dado un string devuelva el mismo string pero sin espacios por detrás. (nombrarla `rightTrim`)
```go
package main

import "fmt"

func main() {
	fmt.Println(rightTrim("no se ve pero los espacios ya no están   "))
}

func rightTrim(aString string) string {
	var trimmedString []byte
	var lastChar int
	var i int
	
	for i = len(aString) - 1; i >= 0; i-- {
		if aString[i] != ' ' {
			lastChar = i + 1
			break
		}
	}
	trimmedString = make([]byte, lastChar)
	for i = 0; i < lastChar; i++ {
		trimmedString[i] = aString[i]
	}
	
	return string(trimmedString)
}
```

#### 15. Construir una función que dado un string devuelva el mismo string pero sin espacios por delante ni por detrás. (nombrarla `trim`)
```go
package main

import "fmt"

func main() {
	fmt.Println(trim("  sin espacios!  "))
}

func trim(aString string) string {
	return leftTrim(rightTrim(aString))
}

// Funcion anteriormente hecha
func leftTrim(aString string) string {
	var i int
	var trimmedString []byte
	for i = 0; i < len(aString); i++ {
		if aString[i] != ' ' {
			break
		}
	}
	for ; i < len(aString); i++ {
		trimmedString = append(trimmedString, aString[i])
	}
	return string(trimmedString)
}

// Funcion anteriormente hecha
func rightTrim(aString string) string {
	var trimmedString []byte
	var lastChar int
	var i int
	
	for i = len(aString) - 1; i >= 0; i-- {
		if aString[i] != ' ' {
			lastChar = i + 1
			break
		}
	}
	trimmedString = make([]byte, lastChar)
	for i = 0; i < lastChar; i++ {
		trimmedString[i] = aString[i]
	}
	
	return string(trimmedString)
}
```

#### 16. Construir una función que dado un string y un número entero devuelva el string a partir del número usado como índice. Si el índice es inválido devolver un string vacío.
```go
package main

import "fmt"

func main() {
	fmt.Println(getStringFrom("no sale pero esto si", 8))
}

func getStringFrom(aString string, index int) string {
	var subString []byte
	var i int
	if index < 0 || index >= len(aString) {
		return ""
	}
	for i = index; i < len(aString); i++ {
		subString = append(subString, aString[i])
	}
	return string(subString)
}
```

#### 17. Contruir una función que dado un string y dos números enteros devuelva el string a partir del primer número usado como índice de comienzo y usando el segundo como largo del string. Si el largo es mayor al posible restante, devolver el string hasta el final. Si el índice es inválido devolver un string vacío. (nombrarla `substr`).

```go
package main

import "fmt"

func main() {
	fmt.Println(substr("no sale, esto si y esto no", 5, 6))
}

func substr(aString string, index int, length int) string {
	var subString []byte
	var actualLength int
	var i int
	if index < 0 || index >= len(aString) {
		return ""
	}
	for i = index; i < len(aString) && i < index + length; i++ {
		subString = append(subString, aString[i])
		actualLength ++
	}
	return string(subString)
}
```

#### 18. Construir una función que dado un string y un byte devuelva un entero que represente el índice de la primer ocurrencia de ese byte en el string. Si el byte no se encuentra devolver `-1`. (nombrarla `findFirstChar`).

```go
package main

import "fmt"

func main() {
	fmt.Println(findFirstChar("El primer char va a ser 3", 'p'))
}

func findFirstChar(aString string, char byte) int {
	var found bool
	var i int
	for i = 0; i < len(aString); i++ {
		if aString[i] == char {
			found = true
			break
		}
	}
	if found {
		return i
	}
	return -1
}
```

#### 19. Construir una función que dado un string y un byte devuelva un slice de enteros que represente todos los índices con las ocurrencias de ese byte en el string (nombrarla `findAllChar`).
```go
package main

import "fmt"

func main() {
	fmt.Println(findAllChar("Va a imprimir [1 3]", 'a'))
}

func findAllChar(aString string, char byte) []int {
	var indexesFound []int
	var i int
	for i = 0; i < len(aString); i++ {
		if aString[i] == char {
			indexesFound = append(indexesFound, i)
		}
	}
	return indexesFound
}
```

#### 20. Construir una función que dados dos strings devuelva un entero que represente el índice de la primer ocurrencia del segundo string en el primero. Si el string no se encuentra devolver `-1`. (nombrarla `findFirstString`).
```go
package main

import "fmt"

func main() {
	fmt.Println(findFirstString("El primer string va a ser 17", "va"))
}

func findFirstString(aString string, searchedString string) int {
	var found bool
	var i int
	var j int

	for i = 0; i < len(aString); i++ {
		found = true
		for j = 0; j < len(searchedString); j++ {
			if i + j >= len(aString) || aString[i + j] != searchedString[j] {
				found = false
				break
			}
		}
		if found {
			break
		}
	}
	if found {
		return i
	}
	return -1
}
```

#### 21. Construir una función que dados dos strings devuelva un slice de enteros que contengan los índices de todas las ocurrencias del segundo string en el primero (nombrarla `findAllString`).
```go
package main

import "fmt"

func main() {
	fmt.Println(findAllString("Todos los strings van a ser [9 23]", " s"))
}

func findAllString(aString string, searchedString string) []int {
	var indexesFound []int
	var found bool
	var i int
	var j int

	for i = 0; i < len(aString); i++ {
		found = true
		for j = 0; j < len(searchedString); j++ {
			if i + j >= len(aString) || aString[i + j] != searchedString[j] {
				found = false
				break
			}
		}
		if found {
			indexesFound = append(indexesFound, i)
		}
	}
	return indexesFound
}
```

#### 22. Construir una función que dado un string y un byte devuelva un slice de strings que contenga todas las particiones del string obtenido de dividirlo por el byte. (nombrarla `splitByChar`)
Ej:
```go
var strings []string = splitByChar("Programar es divertido!", ' ')
fmt.Println(strings)

> ["Programar", "es", "divertido!"]
```
```go
package main

import "fmt"

func main() {
	fmt.Println(splitByChar("Programar es divertido!", ' '))
}

func splitByChar(aString string, char byte) []string {
	var splittedString []string
	var start string
	var end string
	var foundIndex int

	end = aString
	foundIndex = findFirstChar(end, char)
	for foundIndex != -1 {
		start = substr(end, 0, foundIndex)
		end = substr(end, foundIndex+1, len(end))
		if len(start) != 0 {
			splittedString = append(splittedString, start)
		}
		foundIndex = findFirstChar(end, char)
	}
	if len(end) != 0 {
		splittedString = append(splittedString, end)
	}

	return splittedString
}

// Funcion anteriormente hecha
func findFirstChar(aString string, char byte) int {
	var found bool
	var i int
	for i = 0; i < len(aString); i++ {
		if aString[i] == char {
			found = true
			break
		}
	}
	if found {
		return i
	}
	return -1
}

// Funcion anteriormente hecha
func substr(aString string, index int, length int) string {
	var subString []byte
	var actualLength int
	var i int
	if index < 0 || index >= len(aString) {
		return ""
	}
	for i = index; i < len(aString) && i < index+length; i++ {
		subString = append(subString, aString[i])
		actualLength++
	}
	return string(subString)
}
```

#### 23. Construir una función que dados dos strings devuelva un slice de strings que contenga todas las particiones del primer string obtenido de dividirlo por el segundo string. (nombrarla `splitByString`)
Ej:
```go
var strings []string = splitByString("la cama la puerta y la mesa", "la")
fmt.Println(strings)

> [" cama ", " puerta y ", " mesa"]
```
```go
package main

import "fmt"

func main() {
	fmt.Println(splitByString("la cama la puerta y la mesa", "la"))
}

func splitByString(aString string, searchedString string) []string {
	var splittedString []string
	var start string
	var end string
	var foundIndex int
	var i int

	if len(searchedString) == 0 {
		for i = 0; i < len(aString); i++ {
			splittedString = append(splittedString, string(aString[i]))
		}
	} else {
		end = aString
		foundIndex = findFirstString(end, searchedString)
		for foundIndex != -1 {
			start = substr(end, 0, foundIndex)
			end = substr(end, foundIndex+len(searchedString), len(end))
			if len(start) != 0 {
				splittedString = append(splittedString, start)
			}
			foundIndex = findFirstString(end, searchedString)
		}
		if len(end) != 0 {
			splittedString = append(splittedString, end)
		}
	}

	return splittedString
}

// Funcion anteriormente hecha
func findFirstString(aString string, searchedString string) int {
	var found bool
	var i int
	var j int

	for i = 0; i < len(aString); i++ {
		found = true
		for j = 0; j < len(searchedString); j++ {
			if i+j >= len(aString) || aString[i+j] != searchedString[j] {
				found = false
				break
			}
		}
		if found {
			break
		}
	}
	if found {
		return i
	}
	return -1
}

// Funcion anteriormente hecha
func substr(aString string, index int, length int) string {
	var subString []byte
	var actualLength int
	var i int
	if index < 0 || index >= len(aString) {
		return ""
	}
	for i = index; i < len(aString) && i < index+length; i++ {
		subString = append(subString, aString[i])
		actualLength++
	}
	return string(subString)
}
```

#### 24. Construir una función que dados dos strings devuelva un bool dependiendo si el primer string contiene al segundo. (nombrarla `contains`)
```go
package main

import "fmt"

func main() {
	fmt.Println(contains("veamos si lo contiene", "contiene"))
}

func contains(aString string, otherString string) bool {
	return findFirstString(aString, otherString) != -1
}

// Funcion anteriormente hecha
func findFirstString(aString string, searchedString string) int {
	var found bool
	var i int
	var j int

	for i = 0; i < len(aString); i++ {
		found = true
		for j = 0; j < len(searchedString); j++ {
			if i+j >= len(aString) || aString[i+j] != searchedString[j] {
				found = false
				break
			}
		}
		if found {
			break
		}
	}
	if found {
		return i
	}
	return -1
}
```

#### 25. Construir una función que dado un slice de strings y un string devuelva un string con todos los strings del slice concatenados con el string dado. (nombrarla `join`)
Ej:
```go
var strings []string = []string{"hola", "que", "tal?"}
var joinedString string = join(strings, "--")
fmt.Println(joinedString)

> "hola--que--tal?"
```
```go
package main

import "fmt"

func main() {
	fmt.Println(join([]string{"hola", "que", "tal?"}, "--"))
}

func join(strings []string, jointString string) string {
	var joinnedString []byte
	var i int
	var j int
	for i = 0; i < len(strings); i++ {
		for j = 0; j < len(strings[i]); j++ {
			joinnedString = append(joinnedString, strings[i][j])
		}
		if i != len(strings) - 1 {
			for j = 0; j < len(jointString); j++ {
				joinnedString = append(joinnedString, jointString[j])
			}
		}
	}
	return string(joinnedString)
}
```

#### 26. Construir una función que dado un un array de 3 enteros devuelva el mismo array pero invertido (nombrarla `reverseInt3`).
Para pensar: Qué pasaría si en lugar de 3 números enteros, ahora quisiéramos una de 4? y si quisiéramos otra de 5? qué desventaja presenta esto a utilizar un slice?
```go
package main

import "fmt"

func main() {
	fmt.Println(reverseInt3([3]int{1, 2 ,3}))
}

func reverseInt3(numbers [3]int) [3]int {
	var aux int
	var i int
	for i = 0; i < len(numbers) / 2; i++ {
		aux = numbers[i]
		numbers[i] = numbers[len(numbers)-1-i]
		numbers[len(numbers)-1-i] = aux
	}
	return numbers
}
```
Usar un array en lugar de un slice es mucho más restrictivo a la hora de querer crear funciones genéricas. Si quisiéramos nuevas funciones para array de 4, 5, 6, etc valores tendríamos que reescribir la misma función una y otra vez solo cambiando el tipo de dato que recibe y que devuelve la función.

#### 27. Construir una función que dado un slice de números enteros lo devuelva en orden inverso (nombrarla `reverseInt`).
Analizar el resultado del siguiente pedazo de código:
```go
const array3 [3]int = [3]int{1,2,3}
const slice3 []int = []int{1,2,3}
fmt.Printf("Array antes de la ejecución: %v\n", array3)
fmt.Printf("Slice antes de la ejecución: %v\n", slice3)
reverseInt3(array3) // ignoramos lo que nos devuelve
reverseInt(slice3) // ignoramos lo que nos devuelve
fmt.Printf("Array después de la ejecución: %v\n", array3)
fmt.Printf("Slice después de la ejecución: %v\n", slice3)
```
Qué vemos que sucede?
```go
package main

import "fmt"

func main() {
	fmt.Println(reverseInt([]int{1, 2 ,3, 4, 5, 6}))
}

func reverseInt(numbers []int) []int {
	var aux int
	var i int
	for i = 0; i < len(numbers) / 2; i++ {
		aux = numbers[i]
		numbers[i] = numbers[len(numbers)-1-i]
		numbers[len(numbers)-1-i] = aux
	}
	return numbers
}
```
Si ejecutamos el pedazo de código anterior veremos que en el primer caso el array queda con el orden original y por el contrario el slice cambia y queda con el orden inverso. Esto se debe a cómo están implementados estos dos tipos de datos. Podríamos decir que cuando uno pasa un array a una función lo que hace en realidad es pasar una copia de todo el array. Pero cuando uno pasa un slice (que por detrás usa un array) estamos pasando una copia del slice pero no del array. Por lo que al tocar el slice dentro de la función estamos afectando al slice de afuera (en realidad estamos afectando el array que está por detrás)

#### 28. Construir una función que dado un slice de strings lo devuelva en orden inverso (nombrarla `reverseString`).
```go
package main

import "fmt"

func main() {
	fmt.Println(reverseString([]string{"hola", "mundo", "!"}))
}

func reverseString(strings []string) []string {
	var aux string
	var i int
	for i = 0; i < len(strings) / 2; i++ {
		aux = strings[i]
		strings[i] = strings[len(strings)-1-i]
		strings[len(strings)-1-i] = aux
	}
	return strings
}
```

#### 29. Construir un programa que dado el siguiente texto imprima en pantalla
- la cantidad de párrafos que contiene
- la cantidad de palabras que contiene
- la cantidad de caracteres que contiene
- la cantidad de palabras `ipsum` que contiene
- el indice de la primer palabra `Quisque` que aparezca
- todo el texto pero de atrás hacia adelante (las palabras)
```
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas sit amet leo vitae magna rutrum vestibulum. Aliquam erat volutpat. Praesent id nulla et orci gravida mollis. Vestibulum tincidunt interdum nunc sit amet malesuada. Pellentesque aliquam risus in magna ornare, vel dignissim lectus maximus. Sed euismod mi nec est laoreet consequat. Nam et velit quis dolor mollis ullamcorper.
Integer sodales ornare risus, at vehicula enim dapibus eget. Quisque at interdum turpis. Cras interdum suscipit magna sit amet congue. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; In eu erat vel ante euismod tincidunt vel et nunc. Mauris varius scelerisque volutpat. Ut facilisis ipsum vitae hendrerit convallis. Proin tristique imperdiet dolor, eu laoreet massa suscipit non. Vestibulum lobortis, massa condimentum aliquet pulvinar, enim lectus imperdiet massa, placerat porta dui dolor ac mauris. Donec suscipit elit sem, id ultrices ligula placerat id. Vivamus dictum justo velit, eget tempus metus dapibus non. Sed venenatis est non lacus dapibus, posuere rutrum ipsum condimentum. Integer quis tincidunt libero, semper suscipit enim. Sed vel fermentum quam, et sodales dolor.
Mauris volutpat eros quis pretium sodales. Nulla ultricies mollis dui eget suscipit. Aenean pellentesque enim turpis, nec consectetur dolor pellentesque id. Vivamus in mi bibendum orci bibendum sagittis. Quisque dignissim imperdiet nibh, ut dignissim eros egestas vitae. Phasellus gravida vulputate congue. Nullam id rutrum lacus, nec tempor ipsum.
Quisque eu gravida enim. Quisque auctor neque ante, ac varius mi suscipit id. Integer nulla ex, accumsan vitae augue ac, faucibus iaculis elit. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Fusce condimentum erat eu tortor laoreet vulputate sed sed massa. Morbi fermentum elit vitae elit semper elementum at vulputate enim. Aenean id nisl mollis, pulvinar est sit amet, pretium diam.
Morbi nec leo vel massa hendrerit euismod eu ut nisl. Sed dignissim, risus et interdum interdum, eros augue viverra urna, a sodales sapien turpis a justo. Donec quis tortor ipsum. Praesent tempor sit amet purus non auctor. Mauris et pharetra quam. Ut sed laoreet nulla. Ut dictum aliquet neque, malesuada finibus enim imperdiet nec. Sed id ultrices mi. Sed sit amet venenatis turpis. Aliquam erat volutpat.
```
```go
package main

import "fmt"

func main() {
	const text string = `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas sit amet leo vitae magna rutrum vestibulum. Aliquam erat volutpat. Praesent id nulla et orci gravida mollis. Vestibulum tincidunt interdum nunc sit amet malesuada. Pellentesque aliquam risus in magna ornare, vel dignissim lectus maximus. Sed euismod mi nec est laoreet consequat. Nam et velit quis dolor mollis ullamcorper.
	Integer sodales ornare risus, at vehicula enim dapibus eget. Quisque at interdum turpis. Cras interdum suscipit magna sit amet congue. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; In eu erat vel ante euismod tincidunt vel et nunc. Mauris varius scelerisque volutpat. Ut facilisis ipsum vitae hendrerit convallis. Proin tristique imperdiet dolor, eu laoreet massa suscipit non. Vestibulum lobortis, massa condimentum aliquet pulvinar, enim lectus imperdiet massa, placerat porta dui dolor ac mauris. Donec suscipit elit sem, id ultrices ligula placerat id. Vivamus dictum justo velit, eget tempus metus dapibus non. Sed venenatis est non lacus dapibus, posuere rutrum ipsum condimentum. Integer quis tincidunt libero, semper suscipit enim. Sed vel fermentum quam, et sodales dolor.
	Mauris volutpat eros quis pretium sodales. Nulla ultricies mollis dui eget suscipit. Aenean pellentesque enim turpis, nec consectetur dolor pellentesque id. Vivamus in mi bibendum orci bibendum sagittis. Quisque dignissim imperdiet nibh, ut dignissim eros egestas vitae. Phasellus gravida vulputate congue. Nullam id rutrum lacus, nec tempor ipsum.
	Quisque eu gravida enim. Quisque auctor neque ante, ac varius mi suscipit id. Integer nulla ex, accumsan vitae augue ac, faucibus iaculis elit. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Fusce condimentum erat eu tortor laoreet vulputate sed sed massa. Morbi fermentum elit vitae elit semper elementum at vulputate enim. Aenean id nisl mollis, pulvinar est sit amet, pretium diam.
	Morbi nec leo vel massa hendrerit euismod eu ut nisl. Sed dignissim, risus et interdum interdum, eros augue viverra urna, a sodales sapien turpis a justo. Donec quis tortor ipsum. Praesent tempor sit amet purus non auctor. Mauris et pharetra quam. Ut sed laoreet nulla. Ut dictum aliquet neque, malesuada finibus enim imperdiet nec. Sed id ultrices mi. Sed sit amet venenatis turpis. Aliquam erat volutpat.`

	fmt.Printf("Contiene %d páraffos.\n", len(splitByString(text, "\n")))
	fmt.Printf("Contiene %d palabras\n", len(splitByString(join(splitByString(text, "\n"), " "), " ")))
	fmt.Printf("Contiene %d caracteres\n", len(text))
	fmt.Printf("Contiene %d palabras ipsum\n", len(findAllString(text, "ipsum")))
	fmt.Printf("La primer palabra Quisque se encuentra en el indice %d\n", findFirstString(text, "Quisque"))
	fmt.Printf("EL texto de atrás hacia adelante es: \n%s\n", reverseString(splitByString(text, " ")))
}

func splitByString(aString string, searchedString string) []string {
	var splittedString []string
	var start string
	var end string
	var foundIndex int
	var i int

	if len(searchedString) == 0 {
		for i = 0; i < len(aString); i++ {
			splittedString = append(splittedString, string(aString[i]))
		}
	} else {
		end = aString
		foundIndex = findFirstString(end, searchedString)
		for foundIndex != -1 {
			start = substr(end, 0, foundIndex)
			end = substr(end, foundIndex+len(searchedString), len(end))
			if len(start) != 0 {
				splittedString = append(splittedString, start)
			}
			foundIndex = findFirstString(end, searchedString)
		}
		if len(end) != 0 {
			splittedString = append(splittedString, end)
		}
	}

	return splittedString
}

func findFirstString(aString string, searchedString string) int {
	var found bool
	var i int
	var j int

	for i = 0; i < len(aString); i++ {
		found = true
		for j = 0; j < len(searchedString); j++ {
			if i+j >= len(aString) || aString[i+j] != searchedString[j] {
				found = false
				break
			}
		}
		if found {
			break
		}
	}
	if found {
		return i
	}
	return -1
}

func substr(aString string, index int, length int) string {
	var subString []byte
	var actualLength int
	var i int
	if index < 0 || index >= len(aString) {
		return ""
	}
	for i = index; i < len(aString) && i < index+length; i++ {
		subString = append(subString, aString[i])
		actualLength++
	}
	return string(subString)
}

func findAllString(aString string, searchedString string) []int {
	var indexesFound []int
	var found bool
	var i int
	var j int

	for i = 0; i < len(aString); i++ {
		found = true
		for j = 0; j < len(searchedString); j++ {
			if i+j >= len(aString) || aString[i+j] != searchedString[j] {
				found = false
				break
			}
		}
		if found {
			indexesFound = append(indexesFound, i)
		}
	}
	return indexesFound
}

func reverseString(strings []string) []string {
	var aux string
	var i int
	for i = 0; i < len(strings)/2; i++ {
		aux = strings[i]
		strings[i] = strings[len(strings)-1-i]
		strings[len(strings)-1-i] = aux
	}
	return strings
}

func join(strings []string, jointString string) string {
	var joinnedString []byte
	var i int
	var j int
	for i = 0; i < len(strings); i++ {
		for j = 0; j < len(strings[i]); j++ {
			joinnedString = append(joinnedString, strings[i][j])
		}
		if i != len(strings)-1 {
			for j = 0; j < len(jointString); j++ {
				joinnedString = append(joinnedString, jointString[j])
			}
		}
	}
	return string(joinnedString)
}
```

#### 30. Construir una función que dado un slice de strings devuelva un slice de números enteros donde cada elemento es el largo del string en la misma posición del slice dado (nombrarla `mapToLength`).
Ej:
```go
var strings []string = []string{"hola", "mundo", "!"}
var lengths []int = mapToLength(strings)
fmt.Println(lengths)

> [4, 5, 1]
```
```go
package main

import "fmt"

func main() {
	fmt.Println(mapToLength([]string{"hola", "mundo", "!"}))
}

func mapToLength(strings []string) []int {
	var lengths []int
	var i int
	for i = 0; i < len(strings); i++ {
		lengths = append(lengths, len(strings[i]))
	}
	return lengths
}
```

#### 31. Construir una función que dado un slice de bools devuelva true si todos los valores del slice son true o false si no (nombrarla `allTrue`).
```go
package main

import "fmt"

func main() {
	fmt.Println(allTrue([]bool{true, true, false, true}))
}

func allTrue(bools []bool) bool {
	var isTrue bool = true
	var i int
	for i = 0; i < len(bools); i++ {
		if !bools[i] {
			isTrue = false
			break
		} 
	}
	return isTrue
}
```

#### 32. Construir una función que dado un slice de bools devuelva true si al menos un valor del slice es true o false si no (nombrarla `anyTrue`).
```go
package main

import "fmt"

func main() {
	fmt.Println(anyTrue([]bool{true, true, false, true}))
}

func anyTrue(bools []bool) bool {
	var someTrue bool
	var i int
	for i = 0; i < len(bools); i++ {
		if bools[i] {
			someTrue = true
			break
		} 
	}
	return someTrue
}
```

#### 33. Construir una función que dado un slice de números decimales devuelva la suma de todos (nombrarla `sumFloat`).
```go
package main

import "fmt"

func main() {
	fmt.Println(sumFloat([]float64{2.2, 3.1, 5.9, 4}))
}

func sumFloat(floats []float64) float64 {
	var sum float64
	var i int
	for i = 0; i < len(floats); i++ {
		sum += floats[i]
	}
	return sum
}
```

#### 34. Construir una función que dado un slice de números decimales devuelva el promedio de todos (nombrarla `averageFloat`).
```go
package main

import "fmt"

func main() {
	fmt.Println(averageFloat([]float64{2.2, 3.1, 5.9, 4}))
}

func averageFloat(floats []float64) float64 {
	var sum float64
	var i int
	for i = 0; i < len(floats); i++ {
		sum += floats[i]
	}
	if len(floats) == 0 {
		return 0
	}
	return sum / float64(len(floats))
}
```

#### 35. Construir una función que dado un slice de números decimales devuelva un array de 2 números decimales donde en la posición 0 estará el mayor y en la 1 el menor de todos. Si el slice no tiene elementos, devolver el array con 0 en ambos valores (nombrarla `minMaxFloat`).
```go
package main

import "fmt"

func main() {
	fmt.Println(minMaxFloat([]float64{2.2, 3.1, 5.9, 4}))
}

func minMaxFloat(floats []float64) [2]float64 {
	var minMaxArr [2]float64
	var min float64
	var max float64
	var i int
	if len(floats) > 0 {
		min = floats[0]
		max = floats[0]
	}
	for i = 0; i < len(floats); i++ {
		if floats[i] > max {
			max = floats[i]
		}
		if floats[i] < min {
			min = floats[i]
		}
	}
	minMaxArr = [2]float64{max, min}
	return minMaxArr
}
```

#### 36. Construir una función que dado un slice de números enteros devuelva un slice con los números ordenados de menor a mayor (nombrarla `ascOrderInt`).
```go
package main

import "fmt"

func main() {
	fmt.Println(ascOrderInt([]int{7, 3, 1, 5, 4, 2, 6}))
}

func ascOrderInt(numbers []int) []int {
	var ordered bool
	var aux int
	var i int
	var j int
	for i = 0; i < len(numbers); i++ {
		ordered = true
		for j = 0; j < len(numbers) - 1; j++ {
			if numbers[j] > numbers[j+1] {
				aux = numbers[j]
				numbers[j] = numbers[j+1]
				numbers[j+1] = aux
				ordered = false
			}
		}
		if ordered {
			break
		}
	}
	return numbers
}
```

#### 37. Construir una función que dado un slice de números enteros devuelva un slice con los números ordenados de mayor a menor (nombrarla `descOrderInt`).
```go
package main

import "fmt"

func main() {
	fmt.Println(descOrderInt([]int{7, 3, 1, 5, 4, 2, 6}))
}

func descOrderInt(numbers []int) []int {
	var ordered bool
	var aux int
	var i int
	var j int
	for i = 0; i < len(numbers); i++ {
		ordered = true
		for j = 0; j < len(numbers) - 1; j++ {
			if numbers[j] < numbers[j+1] {
				aux = numbers[j]
				numbers[j] = numbers[j+1]
				numbers[j+1] = aux
				ordered = false
			}
		}
		if ordered {
			break
		}
	}
	return numbers
}
```

#### 38. Construir una función que dado un número entero devuelva un string con el día de la semana que representa (nombrarla `dayOfWeek`) según la siguiente tabla:
- 1 -> Domingo
- 2 -> Lunes
- 3 -> Martes
- 4 -> Miércoles
- 5 -> Jueves
- 6 -> Viernes
- 7 -> Sábado
- otro -> Error
```go
package main

import "fmt"

func main() {
	fmt.Println(dayOfWeek(1))
}

func dayOfWeek(day int) string {
	switch day {
	case 1: return "Domingo"
	case 2: return "Lunes"
	case 3: return "Martes"
	case 4: return "Miércoles"
	case 5: return "Jueves"
	case 6: return "Viernes"
	case 7: return "Sábado"
	default: return "Error"
	}
}
```

#### 39. Construir una función que corrobore el funcionamiento de la función anterior. Debe probar todos los posibles casos (puede crear todas las funciones adicionales que crea convenientes)  e imprimir 
- `Caso <x> -> OK` -> si la función devolvió lo esperado
- `Caso <x> -> ERROR` -> si la función no devolvió lo esperado

El `OK` debe aparecer en verde y el `ERROR` debe aparecer en rojo. El `<x>` debe ser reemplazado por el número probado en cada caso.
```go
package main

import "fmt"

func main() {
	checkDayOfWeek()
}

func checkDayOfWeek() {
	const cases int = 8
	var inputs [cases]int = [cases]int{1,2,3,4,5,6,7,8}
	var outputs [cases]string = [cases]string{"Domingo", "Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado", "Error"}
	var i int
	for i = 0; i < cases; i++ {
		fmt.Printf("Caso %d -> %s\n", inputs[i], getStatus(dayOfWeek(inputs[i]) == outputs[i]))
	} 
}

func getStatus(result bool) string {
	if result {
		return inGreen("OK")
	} else {
		return inRed("ERROR")
	}
}

func dayOfWeek(day int) string {
	switch day {
	case 1: return "Domingo"
	case 2: return "Lunes"
	case 3: return "Martes"
	case 4: return "Miércoles"
	case 5: return "Jueves"
	case 6: return "Viernes"
	case 7: return "Sábado"
	default: return "Error"
	}
}

func inGreen(aString string) string {
	const reset string = "\u001b[0m"
	const green string = "\u001b[32m"
	return green + aString + reset
}

func inRed(aString string) string {
	const reset string = "\u001b[0m"
	const red string = "\u001b[31m"
	return red + aString + reset
}
```

#### 40. Construir una función que corrobore el funcionamiento de la función `leftTrim`, `rightTrim` y `trim`. Debe probar todos los posibles casos por cada función (puede crear todas las funciones adicionales que crea convenientes)  e imprimir 
- `Caso <x> -> OK` -> si la función devolvió lo esperado
- `Caso <x> -> ERROR` -> si la función no devolvió lo esperado

El `OK` debe aparecer en verde y el `ERROR` debe aparecer en rojo. El `<x>` debe ser reemplazado por el string probado en cada caso.
```go
package main

import "fmt"

func main() {
	var inputs []string = []string{"", "  ", "hola", "  hola", "hola  ", "  hola  ", "  hola mundo  "}
	var leftTrimOutputs []string = []string{"", "", "hola", "hola", "hola  ", "hola  ", "hola mundo  "}
	var rightTrimOutputs []string = []string{"", "", "hola", "  hola", "hola", "  hola", "  hola mundo"}
	var trimOutputs []string = []string{"", "", "hola", "hola", "hola", "hola", "hola mundo"}

	fmt.Println("\nProbando leftTrim:")
	checkFunction(leftTrim, inputs, leftTrimOutputs)
	fmt.Println("\nProbando rightTrim:")
	checkFunction(rightTrim, inputs, rightTrimOutputs)
	fmt.Println("\nProbando trim:")
	checkFunction(trim, inputs, trimOutputs)
}

func checkFunction(testedFunction func(string) string, inputs []string, outputs []string) {
	var i int
	for i = 0; i < len(inputs); i++ {
		fmt.Printf("Caso %q -> %s\n", inputs[i], getStatus(testedFunction(inputs[i]) == outputs[i]))
	}
}

func getStatus(result bool) string {
	if result {
		return inGreen("OK")
	} else {
		return inRed("ERROR")
	}
}

func leftTrim(aString string) string {
	var i int
	var trimmedString []byte
	for i = 0; i < len(aString); i++ {
		if aString[i] != ' ' {
			break
		}
	}
	for ; i < len(aString); i++ {
		trimmedString = append(trimmedString, aString[i])
	}
	return string(trimmedString)
}

func rightTrim(aString string) string {
	var trimmedString []byte
	var lastChar int
	var i int

	for i = len(aString) - 1; i >= 0; i-- {
		if aString[i] != ' ' {
			lastChar = i + 1
			break
		}
	}
	trimmedString = make([]byte, lastChar)
	for i = 0; i < lastChar; i++ {
		trimmedString[i] = aString[i]
	}

	return string(trimmedString)
}

func trim(aString string) string {
	return leftTrim(rightTrim(aString))
}

func inGreen(aString string) string {
	const reset string = "\u001b[0m"
	const green string = "\u001b[32m"
	return green + aString + reset
}

func inRed(aString string) string {
	const reset string = "\u001b[0m"
	const red string = "\u001b[31m"
	return red + aString + reset
}
```
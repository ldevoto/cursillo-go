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

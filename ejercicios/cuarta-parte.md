## Cuarta parte
Aclaración: En esta cuarta parte vamos a estar trabajando con funciones. Muy posiblemente noten que hay ejercicios que ya hicieron completa o parcialmente. Pueden tomar lo ya hecho para completarlos o bien realizarlos desde cero. E incluso pueden usar funciones programadas en ejercicios anteriores de esta misma parte.
No es necesario ningún paquete externo ni adicional salvo el ya usado `fmt`

No se pide armar el programa completo aunque puede hacerlo si lo desea.

### Primera Tanda

#### 1. Construir una función que imprima en pantalla `Hola Mundo!`

#### 2. Construir una función que dado un string imprima en pantalla dicho string.

#### 3. Construir una función que devuelva un string `Hola Mundo!`.

#### 4. Contruir una función que dado un string imprima en pantalla el string subrayado con guiones `-` (solo las palabras) (nombrarla `printTitle`).
Ej: 
```go
printTitle("Programar es divertido!")

> Programar es divertido!
> --------- -- ----------
```

#### 5. Construir una función que dado dos números enteros devuelva la suma.

#### 6. Construir una función que dado un string devuelva el string dado en color verde. (nombrarla `inGreen`)
Pista: buscar en google `console color escape codes`

#### 7. Construir una función que dado un string devuelva el string dado en color rojo. (nombrarla `inRed`)

#### 8. Construir una función que dado un string devuelva el string dado en color amarillo. (nombrarla `inYellow`)

#### 9. Construir una función que dado un string imprima en pantalla el string dado en color verde. (nombrarla `printInGreen`)

#### 10. Construir una función que dado un string imprima en pantalla el string dado en color rojo. (nombrarla `printInRed`)

#### 11. Construir una función que dado un string imprima en pantalla el string dado en color amarillo. (nombrarla `printInYellow`)

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

#### 13. Construir una función que dado un string devuelva el mismo string pero sin espacios por delante. (nombrarla `leftTrim`)

#### 14. Construir una función que dado un string devuelva el mismo string pero sin espacios por detrás. (nombrarla `rightTrim`)

#### 15. Construir una función que dado un string devuelva el mismo string pero sin espacios por delante ni por detrás. (nombrarla `trim`)

#### 16. Construir una función que dado un string y un número entero devuelva el string a partir del número usado como índice. Si el índice es inválido devolver un string vacío.

#### 17. Contruir una función que dado un string y dos números enteros devuelva el string a partir del primer número usado como índice de comienzo y usando el segundo como largo del string. Si el largo es mayor al posible restante, devolver el string hasta el final. Si el índice es inválido devolver un string vacío. (nombrarla `substr`).

#### 18. Construir una función que dado un string y un byte devuelva un entero que represente el índice de la primer ocurrencia de ese byte en el string. Si el byte no se encuentra devolver `-1`. (nombrarla `findFirstChar`).

#### 19. Construir una función que dado un string y un byte devuelva un slice de enteros que represente todos los índices con las ocurrencias de ese byte en el string (nombrarla `findAllChar`).

#### 20. Construir una función que dados dos strings devuelva un entero que represente el índice de la primer ocurrencia del segundo string en el primero. Si el string no se encuentra devolver `-1`. (nombrarla `findFirstString`).

#### 21. Construir una función que dados dos strings devuelva un slice de enteros que contengan los índices de todas las ocurrencias del segundo string en el primero (nombrarla `findAllString`).

#### 22. Construir una función que dado un string y un byte devuelva un slice de strings que contenga todas las particiones del string obtenido de dividirlo por el byte. (nombrarla `splitByChar`)
Ej:
```go
var strings []string = splitByChar("Programar es divertido!", ' ')
fmt.Println(strings)

> ["Programar", "es", "divertido!"]
```

#### 23. Construir una función que dados dos strings devuelva un slice de strings que contenga todas las particiones del primer string obtenido de dividirlo por el segundo string. (nombrarla `splitByString`)
Ej:
```go
var strings []string = splitByString("la cama la puerta y la mesa", "la")
fmt.Println(strings)

> [" cama ", " puerta y ", " mesa"]
```

#### 24. Construir una función que dados dos strings devuelva un bool dependiendo si el primer string contiene al segundo. (nombrarla `contains`)

#### 25. Construir una función que dado un slice de strings y un string devuelva un string con todos los strings del slice concatenados con el string dado. (nombrarla `join`)
Ej:
```go
var strings []string = []string{"hola", "que", "tal?"}
var joinedString string = join(strings, "--")
fmt.Println(joinedString)

> "hola--que--tal?"
```

#### 26. Construir una función que dado un un array de 3 enteros devuelva el mismo array pero invertido (nombrarla `reverseInt3`).
Para pensar: Qué pasaría si en lugar de 3 números enteros, ahora quisiéramos una de 4? y si quisiéramos otra de 5? qué desventaja presenta esto a utilizar un slice?

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

#### 28. Construir una función que dado un slice de strings lo devuelva en orden inverso (nombrarla `reverseString`).

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

#### 30. Construir una función que dado un slice de strings devuelva un slice de números enteros donde cada elemento es el largo del string en la misma posición del slice dado (nombrarla `mapToLength`).
Ej:
```go
var strings []string = []string{"hola", "mundo", "!"}
var lengths []int = mapToLength(strings)
fmt.Println(lengths)

> [4, 5, 1]
```

#### 31. Construir una función que dado un slice de bools devuelva true si todos los valores del slice son true o false si no (nombrarla `allTrue`).

#### 32. Construir una función que dado un slice de bools devuelva true si al menos un valor del slice es true o false si no (nombrarla `anyTrue`).

#### 33. Construir una función que dado un slice de números decimales devuelva la suma de todos (nombrarla `sumFloat`).

#### 34. Construir una función que dado un slice de números decimales devuelva el promedio de todos (nombrarla `averageFloat`).

#### 35. Construir una función que dado un slice de números decimales devuelva un array de 2 números decimales donde en la posición 0 estará el mayor y en la 1 el menor de todos. Si el slice no tiene elementos, devolver el array con 0 en ambos valores (nombrarla `minMaxFloat`).

#### 36. Construir una función que dado un slice de números enteros devuelva un slice con los números ordenados de menor a mayor (nombrarla `ascOrderInt`).

#### 37. Construir una función que dado un slice de números enteros devuelva un slice con los números ordenados de mayor a menor (nombrarla `descOrderInt`).

#### 38. Construir una función que dado un número entero devuelva un string con el día de la semana que representa (nombrarla `dayOfWeek`) según la siguiente tabla:
- 1 -> Domingo
- 2 -> Lunes
- 3 -> Martes
- 4 -> Miércoles
- 5 -> Jueves
- 6 -> Viernes
- 7 -> Sábado
- otro -> Error

#### 39. Construir una función que corrobore el funcionamiento de la función anterior. Debe probar todos los posibles casos (puede crear todas las funciones adicionales que crea convenientes)  e imprimir 
-> `Caso <x> -> OK` -> si la función devolvió lo esperado
-> `Caso <x> -> ERROR` -> si la función no devolvió lo esperado

El `OK` debe aparecer en verde y el `ERROR` debe aparecer en rojo. El `<x>` debe ser reemplazado por el número probado en cada caso.

#### 40. Construir una función que corrobore el funcionamiento de la función `leftTrim`, `rightTrim` y `trim`. Debe probar todos los posibles casos por cada función (puede crear todas las funciones adicionales que crea convenientes)  e imprimir 
- `Caso <x> -> OK` -> si la función devolvió lo esperado
- `Caso <x> -> ERROR` -> si la función no devolvió lo esperado

El `OK` debe aparecer en verde y el `ERROR` debe aparecer en rojo. El `<x>` debe ser reemplazado por el string probado en cada caso.
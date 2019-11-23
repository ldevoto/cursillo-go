### Desafío
En este desafío esperamos que se diviertan. Los ejercicios de manejo de strings, ocurrencias, ordenamiento, máximos, mínimos, matrices son interesantes y ayudan a formar la cabeza pero no son _divertidos_ per se (o tal vez sí pero solo para algunos). Ahora es el momento de poner todo lo aprendido en juego y literalmente **ponerlo en un juego**.

#### Vamos a programar el viejo y conocido Ta-Te-Ti (o Tic-Tac-Toe en inglés) (se asume que conocen el juego) teniendo en cuenta lo siguiente:
- el juego es para 2 jugadores (por ahora no vamos a competir contra la computadora)
- el juego debe ir preguntando uno por uno los movimientos a cada jugador (uno por vez)
- el juego debe mostrar el escenario después de cada jugada para que el jugador que sigue pueda tomar la mejor decisión
- el escenario debe verse de la siguiente manera:
```
   |   |   
-----------
   |   |   
-----------
   |   |   
```
- el juego debe mostrar las fichas (círculos o cruces) dentro del tablero como en el siguiente ejemplo:
```
 O | X | X 
-----------
 X | O | X 
-----------
 X | O | O 
```
- el juego debe solicitar el ingreso de coordenadas de la ficha del jugador con el siguiente formato: `x,y`. O sea si es mi turno y quiero ingresar mi ficha en el cuadrante del medio debería hacerlo ingresando un `2,2` (las coordenadas empiezan en 1)
- el juego debe detenerse en cuanto alguien alinea 3 de sus fichas.
- el juego debe preguntar los nombres de los jugadores
- el juego debe indicar el nombre del ganador
- el juego debe preguntar si quieren jugar de vuelta

Definir muy bien y con cabeza los nombres de las variables. Pensar cuál será su uso y que fin tienen y en base a eso, nombrarlas (nombrar las variables es un tema no menor a la hora de construir software de calidad). El programa debe ser lo más claro posible y estar formateado según las reglas de formateo que plantea GO.

#### Adicional 1
- el juego debe mostrar la linea ganadora del juego dependiendo del caso como en los siguientes ejemplo:
```
Linea horizontal
 X | X | X ←
-----------
   | O | X 
-----------
   | O | O 

Linea vertical
 X | O | X 
-----------
   | O |   
-----------
   | O |   
     ↑

Linea diagonal 1
 O | X | X 
-----------
 X | O |   
-----------
   |   | O 
           ↖

Linea diagonal 2
           ↙
 O | X | X 
-----------
 O | X |   
-----------
 X |   | O 


Caracteres UNICODE:
\u2190 ←
\u2191 ↑
\u2196 ↖
\u2199 ↙
```

#### Adicional 2
- el juego debe poder jugarse contra la computadora.
- la respuesta de la computadora debe dar la sensación de que piensa (no debe ser instantánea)
- el juego solo tendrá un nivel de dificultad y no se pretende que tenga previsibilidad ni anticipo de jugadas
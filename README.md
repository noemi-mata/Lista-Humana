# Lista Humana

## Actividad Nodos

### Ronda 1: Lista Simple ("el tren humano")

Regla: cada nodo solo puede señalar con la mano derecha al siguiente. El último señala al suelo (null).

Retos: 
1. Recorrido: el "profesor" toca la cabeza y solo se puede avanzar siguiendo las manos. Cada nodo 
dice su dato en voz alta.

<video src="https://github.com/noemi-mata/Lista-Humana/issues/1#issue-5968719182" controls width="100%"></video>

3. Insertar al inicio: un nuevo nodo se une. Primero debe señalar al antiguo primero y después recibir 
el gorro. Si lo hacen al revés, ¡la lista se pierde!

4. Insertar en medio: entre el nodo 2 y el 3. Orden correcto: el nuevo señala al 3, y luego el 2 lo señala 
a él.

5. Eliminar un nodo: el nodo anterior "salta" y señala al siguiente del eliminado, que sale de la fila.
 
6. Buscar: "¿Dónde está el 7?" Solo se puede preguntar siguiendo la cadena desde la cabeza, sin 
saltarse a nadie.


#### Pregunta de reflexión: 
#### ¿Se puede retroceder? 
No, no se puede retroceder. Cada nodo solo tiene la mano derecha, que señala al siguiente, así que no sabe quién está detrás de él.
#### ¿Qué pasó cuando alguien pidió "dame el anterior"? 
Cuando alguien pidió “dame el anterior”, el nodo no pudo responder porque no tiene ningún puntero hacia atrás. La única forma de llegar al anterior es volver a empezar desde la cabeza y recorrer toda la fila hasta encontrar al nodo que lo señala a él.


-----------------------------------------------------------------------------------------------------------

### Ronda 2: Lista doble (el "abrazo de dos manos") 

Regla: ahora cada nodo usa ambas manos. La derecha señala al siguiente y la izquierda al anterior. La  mano izquierda de la cabeza y la derecha de la cola señalan a null (manos al suelo). 

Retos: 
1. Recorrido hacia adelante y hacia atrás: el docente grita "¡Adelante!" o "¡Atrás!" y se pasa un objeto  (una pelota) en esa dirección.
  
2. Insertar en medio: ahora hay que arreglar 4 punteros (el nuevo señala a sus dos vecinos y los dos  vecinos lo señalan a él). Cronometren cuánto tarda cada equipo.
   
3. Eliminar sin conocer al anterior: el nodo a eliminar levanta la mano y dice "¡yo me elimino!".  Gracias a su mano izquierda, él mismo conecta a sus dos vecinos.
   
4. Invertir la lista: cada nodo intercambia sus manos (siguiente ↔ anterior) y la cabeza pasa a la cola.

   
#### Pregunta de reflexión: 
#### ¿Qué ventaja tuvo la doble sobre la simple? 
Se puede recorrer en los dos sentidos, adelante y atrás, como cuando se pasó la pelota en ambas direcciones.
Eliminar un nodo es más fácil, porque el nodo sabe quién está antes y quién está después. Por eso pudo decir “¡yo me elimino!” y conectar a sus dos vecinos sin ayuda.
Invertir la lista es más sencillo, porque basta con que cada nodo intercambie sus manos.

#### ¿Qué costo tuvo (más punteros, más  cuidado)?
Cada nodo necesita dos punteros en lugar de uno, así que ocupa más memoria.
Hay que tener más cuidado al insertar o eliminar. En la lista simple se arreglaban 2 punteros, y en la doble hay que arreglar 4. Si se olvida uno, la lista queda mal conectada o algún nodo queda perdido.

-----------------------------------------------------------------------------------------------------------

### Ronda 3: Lista circular (el "círculo sin fin") 

Regla: el último nodo señala con su mano derecha a la cabeza (ya no hay null). Formen un círculo. En la  doble circular, la mano izquierda de la cabeza también señala al último. 

Retos: 
1. La papa caliente: pasen una pelota siguiendo los punteros mientras suena una canción. Cuando  para, quien la tiene hace una pregunta o un reto. (Esto demuestra que nunca se llega al final.)
  
2. El peligro del ciclo infinito: pidan a un voluntario que recorra "hasta encontrar null". ¡Nunca lo  encontrará! Hagan que digan en voz alta la condición de parada correcta: "me detengo cuando  vuelvo a la cabeza".
   
3. Insertar y eliminar la cabeza: al quitar la cabeza, ¿quién señala a quién? Hay que actualizar el  puntero del último nodo.
   
4. Turnos rotativos (simulación de Round Robin): cada nodo tiene "3 segundos" de turno y pasa al  siguiente. Se puede relacionar con el procesador o con un juego de turnos.
   
#### Pregunta de reflexión: 
#### ¿Para qué sirve una lista circular en la vida real? (turnos, reproductores de música en  bucle, buffers) 

Sirve cuando algo se repite una y otra vez sin tener un final. Algunos ejemplos:

Turnos: en juegos de mesa o en el procesador de una computadora (Round Robin), cada quien tiene su turno y al terminar vuelve a empezar.
Reproductores de música en bucle: al acabar la última canción, vuelve a sonar la primera.
Buffers: son espacios de memoria que se llenan y se reutilizan de forma circular, como en la transmisión de video o audio.
Otros casos: el cambio de luces de un semáforo, o las ventanas que se alternan al presionar Alt + Tab.

-----------------------------------------------------------------------------------------------------------

### Cierre: Desafío final por equipos  

Cada equipo recibe una "orden" escrita en un papel y debe ejecutarla en un tiempo límite, sin errores de  punteros.

## DESAFIO RONDA 1

## DESAFIO RONDA 2

## DESAFIO RONDA 3



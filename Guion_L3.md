# Lección 3: Estructuras de control: Decisiones y bucles (10 minutos)

## Notas para el profesor

* Esta lección es clave — las estructuras de control son el corazón de la lógica del juego.
* Usa ejemplos de la vida cotidiana antes del código: decisiones y repeticiones que los chicos ya conocen.
* El if/else y el while pueden parecer abstractos — el videojuego los hace concretos e inmediatos.
* Al escribir en vivo, lee el código en voz alta como si fuera español: "Si la vida es mayor que cero, el personaje sigue vivo. Si no, perdió." Esto ayuda muchísimo a los principiantes.
* Cuando muestres el código completo, asegúrate de que todos lo corran y vean el resultado antes de pasar a la siguiente lección.

## Guión

**[APERTURA]**

"Ya tenemos un personaje con nombre, vida y ataque. Ahora viene la pregunta importante: ¿cómo decide el programa qué hacer? ¿Cómo sabe si el personaje ganó o perdió? ¿Cómo sabe cuántos turnos jugar? Para eso existen las estructuras de control."

**[SUBTEMA 1 — ¿Qué es una condición? El if y el else]**

"Todos tomamos decisiones todo el tiempo. Si tengo hambre, como. Si no tengo hambre, no como. En programación funciona exactamente igual — se llama un if/else."

"if significa 'si'. else significa 'si no'. El programa evalúa una condición, y dependiendo de si es verdadera o falsa, hace una cosa u otra."

"En nuestro juego: si la vida del personaje es mayor que cero, sigue peleando. Si no, perdió. Así de directo."

***
if (vida > 0) {

System.out.println(nombrePersonaje + " sigue en pie!");

} else {

System.out.println(nombrePersonaje + " ha sido derrotado.");

}
***

"Lean esto como español: si la vida es mayor que cero, imprime que sigue en pie. Si no, imprime que fue derrotado. El programa toma esa decisión solo, en un instante."

**[SUBTEMA 2 — ¿Qué es un bucle? El for y el while]**

"Ahora, ¿qué pasa cuando algo se repite? En un juego de combate por turnos, los turnos se repiten una y otra vez hasta que alguien gana. No vamos a escribir el mismo código cien veces — para eso existen los bucles."

"El bucle while dice: mientras esta condición sea verdadera, sigue repitiendo. En cuanto la condición sea falsa, para."

"En nuestro juego: mientras el personaje tenga vida, el combate continúa. Cuando la vida llegue a cero, el bucle termina y el juego sabe que alguien perdió."

**[PARTE PRÁCTICA — Construimos: la lógica de turnos del juego]**

"Vamos al código. Voy a escribir en vivo la lógica de turnos — síganme línea por línea."

***
int vidaEnemigo = 80;

int turno = 1;

while (vida > 0 && vidaEnemigo > 0) {

System.out.println("--- Turno " + turno + " ---");

vidaEnemigo = vidaEnemigo - ataque;

System.out.println("Atacaste al enemigo! Vida enemigo: " + vidaEnemigo);

turno++;

}

if (vidaEnemigo <= 0) {

System.out.println("¡Ganaste! El enemigo fue derrotado.");

} else {

System.out.println("Perdiste. Tu personaje cayó en batalla.");

}
***

"El while dice: mientras yo tenga vida Y el enemigo tenga vida, seguimos. Cada turno, el enemigo recibe daño. Cuando su vida llega a cero, el bucle para y el if decide quién ganó."

"El turno++ es una forma corta de decir turno = turno + 1. Es solo un contador para saber en qué turno vamos."

**[El profesor muestra el código completo y el resultado en pantalla:]**

"Ahora escríbanlo en sus computadoras. Cuando lo corran van a ver los turnos aparecer uno a uno hasta que el enemigo cae. El juego ya tiene movimiento — ya tiene acción."

**[CIERRE]**

"¿Lo sienten? El juego ya vive. Ya toma decisiones, ya repite acciones, ya sabe quién gana. En la próxima lección vamos a ordenar todo esto en métodos — para que el código sea limpio, organizado, y el jugador pueda ver los mensajes en pantalla de forma clara. Seguimos."






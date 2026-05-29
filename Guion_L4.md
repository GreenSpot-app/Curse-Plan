# Lección 4: Métodos, Entrada/Salida e Introducción a la POO (12 minutos)

## Notas para el profesor

* Esta lección tiene tres conceptos en 12 minutos — administra bien el tiempo.
* Los métodos pueden parecer innecesarios al principio. Usa la analogía de las recetas: en lugar de repetir los pasos cada vez, los escribes una sola vez y los llamas cuando los necesitas.
* System.out.println() ya lo han visto — refuérzalo, no es nuevo. Lo nuevo es Scanner para recibir input del jugador.
* La introducción a la POO al final es una semilla, no una explicación completa. Solo deben salir con la pregunta: ¿y si pudiéramos empaquetar todo esto en una sola cosa? La respuesta llega en la Lección 5.
* Si el tiempo aprieta, el Scanner puede mostrarse rápido — lo importante es que vean que el jugador puede interactuar con el juego.

## Guión

**[APERTURA]**

"El juego ya funciona. Pero si lo miran, el código empieza a crecer. Variables por aquí, bucles por allá, condiciones mezcladas. A medida que un programa crece, necesitamos organizarlo mejor. Y para eso existen los métodos."

**[SUBTEMA 1 — ¿Qué es un método y por qué nos ayuda?]**

"Piensen en una receta de cocina. En vez de escribir todos los pasos cada vez que quieren hacer una torta, la escriben una sola vez, le ponen nombre, y cada vez que la necesitan simplemente dicen: 'hacer torta'. Eso es un método."

"Un método es un bloque de código con nombre que hace una tarea específica. Lo escribes una vez, lo llamas cuando lo necesitas, las veces que quieras."

"En nuestro juego, el ataque es una acción que se repite cada turno. En vez de escribir ese código dentro del bucle, lo metemos en un método llamado atacar() — y simplemente lo llamamos cuando toca."

**[SUBTEMA 2 — Cómo crear y llamar un método en Java]**

"Así se ve un método en Java:"

***
static void mostrarEstado(String nombre, int vida) {

System.out.println(nombre + " - Vida: " + vida);

}
***

"static void es la forma de declarar el método — no se preocupen mucho por eso ahora, lo van a entender mejor cuando lleguemos a clases. mostrarEstado es el nombre que le damos. Entre paréntesis van los datos que necesita para funcionar — en este caso el nombre y la vida del personaje."

"Y para llamarlo, simplemente escribimos su nombre:"

***
mostrarEstado("Guerrero", 100);
***

"Así de simple. Una línea, y el método hace todo el trabajo."

**[SUBTEMA 3 — Entrada y salida: System.out.println() y Scanner]**

"Ya conocen System.out.println() — eso es salida, el programa le muestra información al jugador. Pero ¿qué pasa si queremos que el jugador también pueda escribir algo? Para eso existe Scanner."

"Scanner le permite al programa escuchar lo que escribe el usuario. En nuestro juego, podemos usarlo para que el jugador elija el nombre de su personaje al inicio."

***
Scanner scanner = new Scanner(System.in);

System.out.println("¿Cómo se llama tu personaje?");

String nombrePersonaje = scanner.nextLine();

System.out.println("¡Bienvenido, " + nombrePersonaje + "!");
***

"El programa pregunta, el jugador escribe, y el programa guarda esa respuesta en una variable. Ya hay conversación entre el juego y el jugador."

**[SUBTEMA 4 — Primera mirada a la POO: ¿qué problema resuelve?]**

"Ahora miren todo lo que tenemos: variables del personaje, métodos del personaje, lógica del personaje. Todo suelto, disperso por el código. ¿No sería mejor tener todo eso junto, empaquetado en una sola cosa llamada Personaje?"

"Eso es exactamente lo que hace la Programación Orientada a Objetos. En lugar de tener variables y métodos sueltos, los agrupamos en algo llamado clase. Y de esa clase creamos objetos — personajes reales, con sus propios datos."

"En la próxima lección vamos a hacer exactamente eso. Vamos a crear la clase Personaje, y de ahí vamos a sacar a nuestros dos luchadores. El juego va a quedar completo."

**[PARTE PRÁCTICA — Construimos: el método atacar() y los mensajes del juego]**

"Vamos al código. Escriban conmigo el método atacar() y los mensajes que verá el jugador en pantalla."

[El profesor escribe en vivo:]
***
static void atacar(String atacante, String defensor, int dano, int vidaRestante) {

System.out.println(atacante + " ataca a " + defensor + " por " + dano + " puntos!");

System.out.println(defensor + " le queda " + vidaRestante + " de vida.");

}
***

**[El profesor muestra el código completo con el método integrado al juego:]**

"Córranlo. Escriban su nombre cuando el juego lo pida y vean cómo se desarrolla el combate. Ya hay un jugador real interactuando con el juego."

**[CIERRE]**

"El juego ya habla con el jugador, ya organiza su código en métodos, ya tiene estructura. En la próxima lección damos el salto final — creamos la clase Personaje y lo convertimos en un juego completo y profesional. Es la lección más importante. Prepárense."

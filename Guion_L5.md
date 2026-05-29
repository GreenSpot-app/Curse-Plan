# Lección 5: Fundamentos de POO y programas sencillos (15 minutos)

## Notas para el profesor

* Esta es la lección más densa y más emocionante del curso — administra bien los 15 minutos.
* El concepto de clase y objeto es el más abstracto hasta ahora. Usa la analogía del molde antes de tocar el código — que lo entiendan visualmente primero.
* Escribe la clase Personaje línea por línea, explicando cada parte. No la muestres completa de golpe.
* El momento en que corren el juego completo por primera vez es el pico emocional del curso — dales espacio para celebrarlo. Que sientan el logro.
* Si algún estudiante tiene un error, normalízalo: "Los errores son parte de programar, hasta los mejores programadores del mundo los tienen."
* Al final de esta lección el juego debe estar 100% funcional en las computadoras de todos.

## Guión

**[APERTURA]**

"Este es el momento. Todo lo que aprendieron hasta ahora — variables, condiciones, bucles, métodos — fue preparación para esto. Hoy lo unimos todo en la herramienta más poderosa de Java: las clases y los objetos."

**[SUBTEMA 1 — ¿Qué es una clase y qué es un objeto?]**

"Piensen en un molde de galletas. El molde define la forma — dice que toda galleta tiene esta figura, este tamaño. Pero el molde no es una galleta. Las galletas son lo que produces con ese molde."

"En programación, la clase es el molde. El objeto es la galleta — algo real, concreto, que creaste a partir de ese molde."

"En nuestro juego, vamos a crear una clase llamada Personaje. Esa clase define que todo personaje tiene un nombre, una vida y un ataque. Y de esa clase vamos a crear dos objetos: el héroe y el enemigo. Cada uno con sus propios valores, pero ambos siguiendo el mismo molde."

**[SUBTEMA 2 — Atributos y métodos dentro de una clase]**

"Una clase tiene dos cosas: atributos y métodos."

"Los atributos son las características — los datos que definen al objeto. Para nuestro Personaje: nombre, vida y ataque."

"Los métodos son las acciones — lo que el objeto puede hacer. Para nuestro Personaje: atacar a otro personaje y mostrar su estado."

"Todo junto, dentro de una sola clase. Organizado, limpio, reutilizable."

**[PARTE PRÁCTICA — Construimos: la clase Personaje y el juego completo]**

"Vamos al código. Voy a escribir la clase Personaje línea por línea — síganme."

***

    public class Personaje {

    // Atributos
    String nombre;
    int vida;
    int ataque;

    // Constructor
    Personaje(String nombre, int vida, int ataque) {
        this.nombre = nombre;
        this.vida = vida;
        this.ataque = ataque;
    }

    // Método atacar
    void atacar(Personaje enemigo) {
        enemigo.vida = enemigo.vida - this.ataque;
        System.out.println(this.nombre + " ataca a " + enemigo.nombre + 
                           " por " + this.ataque + " puntos!");
        System.out.println(enemigo.nombre + " le queda " + enemigo.vida + " de vida.");
    }

    // Método mostrar estado
    void mostrarEstado() {
        System.out.println(this.nombre + " - Vida: " + this.vida + 
                           " | Ataque: " + this.ataque);
    }
    }
***

"Miren el constructor — ese método especial que tiene el mismo nombre que la clase. Es lo que usamos para crear un personaje nuevo con sus valores. this significa 'este objeto' — es la forma en que la clase se refiere a sí misma."

**[SUBTEMA 3 — Instanciar objetos y usarlos en el programa]**

"Ahora que tenemos el molde, vamos a crear los dos personajes del juego. Esto se llama instanciar un objeto — crear una galleta a partir del molde."

    Personaje heroe = new Personaje("Guerrero", 100, 15);
    Personaje enemigo = new Personaje("Dragón", 120, 12);

"Con new Personaje() le decimos a Java: crea un objeto real usando esta clase. El héroe tiene 100 de vida y 15 de ataque. El dragón tiene 120 de vida y 12 de ataque. Dos objetos distintos, mismo molde."

**[SUBTEMA 4 — El juego completo: dos personajes se enfrentan]**

"Ahora unimos todo. Aquí está el juego completo — escríbanlo en sus computadoras."

**[El profesor muestra el código completo del juego:]**

"Córranlo. Escriban el nombre de su personaje y vean el combate desarrollarse turno a turno hasta el final."

**[CIERRE DEL JUEGO]**

"¿Lo ven funcionando? Eso que acaban de construir es un programa real, orientado a objetos, escrito en Java. El mismo lenguaje que usan desarrolladores profesionales en todo el mundo."

"Hace menos de una hora no sabían nada de programación. Ahora tienen un videojuego funcionando. Eso es real. Eso lo hicieron ustedes."

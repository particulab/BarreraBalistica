# Barrera Balística

**Barrera Balística** es un minijuego educativo de física desarrollado para **EulerGames**.
El objetivo es proteger un barco colocando bombas flotantes sobre la trayectoria de un misil enemigo.

El juego trabaja conceptos de movimiento rectilíneo con aceleración constante, distancia de frenado, vectores, ángulos y coordenadas cartesianas.

## Descripción del juego

Un misil enemigo se aproxima hacia un barco siguiendo una trayectoria rectilínea. Antes de que el misil entre en escena, el jugador debe lanzar bombas desde una batería defensiva ubicada en el plano cartesiano.

Cada bomba tiene:

* una velocidad inicial (v_0),
* una aceleración negativa (a),
* un ángulo de lanzamiento elegido por el jugador.

La bomba se mueve hasta detenerse. Cuando su velocidad llega a cero, queda flotando en el mar. Para destruir el misil enemigo, este debe impactar contra tres bombas.

## Objetivo

Colocar suficientes bombas sobre la trayectoria del misil para detenerlo antes de que impacte el barco.

Se necesitan **3 impactos de bomba** para destruir un misil.

## Física utilizada

El movimiento de cada bomba se basa en la ecuación:

```text
vf² = v0² + 2as
```

Como la bomba se detiene cuando (vf = 0), el jugador puede calcular la distancia de frenado con:

```text
s = -v0² / 2a
```

donde:

* `v0` es la velocidad inicial de la bomba,
* `a` es la aceleración negativa,
* `s` es la distancia recorrida antes de detenerse.

Después, el jugador debe elegir el ángulo adecuado para colocar la bomba sobre la trayectoria del misil.

## Controles

* Flecha izquierda: disminuir el ángulo en 1°
* Flecha derecha: aumentar el ángulo en 1°
* Flecha abajo: disminuir el ángulo en 0.1°
* Flecha arriba: aumentar el ángulo en 0.1°
* Barra espaciadora: disparar bomba
* Enter: pausar/reanudar
* Botón en pantalla: disparar, pausar, reiniciar y activar sonido

## Mecánica principal

1. El juego muestra la trayectoria del misil enemigo.
2. El jugador revisa los datos de la bomba cargada.
3. Calcula la distancia de frenado.
4. Ajusta el ángulo de disparo.
5. Lanza la bomba.
6. La bomba se detiene y queda flotando.
7. El misil aparece al terminar la cuenta regresiva.
8. Si el misil toca tres bombas, es destruido.
9. Si no, impacta el barco.

El juego continúa por rondas. Después de cada ronda, el jugador puede continuar defendiendo el barco o terminar la partida.

## Tecnologías utilizadas

Este juego está hecho con:

* HTML
* CSS
* JavaScript
* Canvas API
* Web Audio API

No requiere librerías externas ni instalación.

## Cómo ejecutar

Descarga o clona este repositorio y abre el archivo:

```text
index.html
```

en cualquier navegador moderno.

También puede publicarse directamente con GitHub Pages.

## Proyecto EulerGames

**EulerGames** es un proyecto de minijuegos educativos basados en física y matemáticas.
La idea es que el estudiante no sólo interactúe con una simulación, sino que tenga que calcular, razonar y tomar decisiones dentro del juego.

## Estado del proyecto

Versión inicial jugable.

Posibles mejoras futuras:

* selector de dificultad,
* explicación externa del problema,
* modo práctica,
* historial de rondas,
* retroalimentación matemática después de cada intento,
* más juegos dentro del ecosistema EulerGames.

## Autor

Desarrollado como parte del proyecto **EulerGames**.

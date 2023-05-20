# PeopleVZombies

En este repositorio, podemos encontrar el original juego multijugador PeopleVZombies, además del código que lo implementa y una breve descripción y explicación del mismo.

PeopleVZombies parte de la premisa de que un virus se ha extendido por el planeta. Este virus provoca en las personas contagiadas tendencias agresivas y la pérdida de la razón, es decir, las "convierte" en zombies. La historia consiste en que dos personas (los jugadores) se encuentran rodeados por los zombies, y deben resistir hasta la llegada de la ayuda militar sin que los zombies acaben con ellos.

El escenario del juego es el que podemos ver en la imagen:

![game](https://github.com/pabsan16/PeopleVZombies/assets/124245920/54a1e191-d9dc-4501-bc42-2d169a26bfad)

La victoria se dará cuando ambos jugadores aguanten vivos durante 60 segundos (lo que tarda en llegar la ayuda militar). En cambio, serán derrotados si cualquiera de los dos cae antes de que se cumpla ese plazo de tiempo.

Hemos diseñado una pantalla de bienvenida al juego, y otras dos de despedida (una para cuando se gana y una para cuando se pierde).

El jugador principal lo ejecuta desde el archivo sala.py (es el host), y el segundo jugador desde player.py (es el guest).

Para la comunicación entre ambos jugadores hemos importado desde la librería Multiprocessing Listener y Client.

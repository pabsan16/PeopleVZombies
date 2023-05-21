    Javier Martinez Pérez
    Judit Nieto Parla
    Pablo Sánchez Rico

# PeopleVZombies
En este repositorio, podemos encontrar el original juego multijugador PeopleVZombies, además del código que lo implementa y una breve descripción y explicación del mismo. En el archivo memoria_PeopleVZombies se explica en detalle el código implementado.

PeopleVZombies parte de la premisa de que un virus se ha extendido por el planeta. Este virus provoca en las personas contagiadas tendencias agresivas y la pérdida de la razón, es decir, las "convierte" en zombies. Dos supervivientes (los jugadores) se encuentran rodeados de zombies y deberán resistir hasta la llegada de ayuda militar.

El escenario del juego es el que podemos ver en la imagen:

![game](https://github.com/pabsan16/PeopleVZombies/assets/124245920/54a1e191-d9dc-4501-bc42-2d169a26bfad)

El jugador principal ejecutará el juego desde el archivo host.py de la siguiente forma
    
    python3 host.py ip_address_host

donde ip_address_host es la dirección ip del jugador principal. El segundo jugador desde guest.py

    python3 guest.py ip_address_host
    
Las imágenes utilizadas, los mapas y la música los podemos encontrar en las carpetas img, maps y music, respectivamente. La información principal del juego se encuentra en el archivo main.py.

La victoria se dará cuando ambos jugadores aguanten vivos durante 60 segundos, que es lo que tarda en llegar la ayuda militar. En cambio, serán derrotados si cualquiera de los dos cae antes de que se cumpla ese plazo de tiempo.

Hemos diseñado una pantalla de bienvenida al juego, y otras dos de despedida, una para cuando los jugadores ganan y otra para cuando pierden.

El juego se desarrolla en modo multijugador, permitiendo que dos personas se conecten y jueguen juntas. Para la comunicación entre ambos jugadores hemos importado desde la librería Multiprocessing Listener y Client. El host inicia la conexión con un listener y espera a que haya otro jugador que se conecte (el guest), quien se conectará mediante el client.

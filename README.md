    Javier Martinez Pérez
    Judit Nieto Parla
    Pablo Sánchez Rico

# PeopleVZombies
En este repositorio, podemos encontrar el original juego multijugador PeopleVZombies, además del código que lo implementa y una breve descripción y explicación del mismo. En el archivo memoria_PeopleVZombies se explica en detalle el código implementado.

PeopleVZombies parte de la premisa de que un virus se ha extendido por el planeta. Este virus provoca en las personas contagiadas tendencias agresivas y la pérdida de la razón, es decir, las "convierte" en zombies. Dos supervivientes (los jugadores) se encuentran rodeados de zombies y deberán resistir hasta la llegada de ayuda militar.

El escenario del juego es el que podemos ver en la siguiente imagen

![game](https://github.com/pabsan16/PeopleVZombies/assets/124245920/54a1e191-d9dc-4501-bc42-2d169a26bfad)

Las imágenes utilizadas, los mapas y la música los podemos encontrar en las carpetas img, maps y music, respectivamente. La información esencial del juego se encuentra en el archivo main.py.

El jugador principal ejecutará el juego desde el archivo host.py de la siguiente forma
    
    python3 host.py ip_address_host

donde ip_address_host es la dirección ip del jugador principal. El segundo jugador lo hará desde guest.py

    python3 guest.py ip_address_host 

El juego se desarrolla en modo multijugador, permitiendo que dos personas se conecten y jueguen juntas. Para la comunicación entre ambos jugadores hemos importado desde la librería Multiprocessing Listener y Client. El host inicia la conexión con un listener y espera a que haya otro jugador que se conecte (el guest), quien se conectará mediante el client.

Los controles de los jugadores son los siguientes
    a w d s
    ◀ ▲ ▶ ▼
para desplazarse hacia la izquierda, arriba, derecha o abajo, respectivamente. Si se desea disparar a los zombies se pulsará espacio.

La victoria se dará cuando ambos jugadores aguanten vivos durante sesenta segundos, pues es lo que tarda en llegar la ayuda militar. En cambio, serán derrotados si cualquiera de los dos cae antes de que se cumpla ese plazo de tiempo.

Se ha diseñado una pantalla de bienvenida al juego que se muestra cuando ambos jugadores se conectan. De la misma manera, se han diseñado otras dos pantallas diferentes dependiendo de si los jugadores han sobrevivido o no.

Los zombies son hábiles y resistentes. ¿Podrás sobrevivir a la invasión?

# El Gran Desafío

Rosco multijugador de Biología para 1º año (Salta). Dos estudiantes compiten **en línea, cada uno desde su compu**, con el mismo banco de conceptos que el rosco de la cátedra. También se puede jugar de a dos en la misma compu o contra Boti.

## Jugar

Un solo archivo: `index.html` (GitHub Pages: https://patodoc27.github.io/pasapalabra-bio-online/).

1. Elegí **En línea**, escribí tu nombre, avatar y sección.
2. Dejá el código vacío y tocá **Crear sala**: aparece un código de 4 caracteres.
3. Tu rival escribe ese código (o toca la sala en la lista de "Salas esperando rival") y entra.
4. Quien creó la sala toca **Sortear rosco y empezar**. Se turnan letra por letra; quien no tiene el turno ve la letra, pero no la definición.
5. Al final se ve el duelo, se puede **Pedir revancha** o **Practicar las que costaron** (a solas).

## Tiempos

- **Normal · 7 min** o **Rápido · 5 min** de partida (el reloj corre solo mientras alguien responde), o **Sin reloj · práctica**.
- **Cada letra tiene su propio tiempo**, el que necesita un estudiante de 12-13 años: leer la definición (~2,5 palabras/s; si la lee la voz, ese rato no cuenta), pensar (~8 s) y escribir la palabra (~1,3 caracteres/s). Redondeado a 5 s, entre 15 y 45 s (en Rápido, 20 % menos). Si se agota, la letra vuelve como pasapalabra; si ya había vuelto, cuenta como error.

## Cómo funciona la conexión

- Canal en tiempo real de **Supabase Realtime** (broadcast + presence, plan gratuito), el mismo proyecto que usa Activate. No crea tablas ni guarda datos: solo pasa mensajes entre las dos compus de cada sala.
- Quien tiene el turno decide su jugada y la anuncia; las dos compus aplican la misma regla. Si alguien recarga la página o se le corta internet, vuelve a la misma sala y recupera la partida.
- Límites del plan gratuito: 200 conexiones simultáneas (≈ 100 partidas a la vez).

## Ranking

Usa una **planilla nueva**, separada de la del rosco original. Pasos en `instrucciones_ranking.md`. Mientras `RANKING_URL` esté vacía, el juego anda igual pero no muestra el ranking.

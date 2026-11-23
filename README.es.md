*This readme is written in SPANISH. If you prefer, you can read this in [English](README.md).*

# Figurante

Videojuego de detectives ambientado en la multitud de un carnaval. Hecho en Unity, C#, durante la Global Game Jam 2026 (48 horas) en el Teatro Argentino de La Plata.

Podés jugarlo en [itch.io](https://manuellegago.itch.io/figurante).

## Tecnologías

Desarrollado con:
- Lenguaje C#
- Unity 6.3 LTS (URP 2D)

*Podés ver el código [acá](Assets/_Scripts/).*

## Controles

- Moverse: W A S D
- Hablar / Acusar: mantener Espacio 1 segundo
- Pausa: Esc o P

## Idea y desarrollo

Empieza otra temporada de carnavales y alguien planea un homicidio. La única pista es una nota anónima que encontrás al entrar.

La idea era un juego corto de deducción donde se lee una multitud en lugar de una escena del crimen: infiltrarse en el carnaval, escuchar a los testigos y reconstruir la máscara de quien dejó la nota antes de que termine la noche.

## Implementación

Cada asistente usa una máscara armada con tres rasgos al azar: sombrero, ornamento y ojos. La multitud tiene 60 personas y solo una tiene la combinación de quien planea el crimen.

Después del tutorial, algunas personas se vuelven testigos y levantan la mano con el tiempo. Cada una recuerda un rasgo, pero no todas dicen la verdad: por cada rasgo hay dos testimonios falsos y dos verdaderos. Un rasgo se confirma en el identikit recién cuando dos testigos coinciden.

El reloj corre de 23:58 a medianoche mientras avanza una carroza por la calle. Acusar a la persona correcta gana la partida; una acusación equivocada, o llegar a medianoche, la termina.

## Links y créditos

- Desarrollo: Tomás Marmoni ([tdm1094](https://github.com/tdm1094)), Germán DiFrancesco ([GermanDiFrancesco](https://github.com/GermanDiFrancesco)), Facundo Bravo
- Narrativa: Facundo Bravo, Fera Zuccarelli
- Arte y diseño: Fera Zuccarelli (assets de máscaras de [Freepik](https://www.freepik.com))
- Sonido y composición: Manu Elle ([itch.io](https://manuellegago.itch.io))
- Tipografía: Adelphe
